---
UID: NN:shlobj_core.IACList2
title: IACList2 (shlobj_core.h)
author: windows-sdk-content
description: Extends the IACList interface to enable clients of an autocomplete object to retrieve and set option flags.
old-location: shell\IACList2.htm
tech.root: shell
ms.assetid: b765c9dd-20e9-428f-877a-aff4fac44664
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IACList2, IACList2 interface [Windows Shell], IACList2 interface [Windows Shell],described, _win32_IACList2, shell.IACList2, shlobj_core/IACList2
ms.topic: interface
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IACList2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IACList2 interface


## -description


Extends the <a href="https://msdn.microsoft.com/66513683-38ca-4b19-88d5-d14bf7ae73eb">IACList</a> interface to enable clients of an autocomplete object to retrieve and set option flags.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IACList2</b> interface inherits from <a href="https://msdn.microsoft.com/66513683-38ca-4b19-88d5-d14bf7ae73eb">IACList</a>. <b>IACList2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IACList2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/767c1972-8bc8-46d5-abf0-8c5749c0bf0e">GetOptions</a>
</td>
<td align="left" width="63%">
Gets the current autocomplete options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/963428b3-408f-4bdd-b230-9e73f21247a7">SetOptions</a>
</td>
<td align="left" width="63%">
Sets the current autocomplete options.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/66513683-38ca-4b19-88d5-d14bf7ae73eb">IACList</a> interface from which it inherits.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>

<a href="https://msdn.microsoft.com/bed6eb41-3086-4af7-8c75-651da9dba3b2">Autocompletion</a> clients implement this interface to enable the autocomplete object to retrieve and set options. The options are basically a request that the client generate a list with the names of all the files and subfolders contained by one or more specified folders. The autocomplete object then calls the client's <a href="https://msdn.microsoft.com/7f3e642a-17c7-4646-8c70-da6b0946a415">IEnumString</a> interface to request the strings.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Typically, this interface is not used directly by applications.



