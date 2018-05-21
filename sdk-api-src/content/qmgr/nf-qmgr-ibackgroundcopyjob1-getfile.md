---
UID: NF:qmgr.IBackgroundCopyJob1.GetFile
title: IBackgroundCopyJob1::GetFile
author: windows-driver-content
description: Use the GetFile method to retrieve the remote and local file names for the given file in the job.
old-location: bits\ibackgroundcopyjob1_getfile.htm
old-project: Bits
ms.assetid: 6cd680cc-abe0-44e1-a650-079295a8dd4a
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: GetFile, GetFile method [BITS], GetFile method [BITS],IBackgroundCopyJob1 interface, IBackgroundCopyJob1 interface [BITS],GetFile method, IBackgroundCopyJob1.GetFile, IBackgroundCopyJob1::GetFile, bits.ibackgroundcopyjob1_getfile, qmgr/IBackgroundCopyJob1::GetFile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: qmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Qmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: GROUPPROP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	QmgrPrxy.dll
api_name:
-	IBackgroundCopyJob1.GetFile
product: Windows
targetos: Windows
req.lib: 
req.dll: QmgrPrxy.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IBackgroundCopyJob1::GetFile


## -description


<p class="CCE_Message">[<b>IBackgroundCopyJob1</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/72668c9b-e6f3-4f3f-9d4b-50d930d1889d">BITS interfaces</a>.]

Use the <b>GetFile</b> method to retrieve the remote and local file names for the given file in the job.


## -parameters




### -param cFileIndex [in]

Zero-based index that identifies the file in the job.


### -param pFileInfo [out]

A <a href="https://msdn.microsoft.com/1a1d6683-5317-4a34-828d-55142f64f19f">FILESETINFO</a> structure that contains the remote and local names of the file.


## -returns



This method returns the following <b>HRESULT</b> values, as well as others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
Successfully retrieved the file from the job.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>QM_E_ITEM_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified index is greater than the number of files in the job.

</td>
</tr>
</table>
 




## -remarks



Use with <a href="https://msdn.microsoft.com/6aec5e9c-2950-4039-99a4-b1884a9a4673">IBackgroundCopyJob1::GetFileCount</a> to iterate through the files of a job.




## -see-also




<a href="https://msdn.microsoft.com/ccf1b355-c1af-4b5e-b613-181c426ed777">IBackgroundCopyJob1</a>
 

 

