+++
title = 'Why I Think Ruby on Rails Is Better Than Next.js'
date = 2025-06-24T20:41:30+02:00
draft = false
+++

Over the past few days, I’ve been working with Next.js on a project at my company. It’s one of my first serious experiences with the framework. I had briefly tried it before, but chose Svelte instead when working with TypeScript. These days, I prefer Ruby on Rails 8.

Now that I’ve spent some time building real features with what many call the most popular framework in the world, I honestly can’t understand why it’s so mainstream.

Here’s why I think **Ruby on Rails is better**:

## A Power Tool, Not Just a Framework

With Rails, you get everything you need to build a large-scale full stack application out of the box. Need async jobs? Use **Solid Queue**. Caching? **Solid Cache**. Real-time WebSocket updates? **Solid Cable**. It’s not just a framework — it’s a full toolkit with batteries included.

Also, remember how you always have to include Redis in production with Next.js? In Rails, you can often just use your default database (even SQLite) for background jobs. That’s one less dependency to manage.

In the past, I appreciated frameworks like Svelte and React for their SPA capabilities. But today, with **Hotwire/Turbo**, Rails offers the same experience — and in my opinion, it’s even simpler.

## Syntax

Honestly, I find the Next.js/React syntax frustrating. And I truly believe anyone who claims otherwise is kidding themselves. Why does creating a reactive variable require so much boilerplate?

You need a surprising amount of code just to build something basic. And constantly returning divs doesn’t feel odd to anyone?

```ts
import { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0); // reactive variable

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={() => setCount(count + 1)}>Increment</button>
    </div>
  );
}
```

Compared to Svelte, which allows you to write straightforward, clean code with minimal overhead, React/Next.js often feels like overengineering.

```ts
<script>
  let count: number = 0;
</script>

<p>Count: {count}</p>
<button on:click={() => count + 1}>Increment</button>
```

## Deployment

I typically deploy Rails apps using **Kamal 2**, a tool built by DHH (the creator of Rails). With minimal configuration, I can deploy to multiple servers, including databases, using plain Docker and a simple VPS.

Maybe it’s just me, but I couldn’t get anything comparable working with Next.js. I’ve deployed SvelteKit, Rails, and even Go apps without a hitch — but Next.js? Always issues.

Funnily enough, the moment you use Vercel or Azure, everything magically works. Curious, huh?

## Security Issues

Let’s not forget the [major middleware vulnerability in Next.js](https://www.cve.org/CVERecord?id=CVE-2025-29927). It’s a reminder that even the trendiest tools aren’t immune to serious security flaws.

## Culture

I strongly believe in mature, stable technologies. No, I don’t think AI needs to be included in every single app. Like AI, Next.js is constantly evolving — syntax and conventions change often, forcing developers to frequently update their code.

Rails also evolves, but in a much more deliberate and stable way. It’s a 20-year-old framework with thoughtful, paced improvements. The Next.js culture, on the other hand, feels like it’s always chasing the next new thing. That’s just not my style.

People often criticize me for preferring Basecamp over Monday or Jira, or for driving an old Volkswagen instead of a new electric Mercedes. That’s just who I am — and Rails fits that philosophy perfectly. It updates only when needed, once the dust has settled.

---
