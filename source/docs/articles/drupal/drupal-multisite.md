---
title: Drupal Multisite Workaround
description: Best practices for having two Drupal sites on one domain.
category:
  - developing
  - drupal
keywords: drupal, multisite, domains
---
Pantheon only supports one Drupal core and one database per site. We do not support database prefixes or multisite. Our workflow, backup, and deployment tools only perform as expected given the standard Pantheon setup. If you try to install a second site inside your site container, it will most likely break it.

## Best Practice Recommendations
While we can't give specific recommendations for your sites, we can give general best practices for having two sites under one domain. This is a known Drupal problem, as it is a very common issue for which many strategies and workarounds exist. To read more about the issue, see [Multi-headed Drupal](http://www.palantir.net/blog/multi-headed-drupal).

### What Works on Pantheon

 - Separate installs with [redirection to a subdomain](https://pantheon.io/docs/articles/sites/code/redirect-incoming-requests/#redirect-to-subdirectories-or-specific-urls)
 - Features-based installs with Pantheon Enterprise [custom upstreams](https://pantheon.io/docs/articles/organizations/adding-a-custom-upstream/) and [redirection to a subdomain](https://pantheon.io/docs/articles/sites/code/redirect-incoming-requests/#redirect-to-subdirectories-or-specific-urls)
 - Domain access on a single site install. You can try the [Subfolders Domain module](https://www.drupal.org/project/subfolders_domain) but there is no guarantee it will work.
 - [Organic Groups](https://www.drupal.org/project/og)  

 ##See Also
 [Why Drupal Multisite Is Not Enterprise Grade](https://pantheon.io/blog/why-drupal-multisite-not-enterprise-grade)  
 [Drupal Multisite: Much Ado About Drupal Multisite](https://pantheon.io/blog/drupal-multisite-much-ado-about-drupal-multisite)  
 
 
