---
UID: NL:vswriter.IVssWMFiledesc
title: IVssWMFiledesc
author: windows-sdk-content
description: The IVssWMFiledesc interface is a C++ (not COM) interface returned to a calling application by a number of query methods. It provides detailed information about a file or set of files (a file set).
old-location: base\ivsswmfiledesc.htm
old-project: VSS
ms.assetid: 0b86882d-af1b-4a09-8c25-5b806c9ca909
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IVssWMFiledesc, IVssWMFiledesc interface [VSS], IVssWMFiledesc interface [VSS],described, _win32_ivsswmfiledesc, base.ivsswmfiledesc, vswriter/IVssWMFiledesc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
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
req.typenames: VSS_WRITERRESTORE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VssApi.lib
-	VssApi.dll
api_name:
-	IVssWMFiledesc
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssWMFiledesc class


## -description


The 
<b>IVssWMFiledesc</b> interface is a C++ (not COM) interface returned to a calling application by a number of query methods. It provides detailed information about a file or set of files (a file set).

The calling application is responsible for calling <a href="_com_iunknown_release">IUnknown::Release</a> to release the resources held by the returned 
<b>IVssWMFiledesc</b> interface when it is no longer needed.

The following methods return an 
<b>IVssWMFiledesc</b> interface:
<ul>
<li>
<a href="https://msdn.microsoft.com/8c6537eb-67ba-4d6a-ac86-44da176ef5c5">IVssComponent::GetAlternateLocationMapping</a>
</li>
<li>
<a href="https://msdn.microsoft.com/21f22fae-2230-418b-8942-754c863a9213">IVssComponent::GetNewTarget</a>
</li>
<li>
<a href="https://msdn.microsoft.com/886d526f-c477-4c1c-80b0-65e3ea227142">IVssExamineWriterMetadata::GetExcludeFile</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1264d4bc-dd45-41e7-9f95-c6e9aebd4d22">IVssExamineWriterMetadata::GetAlternateLocationMapping</a>
</li>
<li>
<a href="https://msdn.microsoft.com/55956a05-59b8-4197-8496-03903b6e0faa">IVssWMComponent::GetFile</a>
</li>
<li>
<a href="https://msdn.microsoft.com/adb2d6f7-592c-403d-92c0-6b99e2180a6b">IVssWMComponent::GetDatabaseFile</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8aaab68a-27e3-4e76-8116-530001b504a3">IVssWMComponent::GetDatabaseLogFile</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssWMFiledesc</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVssWMFiledesc</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssWMFiledesc</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3bb787eb-ac15-40d0-9901-b869442399c5">GetAlternateLocation</a>
</td>
<td align="left" width="63%">
Obtains the alternate backup location of the component files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d5f3a16-2053-42dd-867d-740c4a34bdb6">GetBackupTypeMask</a>
</td>
<td align="left" width="63%">
Obtains the file backup specification for a file or set of files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9661d22b-5c82-412d-966d-83605c568e22">GetFilespec</a>
</td>
<td align="left" width="63%">
Obtains the file specification for the list of files provided.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/mt432961">GetPath</a>
</td>
<td align="left" width="63%">
Obtains the fully qualified directory path for the list of files provided.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f467bd6f-997b-4d5f-87a4-727d9a84a222">GetRecursive</a>
</td>
<td align="left" width="63%">
Determines whether only files in the root directory or files in the entire directory hierarchy are considered for backup.

</td>
</tr>
</table> 

