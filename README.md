# DotnetCode


using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;


namespace SoloLearn
{

    class Product
    {
        public int Id{get;set;}
        public string name{get;set;}
        public int price{get;set;}
        public string companyName{get;set;}


        public override string ToString()
        {
            return $"ID {Id} Name {name} Price {price} Companyname{companyName}";

        }
    }
	class Program
	{
		static void Main(string[] args)
		{
			List<Product> product=new List<Product>()
            {
                new Product{Id=1,name="mouse",price=120,companyName="Dell"},
              new Product{Id=2,name="Tv",price=10000,companyName="Sony"},
         new Product{Id=3,name="laptop",price=27000,companyName="Lenovo"},
                new Product{Id=4,name="Mobile",price=12000,companyName="Redmi"}



            };
            var result =from p in product
                       select p;

                       foreach(var item in result)
                       {
                           Console.WriteLine(item);
                       }
                       var result1 =from p in product
                       where p.price>20000 select p;

                       foreach(var item in result1)
                       {
                           Console.WriteLine(item);
                       }
                       var result2 =from p in product
                        where p.price<1000 select p;

                       foreach(var item in reult2)
                       {
                           Console.WriteLine(item);
                       }
      var result3 =from p in product companyName.StartWith("D") select p;

                       foreach(var item in result3)
                       {
                           Console.WriteLine(item);
                       }
                       var result4 =from p in product companyName.EndWith("e") select p;

                       foreach(var item in reult4)
                       {
                           Console.WriteLine(item);
                       }
                       
                       var result5 =from p in product copanyName.Contains("m") || companyname.Contains("M") select p;

                       foreach(var item in result5)
                       {
                           Console.WriteLine(item);
                       }
                       var result6=from p in product where p.price>15000 order by price;


                       foreach(var item in result6)
                       {
                           console.WriteLine(item);
                       }

		}
	}
}








// Employee


using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;


namespace SoloLearn
{

   
    class Employee
    {
        public int Id{get;set;}
        public string name{get;set;}
        public int salary{get;set;}
        public string city{get;set}

        public override string ToString()
        {
            return $"Id={Id}  Name={name}  Salary={salary}  City={city}";
        }
    }
	class Program
	{
		static void Main(string[] args)
		{
			List<Employee> employee=new List<Employee>()
            {
                new Employee{Id=1,name="Yogesh",salary=35000,city="Nagpur"},
                new Employee{Id=2,name="Dhiraj",salary=30000,city="Chandrapur"},
                new Employee{Id=3,name="Sanket",salary=38000,city="Pune"},
                new Employee{Id=4,name="Pranav",salary=33000,city="Mumbai"},
                new Employee{Id=5,name="Mayur",salary=25000,city="Nashik"},


            };
            var result= from e in employee select e;
            foreach(var item in result)
            {
                Console.WriteLine(item);
            }


            var result1=from e in employee where salary>30000 order by name 
            select e;
            foreach(var item in resutl1)
            {
                Console.WriteLine(item);
            }

            var result2==from e in employee where salary>25000 select e;
            foreach(var item in result2)
            {
                Console.WriteLine(item);
            }

            var result3=from e in employee where city="Pune" select e;
            foreach(var item in result3)
            {
                Console.WriteLine(item);
            }
            var result4=from e in employee order by salary descending select e;
            foreach(var item in result4)
            {
                Console.WriteLine(item);
            }

            var result5=from e in employee where name.StartWith("P");
            foreach(var item in result5)
            {
                Console.WriteLine(item);
            }
            var result6=from e in employee where salary>25000 && where city="Mumbai" select e;
            foreach(var item in result6)
            {
                Console.WriteLine(item);
            }


		}
	}
}
