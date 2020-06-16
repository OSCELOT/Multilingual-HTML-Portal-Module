## Multilingual-HTML-Portal-Module
Updated version of http://projects-archive.oscelot.org/gf/project/bilingual_html/

This Building Block provides localised Communities Modules using the familiar plain text title and full VTBE for each active language pack.
When deployed to a Communities Tab, the content displayed will be in the user's selected language pack.

If Slick is enabled on a module, it will scroll the content using slickjs. The Module will automatically add this JS for you if it is required.
It may be necessary to edit the VTBE HTML to correctly set the content for Slick.

*These examples are used by a Module that is placed as a Tab's banner Module*
```html
<div class="vtbegenerated" style="margin-left: auto !important; margin-right: auto !important; max-width: 1440px; margin-bottom: 30px !important; overflow-x: initial !important; padding-bottom: 30px !important;">
<p><a href="https://example.org/"><img src="/modules/_1234_1/567.png" alt="Alt Text" width="1440" height="200" /></a></p>
<p><a href="https://example.org/page2/"><img src="/modules/_1234_1/568.png" alt="Alt Text" width="1440" height="200" /></a></p>
<p><a href="https://example.org/page3/"><img src="/modules/_1234_1/569.png" alt="Alt Text" width="1440" height="200" /></a></p>
</div>
``` 

It's also possible to restrict Slick'd content to:
* Show only to specific Institution Roles
* Hide from specific Instituion Roles
* Not display until after a set date and time

```html
<div class="vtbegenerated" style="margin-left: auto !important; margin-right: auto !important; max-width: 1440px; margin-bottom: 30px !important; overflow-x: initial !important; padding-bottom: 30px !important;">
<p data-aber-role="Staff"><a href="https://example.org/"><img src="/modules/_1234_1/567.png" alt="Alt Text" width="1440" height="200" /></a></p>
<p data-aber-not-role="Guest"><a href="https://example.org/page2/"><img src="/modules/_1234_1/568.png" alt="Alt Text" width="1440" height="200" /></a></p>
<p data-aber-show-after="2019-07-28 09:00"><a href="https://example.org/page3/"><img src="/modules/_1234_1/569.png" alt="Alt Text" width="1440" height="200" /></a></p>
</div>
```

If FontAwesome is enabled, the module will automatically pull in the required JS if required.
FontAwesome can then be used as normal.
```html
<div class="vtbegenerated">
<table border="0" cellpadding="7" cellspacing="2">
<tbody>
<tr>
<td align="left" valign="top"><a href="mailto:user@example.org"><i class="fa fa-comments-o fa-4x" aria-hidden="true"> </i></a></td>
<td align="left" valign="top"><a href="https://example.org/training-and-support/"><i class="fa fa-star fa-4x" aria-hidden="true"> </i></a></td>
<td align="left" valign="top"><a href="https://example.org/blackboard/"><i class="fa fa-pencil-square-o fa-4x" aria-hidden="true"> </i></a></td>
<td align="left" valign="top"><a href="https://help.blackboard.com/Learn/Student/Getting_Started/Browser_Support/Browser_Checker"><i class="fa fa-check-square-o fa-4x" aria-hidden="true"> </i></a></td>
</tr>
<tr>
<td align="left" valign="top">Contact Us</td>
<td align="left" valign="top">Training</td>
<td align="left" valign="top">Support<br />Materials</td>
<td align="left" valign="top">Check your <br />browser</td>
</tr>
</tbody>
</table>
</div>
```

### Support Matrix

| B2 Version | Minimum Learn Version |
|:----------:|:---------------------:|
| 1.4.20     | 9.1 SP8               |
| 2.1.23     | Q2 2019 / 3700.0.0    |
| 2.1.34     | Q2 2019 / 3700.0.0    |
| 2.1.36     | Q4 2019 / 3800.0.0    |

### ChangeLog

* 1.4.20 -> 2.1.23: Refactored to use Spring and the most recent Bb APIs. Added support for slick.js and fontawesome.
* 2.1.23 -> 2.1.34: Fixed bugs with automatic language fallback not firing correctly and automatic title substitution failing.
* 2.1.34 -> 2.1.36: Fixes java.lang.SecurityException: Sealing violation loading org.xml.sax.InputSource : Package org.xml.sax is sealed. error in 3800.0.0
