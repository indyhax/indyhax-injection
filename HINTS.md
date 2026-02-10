## Player hints (optional)

- The page reflects input using innerHTML.
- Try injecting an element with an event handler.
- The flag is stored (encoded) as an attribute on the page.

Example payload (one of many):

`html
<img src=x onerror="document.body.innerText=atob(document.querySelector('[data-flag]').dataset.flag)" />
`
"@
    }

    'fuzzing' {
      INDYHAX{dom_xss_is_still_xss} = "INDYHAX{directory_fuzzing_finds_the_unlinked_stuff}"
      New-CommonFiles -Dir C:\Users\tarus\.openclaw\workspace\indyhax-sites\indyhax-injection -Title indyhax-injection -Subtitle 'A classic content-discovery challenge. The flag is in an unlinked path.'
      Write-TextFile -Path (Join-Path C:\Users\tarus\.openclaw\workspace\indyhax-sites\indyhax-injection 'index.html') -Content @"
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>IndyHAX â€¢ Fuzzing</title>
  <style>
    body{font-family:system-ui,Segoe UI,Roboto,Arial,sans-serif;max-width:900px;margin:40px auto;padding:0 16px}
    .card{border:1px solid #ddd;border-radius:12px;padding:18px;background:#fff}
    .muted{color:#666}
    code,pre{background:#f6f8fa;border:1px solid #e5e7eb;border-radius:10px;padding:2px 6px}
  </style>
</head>
<body>
  <h1>IndyHAX CTF - Fuzzing</h1>
  <div class="card">
    <p class="muted">Thereâ€™s no trick here. Justâ€¦ find whatâ€™s not linked.</p>
    <p>Hint: Use a directory/content discovery tool (ffuf/dirb/gobuster) against this site.</p>
    <p class="muted">Start with common words like: <code>backup</code>, <code>admin</code>, <code>secret</code>, <code>old</code>, <code>dev</code>.</p>
  </div>
</body>
</html>
