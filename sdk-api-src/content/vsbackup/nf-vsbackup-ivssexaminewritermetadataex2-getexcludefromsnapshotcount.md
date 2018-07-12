---
UID: NF:vsbackup.IVssExamineWriterMetadataEx2.GetExcludeFromSnapshotCount
title: IVssExamineWriterMetadataEx2::GetExcludeFromSnapshotCount
author: windows-sdk-content
description: Obtains the number of file sets that have been explicitly excluded from a given shadow copy.
old-location: base\ivssexaminewritermetadataex2_getexcludefromsnapshotcount.htm
old-project: vss
ms.assetid: 77f21feb-bd7c-4fd0-820b-9dabb1bcbc89
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: GetExcludeFromSnapshotCount, GetExcludeFromSnapshotCount method, GetExcludeFromSnapshotCount method,IVssExamineWriterMetadataEx2 interface, IVssExamineWriterMetadataEx2 interface,GetExcludeFromSnapshotCount method, IVssExamineWriterMetadataEx2.GetExcludeFromSnapshotCount, IVssExamineWriterMetadataEx2::GetExcludeFromSnapshotCount, base.ivssexaminewritermetadataex2_getexcludefromsnapshotcount, vsbackup/IVssExamineWriterMetadataEx2::GetExcludeFromSnapshotCount
ms.prod: windows
ms.technology: windows-sdk
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
 - IVssExamineWriterMetadataEx2.GetExcludeFromSnapshotCount
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssExamineWriterMetadataEx2::GetExcludeFromSnapshotCount


## -description


Obtains the number of <a href="https://msdn.microsoft.com/library/Aa384656(v=VS.85).aspx">file sets</a> that have been explicitly excluded from a given shadow copy.


## -parameters




### -param pcExcludedFromSnapshot [out]

A pointer to the number of <a href="https://msdn.microsoft.com/library/Aa384656(v=VS.85).aspx">file sets</a> explicitly excluded from the shadow copy.


## -returns



The following are the valid return codes for this method.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The number of <a href="https://msdn.microsoft.com/library/Aa384656(v=VS.85).aspx">file sets</a> was successfully returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pcExcludedFromSnapshot</i> parameter was <b>NULL</b>.

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
 




## -see-also




<a href="https://msdn.microsoft.com/6be4c63c-c36a-4ff4-92b7-63b69a030b86">IVssCreateWriterMetadataEx::AddExcludeFilesFromSnapshot</a>



<a href="https://msdn.microsoft.com/1ef5a83c-8f63-4884-8b70-a8241ba4857b">IVssExamineWriterMetadataEx2</a>



<a href="https://msdn.microsoft.com/3df57749-9a26-4187-b1fc-aeb68a4d1d06">IVssExamineWriterMetadataEx2::GetExcludeFromSnapshotFile</a>
 

 

