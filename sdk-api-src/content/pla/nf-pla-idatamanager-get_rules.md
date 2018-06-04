---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IDataManager::get_Rules


## -description


Retrieves or sets the rules to apply to the report. 

This property is read/write.


## -parameters


## -remarks



The rules modify  the contents of the report after it is generated. To specify the content that TraceRpt generates, see <a href="https://msdn.microsoft.com/32620e9d-9541-4c39-9312-937b0b4825ad">IDataManager::ReportSchema</a>.

The following schema defines the rules that you can specify. The <b>Rules</b> element is the root node. You can specify one or more <b>Group</b> elements, and each <b>Group</b> element can contain one or more <b>Rule</b> elements. The <b>Help</b> element is an optional user-defined element. The <b>Step</b> element defines a set of conditions and associated actions that are taken if the conditions are met.

<div class="code"><span codelanguage="XML"><table>
<tr>
<th>XML</th>
</tr>
<tr>
<td>
<pre>&lt;Rules&gt;
    &lt;Include name="" fatal="true|false"/&gt;
    &lt;Group name="" enabled="true|false"&gt;
        &lt;Rule name="" enabled="true|false"&gt;
            &lt;Help/&gt;
            &lt;Step/&gt;
        &lt;/Rule&gt;
    &lt;/Group&gt;
&lt;/Rules&gt;
</pre>
</td>
</tr>
</table></span></div>
<div class="code"><span codelanguage="XML"><table>
<tr>
<th>XML</th>
</tr>
<tr>
<td>
<pre>&lt;Step select="" fatal="true|false" sortType="first|max|min" sortValue="" sortDataType=""&gt;
    &lt;UserInput/&gt;
    &lt;Exists&gt;
        &lt;When/&gt;
        &lt;Otherwise/&gt;
    &lt;/Exists&gt;
    &lt;Otherwise/&gt;
&lt;/Step&gt;
</pre>
</td>
</tr>
</table></span></div>
<div class="code"><span codelanguage="XML"><table>
<tr>
<th>XML</th>
</tr>
<tr>
<td>
<pre>&lt;UserInput name="" expression=""&gt;
    &lt;Description/&gt;
&lt;/UserInput&gt;
</pre>
</td>
</tr>
</table></span></div>
<div class="code"><span codelanguage="XML"><table>
<tr>
<th>XML</th>
</tr>
<tr>
<td>
<pre>&lt;When expression="" matchRE=""&gt;
    &lt;Action/&gt;
&lt;/When&gt;
...
&lt;Otherwise&gt;
    &lt;Action/&gt;
&lt;/Otherwise&gt;
</pre>
</td>
</tr>
</table></span></div>
<div class="code"><span codelanguage="XML"><table>
<tr>
<th>XML</th>
</tr>
<tr>
<td>
<pre>&lt;Variable name="" expression=""&gt;
&lt;/Variable&gt;

&lt;Warning name=""&gt;
&lt;/Warning&gt;

&lt;Notify type="" code="" severity="" title=""&gt;
&lt;/Notify&gt;

&lt;Insert select=""&gt;
    &lt;Attribute name="" value=""/&gt;
    &lt;Node axis=""/&gt;
&lt;/Insert&gt;
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/a153d88f-4c7e-45fd-9cd8-497160711de4">IDataManager</a>
 

 

