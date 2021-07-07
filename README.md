<!DOCTYPE html>
<html lang="en">
<head>

    <meta charset="utf-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />

    <title>5 Git Workflows &amp; Branching Strategy to deliver better code</title>
    <meta name="HandheldFriendly" content="True" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <link rel="stylesheet" type="text/css" href="/blog/assets/built/screen.css?v=4bff170746" />

    <meta name="description" content="The right git workflow &amp; branching strategy can help you improve your development process. Here are 5 types of Git Workflows you can use within your team." />
    <link rel="icon" href="/blog/favicon.png" type="image/png" />
    <link rel="canonical" href="https://zepel.io/blog/5-git-workflows-to-improve-development/" />
    <meta name="referrer" content="no-referrer-when-downgrade" />
    <link rel="amphtml" href="https://zepel.io/blog/5-git-workflows-to-improve-development/amp/" />
    
    <meta property="og:site_name" content="The Zepel Blog" />
    <meta property="og:type" content="article" />
    <meta property="og:title" content="5 Git Workflows &amp; Branching Strategy to deliver better code" />
    <meta property="og:description" content="The right git workflow and branching strategy can help you improve your development process. Here are 5 types of Git Workflows you can use within your team." />
    <meta property="og:url" content="https://zepel.io/blog/5-git-workflows-to-improve-development/" />
    <meta property="og:image" content="https://zepel.io/blog/content/images/2020/05/git-workflow.png" />
    <meta property="article:published_time" content="2020-05-27T13:15:54.000Z" />
    <meta property="article:modified_time" content="2021-02-16T05:42:31.000Z" />
    <meta property="article:tag" content="Git" />
    <meta property="article:tag" content="Product Development" />
    
    <meta property="article:publisher" content="https://www.facebook.com/GetZepel" />
    <meta name="twitter:card" content="summary_large_image" />
    <meta name="twitter:title" content="5 Git Workflows &amp; Branching Strategy to deliver better code" />
    <meta name="twitter:description" content="The right git workflow and branching strategy can help you improve your development process. Here are 5 types of Git Workflows you can use within your team." />
    <meta name="twitter:url" content="https://zepel.io/blog/5-git-workflows-to-improve-development/" />
    <meta name="twitter:image" content="https://zepel.io/blog/content/images/2020/05/git-workflow.png" />
    <meta name="twitter:label1" content="Written by" />
    <meta name="twitter:data1" content="Vikash Koushik" />
    <meta name="twitter:label2" content="Filed under" />
    <meta name="twitter:data2" content="Git, Product Development" />
    <meta name="twitter:site" content="@GetZepel" />
    <meta name="twitter:creator" content="@svikashk" />
    <meta property="og:image:width" content="1125" />
    <meta property="og:image:height" content="657" />
    
    <script type="application/ld+json">
{
    "@context": "https://schema.org",
    "@type": "Article",
    "publisher": {
        "@type": "Organization",
        "name": "The Zepel Blog",
        "url": "https://zepel.io/blog/",
        "logo": {
            "@type": "ImageObject",
            "url": "https://zepel.io/blog/content/images/2020/06/zepel-logo-header-3.png"
        }
    },
    "author": {
        "@type": "Person",
        "name": "Vikash Koushik",
        "image": {
            "@type": "ImageObject",
            "url": "https://zepel.io/blog/content/images/2020/06/Vikash-Koushik-Sreenivasan-copy.jpg",
            "width": 600,
            "height": 800
        },
        "url": "https://zepel.io/blog/author/vikash/",
        "sameAs": [
            "https://zepel.io/",
            "https://twitter.com/svikashk"
        ]
    },
    "headline": "5 Git Workflows &amp; Branching Strategy to deliver better code",
    "url": "https://zepel.io/blog/5-git-workflows-to-improve-development/",
    "datePublished": "2020-05-27T13:15:54.000Z",
    "dateModified": "2021-02-16T05:42:31.000Z",
    "image": {
        "@type": "ImageObject",
        "url": "https://zepel.io/blog/content/images/2020/05/git-workflow.png",
        "width": 1125,
        "height": 657
    },
    "keywords": "Git, Product Development",
    "description": "The right git workflow and branching strategy can help you improve your development process. Here are 5 types of Git Workflows you can use within your team.",
    "mainEntityOfPage": {
        "@type": "WebPage",
        "@id": "https://zepel.io/blog/"
    }
}
    </script>

    <meta name="generator" content="Ghost 3.23" />
    <link rel="alternate" type="application/rss+xml" title="The Zepel Blog" href="https://zepel.io/blog/rss/" />
    <link rel="preconnect" href="https://ajax.googleapis.com" crossorigin="anonymous">
<link rel="preconnect" href="https://www.google-analytics.com" crossorigin="anonymous">
<script src="//platform-api.sharethis.com/js/sharethis.js#property=5b59798c4970c900111bb94d&product=sticky-share-buttons"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.2/js/bootstrap.min.js"></script>
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.2/css/bootstrap.min.css">

