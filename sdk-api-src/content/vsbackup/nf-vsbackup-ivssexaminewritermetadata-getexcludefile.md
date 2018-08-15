---
UID: NF:vsbackup.IVssExamineWriterMetadata.GetExcludeFile
title: IVssExamineWriterMetadata::GetExcludeFile
author: windows-sdk-content
description: The GetExcludeFile method obtains information about files that have been explicitly excluded from backup for a given writer.
old-location: base\ivssexaminewritermetadata_getexcludefile.htm
old-project: vss
ms.assetid: 886d526f-c477-4c1c-80b0-65e3ea227142
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetExcludeFile, GetExcludeFile method [VSS], GetExcludeFile method [VSS],IVssExamineWriterMetadata interface, IVssExamineWriterMetadata interface [VSS],GetExcludeFile method, IVssExamineWriterMetadata.GetExcludeFile, IVssExamineWriterMetadata::GetExcludeFile, _win32_ivssexaminewritermetadata_getexcludefile, base.ivssexaminewritermetadata_getexcludefile, vsbackup/IVssExamineWriterMetadata::GetExcludeFile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IVssExamineWriterMetadata.GetExcludeFile
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssExamineWriterMetadata::GetExcludeFile


## -description


The 
<b>GetExcludeFile</b> method obtains information about files that have been explicitly excluded from backup for a given writer.


## -parameters




### -param iFile [in]

Index for an excluded file set. The value of this parameter is an integer from 0 
      to <i>n</i>–1 inclusive, where <i>n</i> is the total number of file sets explicitly excluded from the components of a given writer. The value of <i>n</i> is returned by 
<a href="https://msdn.microsoft.com/7c1f1e9d-3154-4e03-a7dd-69b9f505dbb2">IVssExamineWriterMetadata::GetFileCounts</a>.


### -param ppFiledesc [out]

Doubly indirect pointer to an 
<a href="https://msdn.microsoft.com/0b86882d-af1b-4a09-8c25-5b806c9ca909">IVssWMFiledesc</a> object containing the file element information.


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
Successfully returned a pointer to an 
<a href="https://msdn.microsoft.com/0b86882d-af1b-4a09-8c25-5b806c9ca909">IVssWMFiledesc</a> interface.

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
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The file set specified for exclusion does not exist.

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
 




## -remarks



For more information on excluding files, see 
<a href="writer_metadata_document_contents.htm">Exclude File List Specification</a>.

The caller is responsible for calling <a href="_com_iunknown_release">IUnknown::Release</a> to release the resources of the returned 
<a href="https://msdn.microsoft.com/0b86882d-af1b-4a09-8c25-5b806c9ca909">IVssWMFiledesc</a> object.




## -see-also




<a href="https://msdn.microsoft.com/b3aa04d9-7299-4e3a-b092-d07f2de6eefe">IVssExamineWriterMetadata</a>



<a href="https://msdn.microsoft.com/7c1f1e9d-3154-4e03-a7dd-69b9f505dbb2">IVssExamineWriterMetadata::GetFileCounts</a>
 

 

