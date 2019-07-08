# JobAssist

This App helps you find the skills in demand based on your inputs. 

1. User will register using email or LinkedIn. 
2. A profile will be created. User can edit the profile and fill phone number, defautl location and other parameters
1. search terms: User will enter a job title or a skill (say Python software engineer, PHP Web Developer etc.)
2. locations: User optionally enters preferred locations  for jobs. If this is not entered, we will use the default location specified in the profile



The app will fetch you a list of jobs (by aggregating searches on various job search engines, based on your location - for example, if the user is applying jobs from India, it will look at the Indian jobs that match the skills and location preferences - for example Python Web Application jobs in Chennai/Bangalore)
The app will display a list of jobs and corresponding skills for each job. If the user profile contains a certain set of skills the best matched jobs are displayed.


How the system works. 
1. JA will start with a predefined list of job sites. Currently we will use indeed, dice, glassdoor, stackoverflow, hotjobs, monster (or popular job portals)
2. JA will use RPA to search multiple sites and scrape the first 20 jobs from each
3. JA will aggregate the job list, remove duplicates if any and create a list-1
4. JA will extract skills from each job in list-1 and match it with skills from users profile
5. JA will order the jobs by relevance and display them along with a list of skills for each
6. JA will extract the companies from the job list and classify them as recruiter or original company. Each job will be tagged with this attribute. 
7. JA will extract salary information if available
8. JA will extract the type of job (full-time, part-time, contract) and tag the job with the information
9. JA will use the company names to go to the company job pages and store them in the database (an RPA process will check this page daily/weekly for new jobs)
10. JA will scrape the company information page to get the list of locations 
11. JA will scrape the company website to build a company profile
12. JA will scrape the site to find links to social media - twitter, facebook, linkedin, blogs and update the company information in the database and list them in the company profile