<style>
    .post-full-byline-meta h4 {
        font-size: 21px;
    }
    .post-full-content blockquote {
        border-left: 0px solid;
        color: #7171ea; 
        font-style: italic;
		display: block;
		margin: .5em 0;
		padding: 1em 0 1.5em;
		border: 0;
		font-size: 3.2rem;
		line-height: 1.35em;
		text-align: center;
    }
    .post-content a {
    	border-bottom: 2px solid #7171ea;
	}
    .post-content a:hover, .post-content a:focus {
    	color: #6457ae;
	}
    .post-full-content a {
    color: #7171ea;
    box-shadow: inset 0 0px 0 ;
    }
    .hbspt-form
    {
        max-width:800px;
        width:100%;
        margin:0 auto 50px;
        padding:20px;
        box-shadow: 0 1px 5px 3px rgba(46,50,52,0.1);
    }
        .hbspt-form h1 
    {
     line-height:30px;
    }
    .hubspot-link__container.sproket
    {
     display:none !important;  
    }
    .hubspot-link__container
    {display:none !important;
    }
    .triggerclick
    {
     color:#7171ea;
     border-color:#7171ea;
     padding:10px 20px;
        border:1px solid #7171ea;
     background-color:#ffffff;
        outline:none;
        transition:0.2s ease-in-out;
    }
       .triggerclick:hover
    {
     color:#ffffff;
     background-color:#7171ea;
     padding:10px 20px;
         outline:none;
    }
</style>

<!-- Global site tag (gtag.js) - Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=UA-112002143-1"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'UA-112002143-1');
</script>
<!-- End Global site tag (gtag.js) - Google Analytics -->
<!-- Begin Hellobar -->
<script src="https://my.hellobar.com/230bdc82e21aab9512eb71207130acb0c82048f2.js" type="text/javascript" charset="utf-8" async="async"> </script>
<!-- End Hellobar -->

</head>
<body class="post-template tag-git tag-product-development">

    <div class="site-wrapper">

        

<header class="site-header">
    <div class="outer site-nav-main">
    <div class="inner">
        <nav class="site-nav">
    <div class="site-nav-left-wrapper">
        <div class="site-nav-left">
                <a class="site-nav-logo" href="https://zepel.io/blog"><img src="/blog/content/images/2020/06/zepel-logo-header-3.png" alt="The Zepel Blog" /></a>
            <div class="site-nav-content hidden-xs">
                    <ul class="nav">
    <li class="nav-product"><a href="https://zepel.io/?utm_source=zepelblog&utm_medium=topnav">Product</a></li>
    <li class="nav-features"><a href="https://zepel.io/features/?utm_source=zepelblog&utm_medium=topnav">Features</a></li>
    <li class="nav-agile-library"><a href="https://zepel.io/agile/?utm_source=zepelblog&utm_medium=topnav">Agile Library</a></li>
    <li class="nav-pricing"><a href="https://zepel.io/pricing/?utm_source=zepelblog&utm_medium=topnav">Pricing</a></li>
</ul>

                    <span class="nav-post-title ">5 Git workflows and branching strategy you can use to improve your development process</span>
            </div>
        </div>
    </div>
    <div class="site-nav-right">
            <ul class="nav">
    <li class="nav-log-in"><a href="https://zepel.io/login/">Log in</a></li>
    <li class="nav-try-zepel-for-free"><a href="https://zepel.io/?utm_source=zepelblog&utm_medium=topnav">Try Zepel for Free</a></li>
</ul>


    </div>
</nav>
    </div>
</div></header>


