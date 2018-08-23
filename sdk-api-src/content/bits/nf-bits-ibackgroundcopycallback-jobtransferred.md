---
UID: NF:bits.IBackgroundCopyCallback.JobTransferred
title: IBackgroundCopyCallback::JobTransferred
author: windows-sdk-content
description: BITS calls your implementation of the JobTransferred method when all of the files in the job have been successfully transferred.
old-location: bits\ibackgroundcopycallback_jobtransferred.htm
old-project: bits
ms.assetid: 04ff96c4-5b22-4935-bce8-5b9d3196cbe5
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IBackgroundCopyCallback interface [BITS],JobTransferred method, IBackgroundCopyCallback.JobTransferred, IBackgroundCopyCallback::JobTransferred, JobTransferred, JobTransferred method [BITS], JobTransferred method [BITS],IBackgroundCopyCallback interface, _drz_ibackgroundcopycallback_jobtransferred, bits.ibackgroundcopycallback_jobtransferred, bits/IBackgroundCopyCallback::JobTransferred
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bits.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BG_JOB_PROXY_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.h
api_name:
 - IBackgroundCopyCallback.JobTransferred
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBackgroundCopyCallback::JobTransferred


## -description


BITS calls your implementation of the 
<b>JobTransferred</b> method when all of the files in the job have been successfully transferred. For BG_JOB_TYPE_UPLOAD_REPLY jobs, BITS calls the 
<b>JobTransferred</b> method after the upload file has been transferred to the server and the reply has been transferred to the client.
		


## -parameters




### -param pJob [in]

Contains job-related information, such as the time the job completed, the number of bytes transferred, and the number of files transferred. Do not release <i>pJob</i>; BITS releases the interface when the method returns.


## -returns



This method should return <b>S_OK</b>; otherwise,  BITS continues to call this method until <b>S_OK</b> is returned. For performance reasons, you should limit the number  of times you return a value other than <b>S_OK</b> to a few times. As an alternative to returning an error code, consider always returning <b>S_OK</b> and handling the error internally. The interval at which this method is called is arbitrary.

Note that if this method fails and you   called the <a href="https://msdn.microsoft.com/61b99d01-ca0f-4a89-b7ca-77d23c21a9ad">IBackgroundCopyJob2::SetNotifyCmdLine</a> method, the command line is executed and this method is not called again.




## -remarks



Typically, your implementation should call the 
<a href="https://msdn.microsoft.com/d57b0b2e-1181-45ed-b7fc-d002d14527cf">IBackgroundCopyJob::Complete</a> method to acknowledge that BITS successfully transferred the files. Download files and the reply file are not available on the client until you call the 
<b>Complete</b> method.

If you do not call the <a href="https://msdn.microsoft.com/d57b0b2e-1181-45ed-b7fc-d002d14527cf">Complete</a> method or the 
<a href="https://msdn.microsoft.com/bb3f32d9-298a-4099-8d87-4057ddefb0ba">IBackgroundCopyJob::Cancel</a> method within 90 days (default <a href="https://msdn.microsoft.com/32c7e2b1-bac2-4708-a30c-f6b2a816c1a4">JobInactivityTimeout</a> Group Policy), BITS cancels the job and deletes the downloaded files and reply file; job cancellation does not affect files that have been successfully uploaded.

If you want to retrieve the reply data in your callback, query <i>pJob</i> for the 
<a href="https://msdn.microsoft.com/9fd422ba-a68c-40e3-8b21-3077b271e58e">IBackgroundCopyJob2</a> interface and call its 
<a href="https://msdn.microsoft.com/f29df35f-48c2-4837-9809-46bd04f08bfb">GetReplyData</a> method. To retrieve the name of the file that contains the reply data, call the 
<a href="https://msdn.microsoft.com/57f9245c-c1ae-4027-8e84-4926fa4861c3">GetReplyFileName</a> method.

BITS does not guarantee the integrity of the transferred files against third-party intrusions. Clients can implement integrity checks to validate transferred files before calling the <a href="https://msdn.microsoft.com/d57b0b2e-1181-45ed-b7fc-d002d14527cf">Complete</a>  method. To get notification when a file is transferred, implement the <a href="https://msdn.microsoft.com/c7e22911-9c14-48ef-8283-f0787b089432">IBackgroundCopyCallback2::FileTransferred</a> method. Inside the callback, call the <a href="https://msdn.microsoft.com/3fa4cc3b-b134-4e11-8bb6-1c9855d8dd37">IBackgroundCopyFile3::GetTemporaryName</a> method to get the name of the temporary file that contains the downloaded content. Validate the contents and then call the <a href="https://msdn.microsoft.com/c032ce32-07a4-4ab2-ae57-f9d526d1371a">IBackgroundCopyFile3::SetValidationState</a> method to indicate if the content is valid. If the content is not valid and BITS downloaded the file from the origin server, the job goes in the error state. If the job was downloaded from a peer, BITS downloads the file from the origin server.

<div class="alert"><b>Note</b>  BITS supports up to four simultaneous notifications per user. If one or more applications  block all four notifications for a user from returning, an application running as the same user will not receive  notifications until one or more of the blocking notifications return. To reduce the chance that your callback blocks other notifications, keep your implementation short.</div>
<div> </div>

#### Examples

See the example code for the 
<a href="https://msdn.microsoft.com/e1aa6775-d1e5-4463-ae0f-32c0498881e1">IBackgroundCopyCallback</a> interface.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e1aa6775-d1e5-4463-ae0f-32c0498881e1">IBackgroundCopyCallback</a>



<a href="https://msdn.microsoft.com/91dd1ae1-1740-4d95-a476-fc18aead1dc2">IBackgroundCopyJob</a>



<a href="https://msdn.microsoft.com/bb3f32d9-298a-4099-8d87-4057ddefb0ba">IBackgroundCopyJob::Cancel</a>



<a href="https://msdn.microsoft.com/d57b0b2e-1181-45ed-b7fc-d002d14527cf">IBackgroundCopyJob::Complete</a>
 

 

