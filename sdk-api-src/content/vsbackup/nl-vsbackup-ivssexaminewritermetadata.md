---
UID: NL:vsbackup.IVssExamineWriterMetadata
title: IVssExamineWriterMetadata
author: windows-sdk-content
description: The IVssExamineWriterMetadata interface is a C++ (not COM) interface that allows a requester to examine the metadata of a specific writer instance.
old-location: base\ivssexaminewritermetadata.htm
tech.root: VSS
ms.assetid: b3aa04d9-7299-4e3a-b092-d07f2de6eefe
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IVssExamineWriterMetadata, IVssExamineWriterMetadata interface [VSS], IVssExamineWriterMetadata interface [VSS],described, _win32_ivssexaminewritermetadata, base.ivssexaminewritermetadata, vsbackup/IVssExamineWriterMetadata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
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
req.lib: VssApi.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssExamineWriterMetadata
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssExamineWriterMetadata class


## -description


The 
<b>IVssExamineWriterMetadata</b> interface is a C++ (not COM) interface that allows a requester to examine the metadata of a specific writer instance. This metadata may come from a currently executing (live) writer, or it may have been stored as an XML document.

An 
<b>IVssExamineWriterMetadata</b> interface to a live writer's metadata is obtained by a call to 
<a href="https://msdn.microsoft.com/a577d06a-4c9d-4ebe-b4d4-685f96ec9c83">IVssBackupComponents::GetWriterMetadata</a>.

Metadata obtained from a stored XML document can be examined by an instance of 
<b>IVssExamineWriterMetadata</b> obtained by a call to 
<a href="https://msdn.microsoft.com/cb322541-d8c0-4a2e-9ce5-453d19ac3fd1">CreateVssExamineWriterMetadata</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssExamineWriterMetadata</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVssExamineWriterMetadata</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssExamineWriterMetadata</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1264d4bc-dd45-41e7-9f95-c6e9aebd4d22">GetAlternateLocationMapping</a>
</td>
<td align="left" width="63%">
Obtains information about the specified alternate location mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7099d6e-b8dd-44a5-af68-f3347c5d251b">GetBackupSchema</a>
</td>
<td align="left" width="63%">
Gets the backup schema (how a backup is to be executed) to be used when processing a writer's files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd03ac7c-8398-4972-85f1-2afe13317950">GetComponent</a>
</td>
<td align="left" width="63%">
Obtains information about a specified backup component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ade4232-147b-4e56-b45c-e692d08cfcdc">GetDocument</a>
</td>
<td align="left" width="63%">
Reserved for system use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/886d526f-c477-4c1c-80b0-65e3ea227142">GetExcludeFile</a>
</td>
<td align="left" width="63%">
Obtains the specified file element excluded from the backup.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c1f1e9d-3154-4e03-a7dd-69b9f505dbb2">GetFileCounts</a>
</td>
<td align="left" width="63%">
Obtains file element information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55240ef2-f480-4917-98f9-e88a2e23edea">GetIdentity</a>
</td>
<td align="left" width="63%">
Obtains basic information about a specific writer instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a47dbe9-f27d-4f84-bccd-6c7d46e9238b">GetIncludeFile</a>
</td>
<td align="left" width="63%">
Reserved for system use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c93f841f-057c-4aee-b8f2-263395e84c7b">GetRestoreMethod</a>
</td>
<td align="left" width="63%">
Returns information on how the writer data is to be restored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a508a2c-1c42-4414-9c54-a78d1e1564a0">LoadFromXML</a>
</td>
<td align="left" width="63%">
Converts the specified string of backup data into writer metadata.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/146dcd00-e479-40fa-963b-e7111b783822">SaveAsXML</a>
</td>
<td align="left" width="63%">
Converts the specified string of writer metadata into a string that can be saved as part of the backup.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/427ed302-c3b7-483a-aa48-da6fec1160a9">IVssCreateWriterMetadata</a>
 

 