<main id="site-main" class="site-main outer">
    <div class="inner">

        <article class="post-full post tag-git tag-product-development ">

            <header class="post-full-header">
        
                <section class="post-full-tags">
                  
                    May 27, 2020&nbsp; / &nbsp;  <a href="/blog/tag/git/">Git</a>
                </section>


                <h1 class="post-full-title zp-post-h1">5 Git workflows and branching strategy you can use to improve your development process</h1>
            </header>

            <figure class="post-full-image">
                <img
                    srcset="/blog/content/images/size/w300/2020/05/git-workflow.png 300w,
                            /blog/content/images/size/w600/2020/05/git-workflow.png 600w,
                            /blog/content/images/size/w1000/2020/05/git-workflow.png 1000w,
                            /blog/content/images/size/w2000/2020/05/git-workflow.png 2000w"
                    sizes="(max-width: 800px) 400px,
                        (max-width: 1170px) 1170px,
                            2000px"
                    src="/blog/content/images/size/w2000/2020/05/git-workflow.png"
                    alt="5 Git workflows and branching strategy you can use to improve your development process"
                />
            </figure>

            <section class="post-full-content">
                <div class="post-content">
                    <p>I haven't met a developer who looked at a conflict message and did not pull their hair strands with frustration.</p><p>Trying to resolve each merge conflict is one of those things that every developer hates. Especially if it hits you when you're gearing up for a production deploy!</p><p>This is where having the right Git workflow set up can do a world of good for your <a href="https://zepel.io/blog/simple-software-development-workflow/?utm_source=zepelblog&amp;utm_medium=text&amp;utm_campaign=git-workflow">development workflow</a>. </p><p>Of course, having the right git workflow will not solve all your problems. But it's a step in the right direction. After all, with every team working remotely, the need to build features together without having your codebase getting disrupted is critical.</p><p>How you set it up depends on the project you're working on, the release schedules your team has, the size of the team, and more!</p><p>In this article, we’ll walk you through 5 different git workflows, their benefits, their cons, and when you should use them. Let’s jump in!</p><h2 id="1-basic-git-workflow">1. Basic Git Workflow</h2><p></p><p>The most basic git workflow is the one where there is only one branch — the master branch. Developers commit directly into it and use it to deploy to the staging and production environment.</p><figure class="kg-card kg-image-card kg-card-hascaption"><img src="https://zepel.io/blog/content/images/2020/05/Basic-git-workflow-3.png" class="kg-image" alt="Basic Git Workflow"><figcaption>Basic Git Workflow with all commits getting added directly to master branch</figcaption></figure><p>This workflow isn’t usually recommended unless you’re working on a side project and you’re looking to get started quickly.</p><p>Since there is only one branch, there really is no process over here. This makes it effortless to get started with Git. However, some cons you need to keep in mind when using this workflow are:</p><ol><li>Collaborating on code will lead to multiple conflicts.</li><li>Chances of shipping buggy software to production is higher.</li><li>Maintaining clean code is harder.</li></ol><h2 id="2-git-feature-branch-workflow">2. Git Feature Branch Workflow</h2><p></p><p>The Git Feature Branch workflow becomes a must have when you have more than one developer working on the same codebase.</p><p>Imagine you have one developer who is working on a new feature. And another developer working on a second feature. Now, if both the developers work from the same branch and add commits to them, it would make the codebase a huge mess with plenty of conflicts.</p><figure class="kg-card kg-image-card kg-card-hascaption"><img src="https://zepel.io/blog/content/images/2020/05/Feature-Branch-git-workflow-4.png" class="kg-image" alt="Git feature branch workflow"><figcaption>Git workflow with feature branches</figcaption></figure><p>To avoid this, the two developers can create two separate branches from the master branch and work on their features individually. When they’re done with their feature, they can then merge their respective branch to the master branch, and deploy without having to wait for the second feature to be completed.</p><p>The Pros of using this workflow is, the git feature branch workflow allows you to collaborate on code without having to worry about code conflicts.</p><h2 id="3-git-feature-workflow-with-develop-branch">3. Git Feature Workflow with Develop Branch</h2><p></p><p>This workflow is one of the more popular workflows among developer teams. It’s similar to the Git Feature Branch workflow with a develop branch that is added in parallel to the master branch.</p><p>In this workflow, the master branch always reflects a production-ready state. Whenever the team wants to deploy to production they deploy it from the master branch.</p><p>The develop branch reflects the state with the latest development changes for the next release. Developers create branches from the develop branch and work on new features. Once the feature is ready, it is tested, merged with develop branch, tested with the develop branch’s code in case there was a prior merge, and then merged with master.</p><figure class="kg-card kg-image-card kg-card-hascaption"><img src="https://zepel.io/blog/content/images/2020/05/feature-branch-with-develop-git-workflow-2.png" class="kg-image" alt="Git workflow with feature and develop branches"><figcaption>Git workflow with feature and develop branches</figcaption></figure><p>The advantage of this workflow is, it allows teams to consistently merge new features, test them in staging, and deploy to production. While maintaining code is easier, it can get a little tiresome for some teams since it can feel like going through a tedious process.</p><h2 id="4-gitflow-workflow">4. Gitflow Workflow</h2><p></p><p>The gitflow workflow is very similar to the previous workflow we discussed combined with two other branches — the release branch and the hot-fix branch.</p><h3 id="the-hot-fix-branch">The hot-fix branch</h3><p></p><p>The hot-fix branch is the only branch that is created from the master branch and directly merged to the master branch instead of the develop branch. It is used only when you have to quickly patch a production issue. An advantage of this branch is, it allows you to quickly deploy a production issue without disrupting others’ workflow or without having to wait for the next release cycle.</p><p>Once the fix is merged into the master branch and deployed, it should be merged into both develop and the current release branch. This is done to ensure that anyone who forks off develop to create a new feature branch has the latest code.</p><h3 id="the-release-branch">The release branch</h3><p></p><p>The release branch is forked off of develop branch after the develop branch has all the features planned for the release merged into it successfully.</p><p>No code related to new features is added into the release branch. Only code that relates the release is added to the release branch. For example, documentation, bug fixes, and other tasks related to this release are added to this branch.</p><p>Once this branch is merged with master and deployed to production, it’s also merged back into the develop branch, so that when a new feature is forked off of develop, it has the latest code.</p><figure class="kg-card kg-image-card kg-card-hascaption"><img src="https://zepel.io/blog/content/images/2020/05/GitFlow-git-workflow-2.png" class="kg-image" alt="Gitflow workflow"><figcaption>Gitflow workflow with hotfix and release branches</figcaption></figure><p>This workflow was first published and made popular by <a href="http://nvie.com/posts/a-successful-git-branching-model/">Vincent Driessen</a> and since then it has been widely used by organizations that have a scheduled release cycle.</p><p>Since the git-flow is a wrapper around Git, you can install git-flow in your current repository. It's a straightforward process and it doesn't change anything in your repository other than creating branches for you. </p><p>To install on a Mac machine, execute <code>brew install git-flow</code> in your terminal.</p><p>To install on a Windows machine, you'll need to <a href="https://git-scm.com/download/win">download and install the git-flow</a>. After the installation is done, run the following <a href="https://zepel.io/blog/13-git-commands/?utm_source=zepelblog&amp;utm_medium=text&amp;utm_campaign=git-workflow">Git Command</a> <code>git flow init</code> to use it in your project.</p><h2 id="5-git-fork-workflow">5. Git Fork Workflow</h2><p></p><p>The Fork workflow is popular among teams who use open-source software.</p><p>The flow usually looks like this:</p><ol><li>The developer forks the open-source software’s official repository. A copy of this repository is created in their account.</li><li>The developer then clones the repository from their account to their local system.</li><li>A remote path for the official repository is added to the repository that is cloned to the local system.</li><li>The developer creates a new feature branch is created in their local system, makes changes, and commits them.</li><li>These changes along with the branch are pushed to the developer’s copy of the repository on their account.</li><li>A pull request from the branch is opened to the official repository.</li><li>The official repository’s manager checks the changes and approves the changes to get merged into the official repository.</li></ol><hr><h2 id="automating-your-git-workflows-and-branching-strategy-for-better-productivity">Automating your Git Workflows and Branching Strategy for better productivity</h2><p></p><p>One of the things that developers have to constantly juggle with is updating their project management tool to keep their teammates updated. That’s why, at Zepel, our developers automate their workflow, so they can spend more of their time building the software.</p><p>Here’s how we automate our git workflow to keep everyone in sync:</p><figure class="kg-card kg-image-card kg-card-hascaption"><img src="https://zepel.io/blog/content/images/2020/04/zepel-git-developer-workflow.png" class="kg-image" alt="Developer Workflow with GitHub, Zepel, and Slack Integrations"><figcaption>A simple flowchart of how developer workflow is automated with GitHub, Zepel, and Slack</figcaption></figure><p>While Zepel integrates deeply with <a href="https://zepel.io/integrations/github/?utm_source=zepelblog&amp;utm_medium=text&amp;utm_campaign=git-workflow">GitHub</a>, <a href="https://zepel.io/integrations/bitbucket/?utm_source=zepelblog&amp;utm_medium=text&amp;utm_campaign=git-workflow">Bitbucket</a>, and <a href="https://zepel.io/integrations/gitlab/?utm_source=zepelblog&amp;utm_medium=text&amp;utm_campaign=git-workflow">GitLab</a>, we use GitHub internally. So, once we’ve integrated GitHub with Zepel, our development team sets up the git workflow automation within Zepel. Here’s how it looks today:</p><figure class="kg-card kg-image-card kg-card-hascaption"><img src="https://zepel.io/blog/content/images/2020/01/zepel-git-workflow-automation.png" class="kg-image" alt="Git workflow automation"><figcaption>Automating Zepel to update statuses based on Git workflow.</figcaption></figure><p>As developers continue to make progress, our team automatically gets a <a href="https://zepel.io/integrations/slack/?utm_source=zepelblog&amp;utm_medium=text&amp;utm_campaign=git-workflow">Slack</a> notification and their changes are recorded within the user story.</p><figure class="kg-card kg-image-card kg-card-hascaption"><img src="https://zepel.io/blog/content/images/2020/05/image.png" class="kg-image" alt="Git workflow updates to user story in real-time"><figcaption>Real-time updates on every commit, pull request, and branch changes.</figcaption></figure><hr><h2 id="your-own-workflow-and-git-branching-strategy-">Your own workflow and Git branching strategy!</h2><p></p><p>The git workflows I’ve shown in this article are examples of some of the popular and best working workflows for the development team. Some teams create a branch for Staging and it works perfectly for them.</p><p>If you use other workflows that work well for you, tweet to us <a href="https://twitter.com/@getzepel">@getzepel</a>. We’d love to showcase them!</p><!--kg-card-begin: html--><a href="https://zepel.io/?open_modal=true&utm_source=zepelblog&utm_medium=bottom-cta&utm_campaign=git-workflow" class="cta-image"><img src="https://zepel.io/blog/content/images/2020/03/sprint-planning-template-cta.png" alt="development workflow cta button"/></a><!--kg-card-end: html--><hr><h2 id="helpful-articles">Helpful Articles</h2><p></p><figure class="kg-card kg-bookmark-card"><a class="kg-bookmark-container" href="https://zepel.io/blog/how-to-create-a-new-branch-in-github/"><div class="kg-bookmark-content"><div class="kg-bookmark-title">Working with Branches: How to Create a Branch in GitHub?</div><div class="kg-bookmark-description">Step-by-step guide on how to create a new branch in GitHub using their website, desktop app, and terminal commands.</div><div class="kg-bookmark-metadata"><img class="kg-bookmark-icon" src="https://zepel.io/blog/favicon.png"><span class="kg-bookmark-author">Vikash Koushik</span><span class="kg-bookmark-publisher">The Zepel Blog</span></div></div><div class="kg-bookmark-thumbnail"><img src="https://zepel.io/blog/content/images/2020/10/creating-branch-in-github.png"></div></a></figure><figure class="kg-card kg-bookmark-card"><a class="kg-bookmark-container" href="https://zepel.io/blog/how-to-commit-to-github/"><div class="kg-bookmark-content"><div class="kg-bookmark-title">Git Commit: How to Commit Code Changes to GitHub?</div><div class="kg-bookmark-description">Imagine your hours’ worth of code disappearing in seconds. 😱 Stop this nightmare from becoming reality, commit your code to GitHub. Here’s how you can do it.</div><div class="kg-bookmark-metadata"><img class="kg-bookmark-icon" src="https://zepel.io/blog/favicon.png"><span class="kg-bookmark-author">Ranjali Roy</span><span class="kg-bookmark-publisher">The Zepel Blog</span></div></div><div class="kg-bookmark-thumbnail"><img src="https://zepel.io/blog/content/images/2020/11/git-commit.png"></div></a></figure><figure class="kg-card kg-bookmark-card"><a class="kg-bookmark-container" href="https://zepel.io/blog/create-pull-requests-in-github/"><div class="kg-bookmark-content"><div class="kg-bookmark-title">How to Create Pull Requests on GitHub</div><div class="kg-bookmark-description">Learn how to create pull requests on GitHub and effortlessly collaborate on the same code base. Read the step-by-step guide.</div><div class="kg-bookmark-metadata"><img class="kg-bookmark-icon" src="https://zepel.io/blog/favicon.png"><span class="kg-bookmark-author">Ranjali Roy</span><span class="kg-bookmark-publisher">The Zepel Blog</span></div></div><div class="kg-bookmark-thumbnail"><img src="https://zepel.io/blog/content/images/2020/12/github-create-pull-request.png"></div></a></figure>
                </div>
            </section>



        </article>
          <div class="post-full-byline">

                    <section class="post-full-byline-content">

                        <ul class="author-list">
                            <li class="author-list-item">

                                <div class="author-card">
                                    <img class="author-profile-image" src="/blog/content/images/size/w100/2020/06/Vikash-Koushik-Sreenivasan-copy.jpg" alt="Vikash Koushik" />
                                    <div class="author-info">
                                        <div class="bio">
                                            <h2>Vikash Koushik</h2>
                                            <p>Talking to customers and telling their stories at Zepel</p>
                                            <p><a href="/blog/author/vikash/">More posts</a> by Vikash Koushik.</p>
                                        </div>
                                    </div>
                                </div>

                                <a href="/blog/author/vikash/" class="author-avatar">
                                    <img class="author-profile-image" src="/blog/content/images/size/w100/2020/06/Vikash-Koushik-Sreenivasan-copy.jpg" alt="Vikash Koushik" />
                                </a>

                            </li>
                        </ul>
                        <section class="post-full-byline-meta">
                               <div class="bio">
                                            <h4>Vikash Koushik</h4>
                                            <p>Talking to customers and telling their stories at Zepel</p>
                                        </div>
                        </section>      

                    </section>


                </div>
    </div>
