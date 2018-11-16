---
UID: NF:vsbackup.IVssExamineWriterMetadataEx2.GetExcludeFromSnapshotFile
title: IVssExamineWriterMetadataEx2::GetExcludeFromSnapshotFile
author: windows-sdk-content
description: Obtains information about file sets that have been explicitly excluded from a given shadow copy.
old-location: base\ivssexaminewritermetadataex2_getexcludefromsnapshotfile.htm
tech.root: VSS
ms.assetid: 3df57749-9a26-4187-b1fc-aeb68a4d1d06
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetExcludeFromSnapshotFile, GetExcludeFromSnapshotFile method, GetExcludeFromSnapshotFile method,IVssExamineWriterMetadataEx2 interface, IVssExamineWriterMetadataEx2 interface,GetExcludeFromSnapshotFile method, IVssExamineWriterMetadataEx2.GetExcludeFromSnapshotFile, IVssExamineWriterMetadataEx2::GetExcludeFromSnapshotFile, base.ivssexaminewritermetadataex2_getexcludefromsnapshotfile, vsbackup/IVssExamineWriterMetadataEx2::GetExcludeFromSnapshotFile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
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
 - IVssExamineWriterMetadataEx2.GetExcludeFromSnapshotFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- vsbackup.h
: 
- IVssExamineWriterMetadataEx2.GetExcludeFromSnapshotFile
: 
---

# IVssExamineWriterMetadataEx2::GetExcludeFromSnapshotFile


## -description


Obtains information about <a href="https://msdn.microsoft.com/en-us/library/Aa384656(v=VS.85).aspx">file sets</a> that have been explicitly excluded from a given shadow copy.


## -parameters




### -param iFile [in]

An index for an excluded <a href="https://msdn.microsoft.com/en-us/library/Aa384656(v=VS.85).aspx">file set</a>. The value of this parameter is an integer from 0 
      to <i>n</i>–1 inclusive, where <i>n</i> is the total number of <i>file sets</i> explicitly excluded from a given shadow copy. The value of <i>n</i> is returned by 
the <b>IVssExamineWriterMetadataEx2::GetExcludeFromSnapshotCount</b> method.


### -param ppFiledesc [out]

A doubly indirect pointer to an 
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
The pointer to an 
<a href="https://msdn.microsoft.com/0b86882d-af1b-4a09-8c25-5b806c9ca909">IVssWMFiledesc</a> interface was successfully returned.

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



The caller is responsible for calling the <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> method to release the resources of the returned 
<a href="https://msdn.microsoft.com/0b86882d-af1b-4a09-8c25-5b806c9ca909">IVssWMFiledesc</a> object.

The <b>GetExcludeFromSnapshotFile</b> method is intended to report information about <a href="https://msdn.microsoft.com/en-us/library/Aa384656(v=VS.85).aspx">file sets</a> excluded from a shadow copy. Requesters should not exclude files from backup based on the information returned by this method.




## -see-also




<a href="https://msdn.microsoft.com/6be4c63c-c36a-4ff4-92b7-63b69a030b86">IVssCreateWriterMetadataEx::AddExcludeFilesFromSnapshot</a>



<a href="https://msdn.microsoft.com/1ef5a83c-8f63-4884-8b70-a8241ba4857b">IVssExamineWriterMetadataEx2</a>



<a href="https://msdn.microsoft.com/3df57749-9a26-4187-b1fc-aeb68a4d1d06">IVssExamineWriterMetadataEx2::GetExcludeFromSnapshotCount</a>
 

 

