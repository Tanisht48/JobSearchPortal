# JobSearchPortal

## FrameWork and Language
    Framework:SpringBoot
    Language : Java
## Dependencies
    SpringBoot Starter Web
    Lombok
    Validation
    H2 Database
    JPA

## Data Flow
  ### Job
  
       1. private Long id;  @Id
       2. private String title;
       3. private String description;
       4. private String location;
       5. private Double jobSalary; @Min(value = 20000)
       6. private String companyEmail; @Email
       7. private String companyName;
       8. private String employerName;
       9. private JobType jobType;@Enumerated(EnumType.STRING)
  ### Controller
       1. @GetMapping("jobs")
       2. @GetMapping("job/{id}")
       3. @GetMapping("jobs/type/{type}")
       4. @GetMapping("jobs/salary/range/{salary}")
       5. @GetMapping("jobs/company/")
       6. @PostMapping("job")
       7. @PostMapping("jobs")
       8. @PutMapping("job/id/{id}/Salary/{salary}")
       9. @PutMapping("job/id/{id}/{loc}")
       10. @PutMapping("job/id/{id}/email")
       11. @PutMapping("jobs/salaryHike/jobType/{type}")
       12. @DeleteMapping("job/delete/id/{id}")
       13  @DeleteMapping("jobs/company/{cName}")
  ### Service
       1. getAllJobs() 
       2. getJobById(Long id) 
       3. postAJob(Job j)  
       4. postJobs(List<Job> j)
       5. updateSalaryById(Long id, Double salary)
       6. updateLocationById(Long id, String location)
       7. updateEmailById(Long id, String email)
       8. removeJobById(Long id)
       9. getAllSameTypeJobs(JobType type)
       10. getAllJobsInASalaryRange(Double salary)
       11. getAllJobsWithTheSameCompany(String cName) 
       12. removeAllJobsOfTheSameCompany(String cName)
       13. updateSalaryOfSimilarJobType(JobType type)

 
  

## Project Summary
  In this application we can  Create Read Update Delete a jobs from the different api that are in this application
