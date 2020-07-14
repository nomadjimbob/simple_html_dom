# simple_html_dom

Modified version of simple_html_dom (https://sourceforge.net/projects/simplehtmldom/) for use with DokuWiki. Based on version 1.9.1.

## Modifications
* Added class option stripRNAttrValues to ignore \r \n characters in tag attribute values. This affects the DokuWiki editor ($ACT='edit')


To load DokuWiki content correctly:

`
$html = new \simple_html_dom;
$html->stripRNAttrValues = false;
$html->load($content, true, false);
`