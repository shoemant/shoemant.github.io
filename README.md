# shoemant.github.io


1. `[0 marks]` Links to your project repo AND website  
   Website Link: https://shoemant.github.io/  
   Link to Assigned Repository: https://github.com/CMPT-276-SPRING-2025/solo-mini-project-shoemant  
   Link to Website Repository: https://github.com/shoemant/shoemant.github.io  
3. `[0.5 marks]` Provide an overview of your website and all the elements that it includes  
  My website consists of 3 tabs: Home, Projects, Contact. We can navigate through the pages using the top navigation bar. On the Home page, we have a quick introduction of myself with a download button for my resume and hyperlinks to my GitHub page, LinkedIn, and Email. Scrolling down, we can see two of my featured projects with hyperlinks to their respective GitHub source code. It also includes an image of the project running with a short description along with the technologies attached. Under the projects tab, we can see all the projects I have on my GitHub. All of these projects have a hyperlink to their GitHub repository, a picture of the program, and a short description. Finally, we have a contact page with hyperlinks to  my resume, LinkedIn, GitHub, and email.
5. `[1 marks]` What is a favicon and why is it important for SEO?  
   A favicon is a small icon associated with a website, displayed in browser tabs, bookmarks, and sometimes search results. It enhances brand recognition, improves user experience, and adds credibility to a site. While not a direct SEO ranking factor, a favicon can improve click-through rates in search results and bookmarks, indirectly benefiting SEO by increasing user engagement and trust.
7. `[1 marks]` What are Github Pages? How do they differ from a regular webpage?  
  GitHub Pages is a free hosting service provided by GitHub that allows users to deploy static websites directly from a GitHub repository. It supports HTML, CSS, JavaScript, and Jekyll for automatic site generation. Unlike regular web hosting services, GitHub Pages is designed for developers, integrates seamlessly with version control, and primarily serves static content (i.e., no backend processing or databases). Regular web hosting, on the other hand, can support dynamic websites with server-side scripting, databases, and more complex functionalities.
9. `[1 marks]` What are Github Actions? Provide an example of a `.yml` file that you used in your lab and explain what it does, line by line in plain English.  

  GitHub Actions is a CI/CD (Continuous Integration/Continuous Deployment) tool that automates workflows directly within a GitHub repository. It allows developers to build, test, and deploy code automatically when specific events (such as pushes, pull requests, or scheduled tasks) occur.

```
name: TeleportPlus
version: 1.0
main: com.Sumant.TeleportPlus.TeleportPlus
author: Sumant
commands:
  sethome:
    description: Sets your home location.
  home:
    description: Teleports you to your home location.
```

This is a **Bukkit/Spigot plugin configuration file** that defines the plugin’s metadata, main class, and commands.  
```name: TeleportPlus``` → Defines the plugin name (TeleportPlus).  
```version: 1.0``` → Specifies the plugin version (1.0).  
```main: com.Sumant.TeleportPlus.TeleportPlus``` → Specifies the main class of the plugin (TeleportPlus). Located in the package com.Sumant.TeleportPlus This class must extend  JavaPlugin (from the Bukkit API).
```author: Sumant``` → Lists the plugin author (Sumant).  
```commands:``` → Defines the commands available in the plugin.  
```sethome:``` → Registers the command /sethome.  
```description:``` Sets your home location. → Describes /sethome.  
```home:``` → Registers the command /home.  
```description:``` Teleports you to your home location. → Describes /home.  


11. `[0.5 mark]` What technology stack did you use to develop this website? Why did you choose this stack?  
I developed this website using HTML and CSS, where HTML structures the content, and CSS styles and enhances its visual presentation. This stack was chosen for its simplicity, speed, and cross-browser compatibility, making it ideal for a static website. HTML provides a clean, semantic layout, while CSS allows for responsive design and customization. Together, they ensure fast loading times, easy maintenance, and a smooth user experience.

## Github Video + Questions `[7 marks]`
Watch the video below and answer the questions:
- [Git & GitHub Tutorial for Beginners #9 - Merging Branches (& conflicts)](https://youtu.be/XX-Kct0PfFc)
- [Git & GitHub Tutorial for Beginners #11 - Collaborating on GitHub](https://youtu.be/MnUd31TvBoU)
### Questions
1. `[2 marks]` In 3-4 sentences, explain what pull requests (PRs) are and their purpose.

A pull request (PR) is a feature in GitHub that allows developers to propose changes to a codebase before merging them into the main branch. PRs facilitate code review, enabling team members to discuss modifications, suggest improvements, and ensure code quality before integration. They help maintain a structured development workflow, prevent bugs, and allow for version control tracking. Once approved, the changes can be merged into the target branch.


3. `[1 marks (0.5 each)]` Describe what the green and red colours indicate when viewing `Files changed` on a pull request.  
   ![Github Red Green](github-red-green.png)

Green indicates added or modified lines of code in the proposed changes. Red represents deleted or replaced lines from the original file.
   
5. Suppose you have the following branches on github (`develop`, `test` and `production`) and you are currently on the `develop` branch.
   a. `[2 marks]` In your own words, describe what following git command does:
      - `git merge test`
      After running the git command above, you recieve the following error in your `README.md` file:
      ```shell
      Line 1: <<<<<<< HEAD
      Line 2: this is some content to mess with
      Line 3: content to append
      Line 4: =======
      Line 5: totally different content to merge later
      Line 6: >>>>>> test
      ```
      The command ```git merge test``` attempts to merge the test branch into the current branch (develop). If successful, it integrates the changes from test into develop, preserving the commit history. However, if there are conflicts (changes made to the same lines in both branches), Git will halt the merge and prompt the user to resolve them manually.
   
   b. `[1 mark]` Explain why this message has appeared and what it means.

The conflict message appears because both the develop and test branches have modified the same lines in README.md, but in different ways. Git is unable to automatically determine which changes should be kept, so it marks the conflicting section for manual resolution.

   c. `[1 mark]` Identify which line(s) of code belong to which branch (`develop` and `test`)

   Lines 2-3: belong to develop (HEAD).  
   Line 5: belongs to test.  
   To resolve the conflict, you must manually edit the file, keeping the desired changes, then run:  
   ``` git add README.md ```  
   ``` git commit -m "Resolved merge conflict between develop and test" ```
