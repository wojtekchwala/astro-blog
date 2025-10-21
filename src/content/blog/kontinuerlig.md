---
title: "KONTINUERLIG: Chaining GitHub Actions Exploits to Steal Secrets - Hack.lu 2025 Writeup"
description: "Hack.lu 2025 Writeup"
pubDate: "Oct 22 2025"
heroImage: "/"
tags: ["ctf", "hack.lu"]
---

During Hack.lu 2025, I encountered KONTINUERLIG - a deceptively elegant challenge that showcases just how dangerous misconfigurations in GitHub Actions can be. What started as a simple code review task quickly spiraled into a multi-stage exploitation chain involving heredoc injection, environment variable manipulation, Docker breakouts, and ultimately bypassing GitHub's secret redaction mechanisms.
The challenge presents you with a seemingly innocent private GitHub repository containing three workflow files and a single secret named flag. Your mission? Extract that flag. Simple, right? Not quite.

> KONTINUERLIG (Norwegian for "continuous" - a nod to CI/CD) brilliantly demonstrates real-world attack patterns found in production GitHub Actions configurations. It's not just a CTF challenge; it's a cautionary tale about the security pitfalls of CI/CD pipelines that many organizations face today.
