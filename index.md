---
layout: default
title: SCAM
---

<p class="egg">&lt;!DOCTYPE html&gt; &lt;!-- oh, you read the source? --&gt;</p>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SCAM</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --bg: #101010;
            --fg: #d8d8d8;
            --muted: #808080;
            --accent: #7aa2f7;
            --line: #262626;
        }

        @media (prefers-color-scheme: light) {
            :root {
                --bg: #fafafa;
                --fg: #1a1a1a;
                --muted: #737373;
                --accent: #3a5bcc;
                --line: #e5e5e5;
            }
        }

        body {
            font-family: "SFMono-Regular", Menlo, Consolas, "Liberation Mono", monospace;
            background: var(--bg);
            color: var(--fg);
            line-height: 1.65;
            font-size: 16px;
        }

        .wrap {
            max-width: 680px;
            margin: 0 auto;
            padding: 80px 24px 60px;
        }

        .intro h1 {
            font-size: 1.6rem;
            font-weight: 700;
            letter-spacing: -0.4px;
            margin-bottom: 16px;
        }

        .intro p {
            color: var(--muted);
            font-size: 0.98rem;
        }

        .posts {
            margin-top: 64px;
        }

        .posts h2 {
            font-size: 0.8rem;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1.5px;
            color: var(--muted);
            margin-bottom: 24px;
        }

        .post-item {
            display: block;
            text-decoration: none;
            color: inherit;
            padding: 16px 0;
            border-top: 1px solid var(--line);
        }

        .post-item:last-child {
            border-bottom: 1px solid var(--line);
        }

        .post-item .title {
            color: var(--fg);
            font-weight: 600;
            transition: color 0.15s ease;
        }

        .post-item:hover .title {
            color: var(--accent);
        }

        .post-item .date {
            color: var(--muted);
            font-size: 0.82rem;
            margin-top: 4px;
        }

        a {
            color: var(--accent);
            text-decoration: none;
        }

        a:hover {
            text-decoration: underline;
        }

   
        footer {
            margin-top: 80px;
            padding-top: 24px;
            border-top: 1px solid var(--line);
            color: var(--muted);
            font-size: 0.82rem;
        }
        
        .footer-inner {
            display: flex;
            align-items: center;
            gap: 12px;
        }
        
        .footer-sig {
            color: var(--accent);
            font-weight: 700;
            font-size: 1rem;
            letter-spacing: 2px;
            text-transform: uppercase;
        }
        
        .footer-sep {
            color: var(--line);
            user-select: none;
        }
        
        .footer-year {
            color: var(--muted);
            font-size: 0.78rem;
        }


        .egg {
            font-size: 0.78rem;
            color: var(--muted);
            opacity: 0.55;
            padding: 12px 24px 0;
            max-width: 680px;
            margin: 0 auto;
        }
    </style>
</head>
<body>
    <div class="wrap">
        <section class="intro">
            <h1>Hello Friend 👋</h1>
            <p>I'm interested in cyber and hacking. This is where I keep my notes.</p>
        </section>

        <section class="posts">
            <h2>Notes</h2>
            {% for post in site.posts %}
            <a href="{{ post.url }}" class="post-item">
                <div class="title">{{ post.title }}</div>
                <div class="date">{{ post.date | date: "%Y-%m-%d" }}</div>
            </a>
            {% endfor %}
            {% if site.posts.size == 0 %}
            <p style="color: var(--muted);">Nothing here yet.</p>
            {% endif %}
        </section>

        <footer>
         <div class="footer-inner">
            <span class="footer-sig">- scam</span>
            <span class="footer-sep">/</span>
            <a href="https://github.com/scamrepo">github</a>
            <span class="footer-sep">/</span>
            <span class="footer-year">{{ site.time | date: "%Y" }}</span>
          </div>
        </footer>
    </div>
</body>
</html>
