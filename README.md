# Psrify Internal Functions

Welcome to **PsrifyInternalFunctions**—the tool for those who are a perfectionist with a penchant for PSR standards or just someone who prefers camelCase over snake_case, or someone who with OCD and just can’t stand the sight of snake_case lurking in their code. If you’re the type of developer who feels that deep, unspeakable urge to tidy up your codebase—especially when it comes to PHP's old legacy naming conventions—this library is your new best friend.

**PsrifyInternalFunctions** does exactly what it says on the tin: it takes PHP's internal functions (those old legacy naming snake_case ones) and converts them into clean, elegant camelCase. Because let's be honest, if you’re following **PSR-Standard** and for this case **PSR-12**, there's no room for those legacy snake_case makes you ill-feel.

## Features

- Converts PHP internal functions from snake_case to camelCase with ease.
- For those with OCD who demand PSR conformity and can’t ignore snake_case.
- No more sleepless nights thinking about the unsightly `file_get_contents()` in your code.

## Example

```php
<?php
// Before:
$fileContents = file_get_contents($filePath);

// After:
$fileContents = fileGetContents($filePath);
```

## Installation

Install **PsrifyInternalFunctions** via Composer:

```bash
composer require your-username/psrify-internal-functions
```

## Usage

```php
// Instead of calling the traditional legacy snake_case function:
$response = curl_init();

// Use the beautify camelCased version that aligned with PSR-12:
$response = curlInit();
```

## How is it working under the hood?

PsrifyInternalFunctions operates by checking if a camelCase version of a PHP internal function already exists using function_exists(). If it doesn't, the library defines it. This way, when you call fileGetContents(), it seamlessly invokes PHP's native file_get_contents() function.

Here's a sneak peek of one example on how it works:

```php

<?php
if (!function_exists('fileGetContents')) {
    function fileGetContents($filePath) {
        return file_get_contents($filePath);
    }
}
?>


```

Now, you might be thinking, "Refactor over 9,000 internal functions? No way!" And you'd be right. That's where PsrifyInternalFunctions comes in—to save you from that Herculean task.

So, whether you're a perfectionist with a penchant for PSR standards or just someone who prefers camelCase over snake_case, or someone who with OCD, this library has got your back. Sit back, relax, and let PsrifyInternalFunctions do the heavy lifting for you.

## Why Psrify?

Because if you’re going to follow PSR standards, you deserve to do it right. You wouldn’t write `user_name`, so why settle for `file_get_contents()`? Let’s make those internal functions just as clean and beautiful as your code.

For those of us with OCD (we totally understand), this is your chance to finally tidy up that PHP codebase—one camelCase function at a time.

### Say goodbye to snake_case. Hello to PSR-perfect code!
