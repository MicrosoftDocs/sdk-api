---
UID: NF:vsbackup.IVssExamineWriterMetadata.GetFileCounts
title: IVssExamineWriterMetadata::GetFileCounts
author: windows-sdk-content
description: The GetFileCounts method obtains excluded files and the number of components that a writer manages.
old-location: base\ivssexaminewritermetadata_getfilecounts.htm
tech.root: vss
ms.assetid: 7c1f1e9d-3154-4e03-a7dd-69b9f505dbb2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetFileCounts, GetFileCounts method [VSS], GetFileCounts method [VSS],IVssExamineWriterMetadata interface, IVssExamineWriterMetadata interface [VSS],GetFileCounts method, IVssExamineWriterMetadata.GetFileCounts, IVssExamineWriterMetadata::GetFileCounts, _win32_ivssexaminewritermetadata_getfilecounts, base.ivssexaminewritermetadata_getfilecounts, vsbackup/IVssExamineWriterMetadata::GetFileCounts
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IVssExamineWriterMetadata.GetFileCounts
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssExamineWriterMetadata::GetFileCounts


## -description


The 
<b>GetFileCounts</b> method obtains excluded files and the number of components that a writer manages.


## -parameters




### -param pcIncludeFiles [out]

Reserved for system use.


### -param pcExcludeFiles [out]

The address of a caller-allocated variable that receives the number of file sets that are explicitly excluded from the backup.


### -param pcComponents [out]

The address of a caller-allocated variable that receives the total number of components that are managed by the current writer.


## -returns



The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Successfully returned the number of files.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_INVALID_XML_DOCUMENT</b></dt>
</dl>
</td>
<td width="60%">
The XML document is not valid. Check the event log for details. For more information, see 
<a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error. The error code is logged in the error log file. For more information, see 
        <a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b3aa04d9-7299-4e3a-b092-d07f2de6eefe">IVssExamineWriterMetadata</a>



<a href="https://msdn.microsoft.com/fd03ac7c-8398-4972-85f1-2afe13317950">IVssExamineWriterMetadata::GetComponent</a>



<a href="https://msdn.microsoft.com/886d526f-c477-4c1c-80b0-65e3ea227142">IVssExamineWriterMetadata::GetExcludeFile</a>
 

 