</main>

<aside class="read-next outer">
    <div class="inner">
        <div class="read-next-feed">
                <article class="read-next-card">
                    <header class="read-next-card-header">
                        <h3><span>More in</span> <a href="/blog/tag/git/">Git</a></h3>
                    </header>
                    <div class="read-next-card-content">
                        <ul>
                            <li>
                                <h4><a href="/blog/ways-to-improve-developer-productivity/">7 ways to improve developer productivity without getting drained</a></h4>
                                <div class="read-next-card-meta">
                                    <p><time datetime="2021-03-19">19 Mar 2021</time> –
                                        6 min read</p>
                                </div>
                            </li>
                            <li>
                                <h4><a href="/blog/simple-software-development-workflow/">An improved software development workflow to build better products and features</a></h4>
                                <div class="read-next-card-meta">
                                    <p><time datetime="2021-02-18">18 Feb 2021</time> –
                                        9 min read</p>
                                </div>
                            </li>
                            <li>
                                <h4><a href="/blog/how-to-merge-branches-in-github/">How to Merge Branches and Pull Requests in GitHub</a></h4>
                                <div class="read-next-card-meta">
                                    <p><time datetime="2021-01-11">11 Jan 2021</time> –
                                        6 min read</p>
                                </div>
                            </li>
                        </ul>
                    </div>
                    <footer class="read-next-card-footer">
                        <a href="/blog/tag/git/">See all 7 posts
                            →</a>
                    </footer>
                </article>

                <article class="post-card post tag-agile tag-project-management ">

    <a class="post-card-image-link" href="/blog/scrum-tools/">
        <img class="post-card-image"
            srcset="/blog/content/images/size/w300/2020/01/scrum-software-tools.png 300w,
                    /blog/content/images/size/w600/2020/01/scrum-software-tools.png 600w,
                    /blog/content/images/size/w1000/2020/01/scrum-software-tools.png 1000w,
                    /blog/content/images/size/w2000/2020/01/scrum-software-tools.png 2000w"
            sizes="(max-width: 1000px) 400px, 700px"
            loading="lazy"
            src="/blog/content/images/size/w600/2020/01/scrum-software-tools.png"
            alt="9 Top Scrum Software Tools in 2021"
        />
    </a>

    <div class="post-card-content">

        <a class="post-card-content-link" href="/blog/scrum-tools/">

            <header class="post-card-header">
                    <div class="post-card-primary-tag">Agile</div>
                <h2 class="post-card-title">9 Top Scrum Software Tools in 2021</h2>
            </header>

            <section class="post-card-excerpt" >
                    <p>Compare the top 9 scrum tools of 2021 for agile project management. Contains detail review, top features, and more.</p>
            </section>

        </a>

        <footer class="post-card-meta">
            <ul class="author-list">
                <li class="author-list-item">
            
                    <div class="author-name-tooltip">
                        Vikash Koushik
                    </div>
            
                    <a href="/blog/author/vikash/" class="static-avatar">
                        <img class="author-profile-image" src="/blog/content/images/size/w100/2020/06/Vikash-Koushik-Sreenivasan-copy.jpg" alt="Vikash Koushik" />
                    </a>
                </li>
            </ul>
            <div class="post-card-byline-content">
                <span><a href="/blog/author/vikash/">Vikash Koushik</a></span>
                <span class="post-card-byline-date"><time datetime="2020-06-24">24 Jun 2020</time> <span class="bull">&bull;</span> 9 min read</span>
            </div>
        </footer>

    </div>

