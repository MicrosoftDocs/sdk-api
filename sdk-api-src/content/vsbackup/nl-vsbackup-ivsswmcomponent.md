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

# IVssWMComponent class


## -description


The 
<b>IVssWMComponent</b> is a C++ (not COM) interface that allows access to component information stored in a Writer Metadata Document.

Instances of 
<b>IVssWMComponent</b> are obtained by calling 
<a href="https://msdn.microsoft.com/fd03ac7c-8398-4972-85f1-2afe13317950">IVssExamineWriterMetadata::GetComponent</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssWMComponent</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVssWMComponent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssWMComponent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f0c4634-2b1c-4a9b-9c13-ace38e03a7ce">FreeComponentInfo</a>
</td>
<td align="left" width="63%">
Deallocates system resources devoted to the specified component information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac01bfea-e60f-4f50-a865-5bb7e372fbf2">GetComponentInfo</a>
</td>
<td align="left" width="63%">
Obtains basic information about the specified backup component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/adb2d6f7-592c-403d-92c0-6b99e2180a6b">GetDatabaseFile</a>
</td>
<td align="left" width="63%">
Obtains an 
<a href="https://msdn.microsoft.com/0b86882d-af1b-4a09-8c25-5b806c9ca909">IVssWMFiledesc</a> object containing information about the specified database backup component file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8aaab68a-27e3-4e76-8116-530001b504a3">GetDatabaseLogFile</a>
</td>
<td align="left" width="63%">
Obtains an 
<a href="https://msdn.microsoft.com/0b86882d-af1b-4a09-8c25-5b806c9ca909">IVssWMFiledesc</a> object containing information for the log file of a specified database backup component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ead9ff63-15dc-4fcc-b341-85ad9c3eabb7">GetDependency</a>
</td>
<td align="left" width="63%">
Returns the dependency information for a component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55956a05-59b8-4197-8496-03903b6e0faa">GetFile</a>
</td>
<td align="left" width="63%">
Obtains an 
<a href="https://msdn.microsoft.com/0b86882d-af1b-4a09-8c25-5b806c9ca909">IVssWMFiledesc</a> object containing information about the specified member of a file group.

</td>
</tr>
</table> 

