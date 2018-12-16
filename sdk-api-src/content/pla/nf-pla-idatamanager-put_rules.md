---
UID: NF:pla.IDataManager.put_Rules
title: IDataManager::put_Rules
author: windows-sdk-content
description: Retrieves or sets the rules to apply to the report.
old-location: pla\idatamanager_rules.htm
tech.root: pla
ms.assetid: 17403e57-2eea-4a2b-a75c-66f486622078
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDataManager interface [PLA],Rules property, IDataManager.Rules, IDataManager.put_Rules, IDataManager::Rules, IDataManager::get_Rules, IDataManager::put_Rules, Rules property [PLA], Rules property [PLA],IDataManager interface, base.idatamanager_rules, pla.idatamanager_rules, pla/IDataManager::Rules, pla/IDataManager::get_Rules, pla/IDataManager::put_Rules, put_Rules
ms.topic: method
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Pla.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IDataManager.Rules
 - IDataManager.get_Rules
 - IDataManager.put_Rules
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDataManager::put_Rules


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
 

 