</article>

                <article class="post-card post tag-product ">

    <a class="post-card-image-link" href="/blog/introducing-aggregate-estimates-multiple-feature-creation-progress-update/">
        <img class="post-card-image"
            srcset="/blog/content/images/size/w300/2020/05/aggregate-estimation.jpeg 300w,
                    /blog/content/images/size/w600/2020/05/aggregate-estimation.jpeg 600w,
                    /blog/content/images/size/w1000/2020/05/aggregate-estimation.jpeg 1000w,
                    /blog/content/images/size/w2000/2020/05/aggregate-estimation.jpeg 2000w"
            sizes="(max-width: 1000px) 400px, 700px"
            loading="lazy"
            src="/blog/content/images/size/w600/2020/05/aggregate-estimation.jpeg"
            alt="Introducing Aggregated Soft Estimation, Multiple Feature Creation, and Improved Feature Progress"
        />
    </a>

    <div class="post-card-content">

        <a class="post-card-content-link" href="/blog/introducing-aggregate-estimates-multiple-feature-creation-progress-update/">

            <header class="post-card-header">
                    <div class="post-card-primary-tag">Product</div>
                <h2 class="post-card-title">Introducing Aggregated Soft Estimation, Multiple Feature Creation, and Improved Feature Progress</h2>
            </header>

            <section class="post-card-excerpt" >
                    <p>Breaking user stories down to actionable subtasks and estimating them isn’t just a best</p>
            </section>

        </a>

        <footer class="post-card-meta">
            <ul class="author-list">
                <li class="author-list-item">
            
                    <div class="author-name-tooltip">
                        Vikash Koushik
                    </div>
            
                    <a href="/blog/author/vikash/" class="static-avatar">
                        <img class="author-profile-image" src="/blog/content/images/size/w100/2020/06/Vikash-Koushik-Sreenivasan-copy.jpg" alt="Vikash Koushik" />
                    </a>
                </li>
            </ul>
            <div class="post-card-byline-content">
                <span><a href="/blog/author/vikash/">Vikash Koushik</a></span>
                <span class="post-card-byline-date"><time datetime="2020-05-21">21 May 2020</time> <span class="bull">&bull;</span> 3 min read</span>
            </div>
        </footer>

    </div>

