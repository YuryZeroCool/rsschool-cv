 ## CURRICULUM VITAE 
-------
### 1. Yury Kishkurno
### 2. My contacts for communication:
  * number: tel. +375297337323
  * email : [Kishkurno.yury@yandex.by](Kishkurno.yury@yandex.by)
  * [LinkedIn](https://www.linkedin.com/in/%D1%8E%D1%80%D0%B8%D0%B9-%D0%BA%D0%B8%D1%88%D0%BA%D1%83%D1%80%D0%BD%D0%BE-3514a4183/)
  * [GitHub](https://github.com/YuryZeroCool)
 ### 3. I work as a maintenance engineer. I am fond of programming for five years I want to try myself in programming.
 ### 4. I have language programming skills in C#, C++, JS, Entity Framework core, SQL, React, Angular, CSS, Gulp, GitHub,Azure DveOps. 
 ### 5.

 ```
using CES.DocumentHelper.DAL.Models;
using CES.DocumentHelper.DAL.Models.Department;
using Microsoft.EntityFrameworkCore;
using System;
namespace CES.DocumentHelper.DAL.EF
{
    public class DocHelperDbContex : DbContext
    {
        public virtual DbSet<Driver> Drivers { get; set; }
        public  virtual  DbSet<DriverLicense> DriverLicenses { get; set; }
        public virtual DbSet<Department> Departments { get; set; }

        protected override void OnConfiguring(DbContextOptionsBuilder optionsBuilder)
        {
           var connStg = Environment.GetEnvironmentVariable("CONNECTION_STRING");
            optionsBuilder.UseSqlServer(connStg);
            //optionsBuilder.UseSqlServer("Data Source=DESKTOP-M6S9KU1\\SQLEXPRESS;Initial Catalog=DocHelperDb_dev;Trusted_Connection=True;");

        }
                       
        protected override void OnModelCreating(ModelBuilder modelBuilder)
        {
            modelBuilder
                .Entity<Driver>()
                .HasOne(t => t.DriverLicense)
                .WithOne(p => p.Driver)
                .HasForeignKey<DriverLicense>(c => c.DriveId);
        }
    }
}
 ``` 
 ### 6.
 ### 7. Higher education. Belarusian State University of Informatics and Radioelectronics.
 ### 8. English Level-A0.

           


