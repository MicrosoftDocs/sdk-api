---
UID: NF:bits3_0.IBackgroundCopyCallback2.FileTransferred
title: IBackgroundCopyCallback2::FileTransferred
author: windows-sdk-content
description: BITS calls your implementation of the FileTransferred method when BITS successfully finishes transferring a file.
old-location: bits\ibackgroundcopycallback2_filetransferred.htm
tech.root: Bits
ms.assetid: c7e22911-9c14-48ef-8283-f0787b089432
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: FileTransferred, FileTransferred method [BITS], FileTransferred method [BITS],IBackgroundCopyCallback2 interface, IBackgroundCopyCallback2 interface [BITS],FileTransferred method, IBackgroundCopyCallback2.FileTransferred, IBackgroundCopyCallback2::FileTransferred, bits.ibackgroundcopycallback2_filetransferred, bits3_0/IBackgroundCopyCallback2::FileTransferred
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
 - IBackgroundCopyCallback2.FileTransferred
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyCallback2::FileTransferred


## -description


BITS calls your implementation of the 
<b>FileTransferred</b> method when BITS successfully finishes transferring a file.
		


## -parameters




### -param pJob [in]

Contains job-related information. Do not release <i>pJob</i>; BITS releases the interface when this method returns.


### -param pFile [in]

Contains file-related information. Do not release <i>pFile</i>; BITS releases the interface when this method returns.


## -returns



This method should return <b>S_OK</b>; otherwise,  if negative, BITS continues to call this method until <b>S_OK</b> is returned. For performance reasons, you should limit the number  of times you return a value other than <b>S_OK</b> to a few times. As an alternative to returning an error code, consider always returning <b>S_OK</b> and handling the error internally. The interval at which this method is called is arbitrary.




## -remarks



Typically, you would not use this callback unless you want to validate the contents of the file that was downloaded. Validating the file may be important to you if you are downloading content that could be served to peers. 

To get the name of the temporary file that contains the downloaded content, call the <a href="https://msdn.microsoft.com/en-us/library/Aa362953(v=VS.85).aspx">IBackgroundCopyFile3::GetTemporaryName</a> method. After verifying the content, call the <a href="https://msdn.microsoft.com/en-us/library/Aa362955(v=VS.85).aspx">IBackgroundCopyFile3::SetValidationState</a> method to indicate to BITS if the contents of the file is valid. If you set the validation state to <b>FALSE</b> and the content is from the origin server, the job moves to the error state. 

If the content is from a peer, BITS downloads the file from the origin server. The callback is called again after the file transfer from the origin server completes.

<b>BITS 3.0:  </b>The callback is not called again after the file transfer from the origin server completes.

For a job, <b>FileTransferred</b> callbacks are serialized. BITS will not dispatch a callback for the next file in the job until the current callback returns successfully.

<b>FileTransferred</b> callbacks are dispatched before <a href="https://msdn.microsoft.com/en-us/library/Aa362874(v=VS.85).aspx">JobTransferred</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa362872(v=VS.85).aspx">JobError</a> callbacks.

The <b>FileTransferred</b> callback is for download jobs or the reply portion of an upload-reply job. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362867(v=VS.85).aspx">IBackgroundCopyCallback</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362870(v=VS.85).aspx">IBackgroundCopyCallback2</a>
 

 