</article>
        </div>
    </div>
</aside>




<footer class="site-footer outer hidden-sm hidden-xs" >
            <div class="site-footer-content inner">
                <div class="row container site-footer-links">
                        <div class="col-lg-1 col-md-1 text-center">
           <a href="https://zepel.io">
        <img src="https://zepel.io/website-assets/zepel-logo-short-78cdb993764c80b2a50ef36061f73fadde6cbfb0739d1e58ff6e30ca5b03cda3.svg" style="margin-top: 20px;" alt="zepel logo">
          </a>
      </div>
        <div class="col-lg-11 col-md-11">
                  <div class="col-md-3 col-xs-12 col-sm-6">
                      <div class="zp-ft-wrapper">
                      <h3>Product</h3>
                    <ul class="footer-links">
                       <li><a href="https://zepel.io/?ref=blogfooter">Home</a></li>
              <li><a href="https://zepel.io/pricing/?ref=blogfooter">Pricing</a></li>
             <li><a href="https://zepel.io/product/streams?ref=blogfooter">Streams</a></li>
             <li><a href="https://zepel.io/product/squads?ref=blogfooter">Squads</a></li>
              <li><a href="https://zepel.io/integrations/?ref=blogfooter">Integrations</a></li>
                    </ul>  

                    <h3>Resources</h3>
                <ul class="footer-links">
                <li><a href="https://zepel.io/agile/agile-software-development/?ref=blogfooter">Agile Library</a></li>
              <li><a href="https://zepel.io/agile/scrum/?ref=blogfooter">Scrum Guide</a></li>
              <li><a href="https://zepel.io/agile/kanban/?ref=blogfooter">Kanban Guide</a></li>
                <li><a href="https://zepel.io/agile/reports/?ref=blogfooter">Agile Reports</a></li>
             
                    </ul> 
                    </div>
                  </div> 
                   <div class="col-md-3 col-xs-12 col-sm-6">
                       <div class="zp-ft-wrapper">
                      <h3>Top Features</h3>
                    <ul class="footer-links">
                       <li><a href="https://zepel.io/features/plan-features/?ref=blogfooter">Plan Features</a></li> 
                        <li><a href="https://zepel.io/features/kanban-board/?ref=blogfooter">Kanban Board</a></li> 
                        <li><a href="https://zepel.io/features/scrum-board/?ref=blogfooter">Scrum Board</a></li>
                        <li><a href="https://zepel.io/features/sprints/?ref=blogfooter">Sprints</a></li>
                      <li><a href="https://zepel.io/feature-tracking/?ref=blogfooter">Track Features</a></li>
                      <li><a href="https://zepel.io/features/reports/?ref=blogfooter">Reports</a></li>
                      <li><a href="https://zepel.io/features/?ref=blogfooter">Explore All Features</a></li>

                    </ul>  
                    </div>
                  </div> 
                       <div class="col-md-3 col-xs-12 col-sm-6">
                                  <div class="zp-ft-wrapper">
                      <h3>Solutions</h3>
                    <ul class="footer-links">
                       <li><a href="https://zepel.io/solutions/product-development/?ref=blogfooter">Product Development</a></li>
            <li><a href="https://zepel.io/solutions/scrum/?ref=blogfooter">Scrum Tool</a></li>
            <li><a href="https://zepel.io/kanban-software/?ref=blogfooter">Kanban Software</a></li>
            <li><a href="https://zepel.io/solutions/developers/?ref=blogfooter">Developers</a></li>
                    </ul>  
                    </div>
                  </div> 
                       <div class="col-md-3 col-xs-12 col-sm-6">
                                  <div class="zp-ft-wrapper">
                      <h3>Compare</h3>
                    <ul class="footer-links">
                     <li><a href="https://zepel.io/compare/jira-alternative/?ref=blogfooter">JIRA Alternative</a></li>
            <li><a href="https://zepel.io/compare/asana-alternative/?ref=blogfooter">Asana Alternative</a></li>
            <li><a href="https://zepel.io/compare/trello-alternative/?ref=blogfooter">Trello Alternative</a></li>
                    </ul>  
                      <h3>Company</h3>
                    <ul class="footer-links">
                     <li><a href="https://zepel.io/privacy/?ref=blogfooter">Privacy</a></li>
            <li><a href="https://zepel.io/terms/?ref=blogfooter">Terms</a></li>
                    </ul>  
                    <div class="social-flex-container">
              <a href="https://www.facebook.com/GetZepel" rel="noopener" target="_blank"><img data-src="https://zepel.io/website-assets/facebook-3eeefda39f7081c1f42198aa8c07618d55426f1ea165aba094299052ae0a7c08.svg" alt="Zepel on Facebook" src="https://zepel.io/website-assets/facebook-3eeefda39f7081c1f42198aa8c07618d55426f1ea165aba094299052ae0a7c08.svg"></a>
              <a href="https://twitter.com/getzepel" rel="noopener" target="_blank"><img data-src="https://zepel.io/website-assets/twitter-c30ccd825488112b0dba1d46f9763a7c39e3848b574b7d8616deaac2fc9e0a69.svg" alt="Zepel on Twitter" src="https://zepel.io/website-assets/twitter-c30ccd825488112b0dba1d46f9763a7c39e3848b574b7d8616deaac2fc9e0a69.svg"></a>
              <a href="https://www.linkedin.com/company/zepel-io" rel="noopener" target="_blank"><img data-src="https://zepel.io/website-assets/linkedin-770026eaea453ccddcd6eb31b2909b4d0f1fb46584eb3d5adc1a3b4067701293.svg" alt="Zepel on LinkedIn" src="https://zepel.io/website-assets/linkedin-770026eaea453ccddcd6eb31b2909b4d0f1fb46584eb3d5adc1a3b4067701293.svg"></a>
            </div>
                  </div> 
                  </div>
                  </div>
                  </div>
            </div>
        </footer>
        <footer class="visible-sm visible-xs zp-footer-mobile">
  <div class="zp-mob-accordion">Product <span class="zp-menu-right"></span></div>
  <div class="zp-mob-panel">
      <div class="features-list-wrapper">
          <ul>
            <li><a href="https://zepel.io/?ref=blogfooter">Home</a></li>
              <li><a href="https://zepel.io/pricing/?ref=blogfooter">Pricing</a></li>
             <li><a href="https://zepel.io/product/streams?ref=blogfooter">Streams</a></li>
             <li><a href="https://zepel.io/product/squads?ref=blogfooter">Squads</a></li>
              <li><a href="https://zepel.io/integrations/?ref=blogfooter">Integrations</a></li>          
          </ul>
        </div>
  </div>
  <div class="zp-mob-accordion">Top Features <span class="zp-menu-right"></span></div>
  <div class="zp-mob-panel">
      <div class="features-list-wrapper">
          <ul>
                   <li><a href="https://zepel.io/features/plan-features/?ref=blogfooter">Plan Features</a></li> 
                        <li><a href="https://zepel.io/features/kanban-board/?ref=blogfooter">Kanban Board</a></li> 
                        <li><a href="https://zepel.io/features/scrum-board/?ref=blogfooter">Scrum Board</a></li>
                        <li><a href="https://zepel.io/features/sprints/?ref=blogfooter">Sprints</a></li>
                      <li><a href="https://zepel.io/feature-tracking/?ref=blogfooter">Track Features</a></li>
                      <li><a href="https://zepel.io/features/reports/?ref=blogfooter">Reports</a></li>
                      <li><a href="https://zepel.io/features/?ref=blogfooter">Explore All Features</a></li>
          </ul>
        </div>
  </div>

  <div class="zp-mob-accordion">Solutions <span class="zp-menu-right"></span></div>
  <div class="zp-mob-panel">
      <ul class="solutions">
     <li><a href="https://zepel.io/solutions/product-development/?ref=blogfooter">Product Development</a></li>
            <li><a href="https://zepel.io/solutions/scrum/?ref=blogfooter">Scrum Tool</a></li>
            <li><a href="https://zepel.io/kanban-software/?ref=blogfooter">Kanban Software</a></li>
            <li><a href="https://zepel.io/solutions/developers/?ref=blogfooter">Developers</a></li>
        </ul>
