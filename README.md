## Article types

- [Abstract](https://bdougherty-wiley.github.io/article-types/types/bcb805fc-64c9-4790-9a39-ce421e655c37.json)
- [Announcement](https://bdougherty-wiley.github.io/article-types/types/ca436f9e-2e1e-487d-8e49-94d580e574b1.json)
- Career and Management
- Case Study
- Correction
- Correspondence
- Data Article
- Education
- Events
- Index
- Introduction
- Lecture
- Media Review
- Meeting Report
- Method and Protocol
- News
- Obituary
- Opinion
- Perspective
- Practice and Policy
- Profile
- Rapid Publication
- Research Article
- Retraction or Concern
- Review Article
- Short Communication
- Technical Note

 <script type="text/javascript">
    function setAccessedDate() {
      if (document.getElementById('accessed-on')) {
        var now = new Date();
        var months = ['Jan','Feb','Mar','Apr','May','Jun','Jul','Aug','Sep','Oct','Nov','Dec'];
        var formattedDate = now.getDate().padStart(2,'0')+" "+months[now.getMonth()]+" "+now.getFullYear();
        document.getElementById('accessed-on').textContent = " (accessed " + formattedDate + ")";
      }
    }
    function setModifiedDate() {
      if (document.getElementById('last-modified')) {
        fetch("https://api.github.com/repos/{{ site.github.owner_name }}/{{ site.github.repository_name }}/commits?path={{ page.path }}")
          .then((response) => {
            return response.json();
          })
          .then((commits) => {
            var modified = commits[0]['commit']['committer']['date'].slice(0,10);
            if(modified != "{{ page.date | date: "%Y-%m-%d" }}") {
              document.getElementById('last-modified').textContent = "Last Modified: " + modified;
            }
          });
      }
    }
  </script>
