---
layout: default
title: Blogs
permalink: /blog/
---

<h1>Blog Posts</h1>
<div class="blog-cards">
  {% for post in site.posts %}
    <div class="blog-card">
      <img src="{{ post.image | relative_url }}" alt="{{ post.title }}">
      <div class="blog-card-content">
        <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
        <p>{{ post.excerpt }}</p>
        <small>Published on {{ post.date | date: "%B %d, %Y" }}</small>
      </div>
    </div>
  {% endfor %}
</div>

<style>
  .blog-cards {
    display: flex;
    flex-direction: column;
    gap: 20px;
  }
  .blog-card {
    display: flex;
    flex-direction: row;
    border: 1px solid #ddd;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    background-color: rgba(0, 0, 0, 0.46);
    width: 100%;
  }
  .blog-card img {
    width: 200px;
    height: 100%;
    object-fit: cover;
  }
  .blog-card-content {
    padding: 15px;
    display: flex;
    flex-direction: column;
    flex: 1;
  }
  .blog-card-content h2 {
    margin: 0 0 10px;
    font-size: 1.5em;
  }
  .blog-card-content p {
    margin: 0 0 10px;
    color: #555;
  }
  .blog-card-content small {
    color: #999;
  }
</style>