</div>
<div class="zp-mob-accordion">Resources <span class="zp-menu-right"></span></div>
<div class="zp-mob-panel">
  <ul class="resources">
                  <li><a href="https://zepel.io/agile/agile-software-development/?ref=blogfooter">Agile Library</a></li>
              <li><a href="https://zepel.io/agile/scrum/?ref=blogfooter">Scrum Guide</a></li>
              <li><a href="https://zepel.io/agile/kanban/?ref=blogfooter">Kanban Guide</a></li>
                <li><a href="https://zepel.io/agile/reports/?ref=blogfooter">Agile Reports</a></li>
    </ul>
</div>
<div class="zp-mob-accordion">Compare <span class="zp-menu-right"></span></div>
<div class="zp-mob-panel">
    <ul class="solutions">
                     <li><a href="https://zepel.io/compare/jira-alternative/?ref=blogfooter">JIRA Alternative</a></li>
            <li><a href="https://zepel.io/compare/asana-alternative/?ref=blogfooter">Asana Alternative</a></li>
            <li><a href="https://zepel.io/compare/trello-alternative/?ref=blogfooter">Trello Alternative</a></li>
      </ul>
</div>
<div class="zp-mob-accordion">Company <span class="zp-menu-right"></span></div>
<div class="zp-mob-panel">
  <ul class="resources">
                     <li><a href="https://zepel.io/privacy/?ref=blogfooter">Privacy</a></li>
            <li><a href="https://zepel.io/terms/?ref=blogfooter">Terms</a></li>
    </ul>
