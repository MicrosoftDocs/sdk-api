---
UID: NF:bits3_0.IBackgroundCopyFile3.GetTemporaryName
title: IBackgroundCopyFile3::GetTemporaryName
author: windows-sdk-content
description: Gets the full path of the temporary file that contains the content of the download.
old-location: bits\ibackgroundcopyfile3_gettemporaryname.htm
tech.root: bits
ms.assetid: 3fa4cc3b-b134-4e11-8bb6-1c9855d8dd37
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetTemporaryName, GetTemporaryName method [BITS], GetTemporaryName method [BITS],IBackgroundCopyFile3 interface, IBackgroundCopyFile3 interface [BITS],GetTemporaryName method, IBackgroundCopyFile3.GetTemporaryName, IBackgroundCopyFile3::GetTemporaryName, bits.ibackgroundcopyfile3_gettemporaryname, bits3_0/IBackgroundCopyFile3::GetTemporaryName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bits3_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits3_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBackgroundCopyFile3.GetTemporaryName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyFile3::GetTemporaryName


## -description


Gets the full path of the temporary file that contains the content of the download.


## -parameters




### -param pFilename [out]

Null-terminated string that contains the full path of the temporary file. Call the 
<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function to free <i>ppFileName</i> when done.


## -returns



The method returns the following return values.

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
Success

</td>
</tr>
</table>
 




## -remarks



Applications can use this method to gain access to the data before the job is complete. Open the file for shared write access (FILE_SHARE_WRITE). To determine how many bytes have been transferred and are available for reading, call the <a href="https://msdn.microsoft.com/e72ec5af-7c21-48f8-b027-76a6c9e67f5e">IBackgroundCopyFile::GetProgress</a> method. Note that the progress information will be set back to zero if the time stamp of the URL changes.

Do not open the file for reading until BITS begins transferring the file; otherwise, the job will go into the transient error state. 

 The temporary file is available until the application calls the <a href="https://msdn.microsoft.com/d57b0b2e-1181-45ed-b7fc-d002d14527cf">IBackgroundCopyJob::Complete</a> or <a href="https://msdn.microsoft.com/bb3f32d9-298a-4099-8d87-4057ddefb0ba">IBackgroundCopyJob::Cancel</a> method, or the JobInactivityTimeout group policy expires. You must release your handle to the temporary file before calling the <b>Complete</b> or <b>Cancel</b> method.

The ACL for the temporary file is the same as that of the final file when <a href="https://msdn.microsoft.com/d57b0b2e-1181-45ed-b7fc-d002d14527cf">Complete</a> is called (the ACL is inherited from the folder). 

To determine if BITS finished transferring the file, you can:

<ul>
<li>Call the <a href="https://msdn.microsoft.com/e72ec5af-7c21-48f8-b027-76a6c9e67f5e">IBackgroundCopyFile::GetProgress</a> method and compare <b>BytesTransferred</b> to <b>BytesTotal</b>.</li>
<li>Implement the <a href="https://msdn.microsoft.com/c7e22911-9c14-48ef-8283-f0787b089432">IBackgroundCopyCallback2::FileTransferred</a> callback.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/c7e22911-9c14-48ef-8283-f0787b089432">IBackgroundCopyCallback2::FileTransferred</a>



<a href="https://msdn.microsoft.com/5304f93a-993a-4327-9fdb-fb2ef1dafecb">IBackgroundCopyFile3</a>
 

 

