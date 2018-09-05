---
UID: NL:vsbackup.IVssWMComponent
title: IVssWMComponent
author: windows-sdk-content
description: The IVssWMComponent is a C++ (not COM) interface that allows access to component information stored in a Writer Metadata Document.
old-location: base\ivsswmcomponent.htm
old-project: VSS
ms.assetid: 8567ca7f-dc50-4cf2-b3c1-a2ae8d55dc95
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IVssWMComponent, IVssWMComponent interface [VSS], IVssWMComponent interface [VSS],described, _win32_ivsswmcomponent, base.ivsswmcomponent, vsbackup/IVssWMComponent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AMVPSIZE, *LPAMVPSIZE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssWMComponent
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: VssApi.dll
req.irql: 
req.product: Windows UI
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