</div>


</footer>

    </div>


    <script
        src="https://code.jquery.com/jquery-3.4.1.min.js"
        integrity="sha256-CSXorXvZcTkaix6Yvo6HppcZGetbYMGWSFlBw8HfCJo="
        crossorigin="anonymous">
    </script>
    <script src="/blog/assets/built/casper.js?v=4bff170746"></script>

    <script>
        // Parse the URL parameter
        function getParameterByName(name, url) {
            if (!url) url = window.location.href;
            name = name.replace(/[\[\]]/g, "\\$&");
            var regex = new RegExp("[?&]" + name + "(=([^&#]*)|&|#|$)"),
                results = regex.exec(url);
            if (!results) return null;
            if (!results[2]) return '';
            return decodeURIComponent(results[2].replace(/\+/g, " "));
        }

        // Give the parameter a variable name
        var action = getParameterByName('action');

        $(document).ready(function () {
            if (action == 'subscribe') {
                $('body').addClass("subscribe-success");
            }

            $('.subscribe-success-message .subscribe-close').click(function () {
                $('.subscribe-success-message').addClass('close');
            });

            // Reset form on opening subscrion overlay
            $('.subscribe-button').click(function() {
                $('.subscribe-overlay form').removeClass();
                $('.subscribe-email').val('');
            });
        });
         $(window).scroll(function(){

        if( $(this).scrollTop() > 50)
        {
	$('.site-nav-main').addClass('nav-scrolled');
    $('.nav-try-zepel-for-free a').css({"background-color": "#7171eA", "color":"#ffffff"});
    
        }
        else
        {
           $('.site-nav-main').removeClass('nav-scrolled'); 
         $('.nav-try-zepel-for-free a').css({"background-color": "#7171eA", "color":"#ffffff"});
        }
});
    </script>

    <script>
    $(document).ready(function () {
        // FitVids - start
        var $postContent = $(".post-full-content");
        $postContent.fitVids();
        // FitVids - end

        // Replace nav with title on scroll - start
        Casper.stickyNavTitle({
            navSelector: '.site-nav-main',
            titleSelector: '.post-full-title',
           
        });
        // Replace nav with title on scroll - end

        // Hover on avatar
        var hoverTimeout;
        $('.author-list-item').hover(function () {
            var $this = $(this);

            clearTimeout(hoverTimeout);

            $('.author-card').removeClass('hovered');
            $(this).children('.author-card').addClass('hovered');

        }, function () {
            var $this = $(this);

            hoverTimeout = setTimeout(function () {
                $this.children('.author-card').removeClass('hovered');
            }, 800);
        });
    });
</script>


    <script>
    var acc = document.getElementsByClassName("zp-mob-accordion");
var panel = document.getElementsByClassName('zp-mob-panel');

for (var i = 0; i < acc.length; i++) {
    acc[i].onclick = function() {
    	var setClasses = !this.classList.contains('active');
        setClass(acc, 'active', 'remove');
        setClass(panel, 'show', 'remove');
        
       	if (setClasses) {
            this.classList.toggle("active");
            this.nextElementSibling.classList.toggle("show");
        }
    }
}

function setClass(els, className, fnName) {
    for (var i = 0; i < els.length; i++) {
        els[i].classList[fnName](className);
    }
}
    

    
 
</script>

</body>
</html>



# git-learning-

##git commands##


**etting & Creating Projects**

Command	Description


git init	Initialize a local Git repository
git clone ssh://git@github.com/[username]/[repository-name].git	
Create a local copy of a remote repository

Command	Description


**git status	Check status**

git add [file-name.txt]	Add a file to the staging area


git add -A	Add all new and changed files to the staging area


git commit -m "[commit message]"	Commit changes


git rm -r [file-name.txt]	Remove a file (or folder)



**Branching & Merging**


Command	Description
git branch	List branches (the asterisk denotes the current branch)


git branch -a	List all branches (local and remote)


git branch [branch name]	Create a new branch


git branch -d [branch name]	Delete a branch


git push origin --delete [branch name]	Delete a remote branch


git checkout -b [branch name]	Create a new branch and switch to it


git checkout -b [branch name] origin/[branch name]	Clone a remote branch and switch to it


git branch -m [old branch name] [new branch name]	Rename a local branch


git checkout [branch name]	Switch to a branch


git checkout -	Switch to the branch last checked out


git checkout -- [file-name.txt]	Discard changes to a file


git merge [branch name]	Merge a branch into the active branch


git merge [source branch] [target branch]	Merge a branch into a target branch


git stash	Stash changes in a dirty working directory


git stash clear	Remove all stashed entries



**Sharing & Updating Projects**


Command	Description


git push origin [branch name]	Push a branch to your remote repository


git push -u origin [branch name]	Push changes to remote repository (and remember the branch)


git push	Push changes to remote repository (remembered branch)


git push origin --delete [branch name]	Delete a remote branch


git pull	Update local repository to the newest commit


git pull origin [branch name]	Pull changes from remote repository


git remote add origin ssh://git@github.com/[username]/[repository-name].git	Add a remote repository


git remote set-url origin ssh://git@github.com/[username]/[repository-name].git	Set a repository's origin branch to SSH



**Inspection & Comparison**


Command	Description

git log	View changes


git log --summary	View changes (detailed)


git log --oneline	View changes (briefly)


git diff [source branch] [target branch]	Preview changes before merging
