---
UID: NF:bits.IBackgroundCopyCallback.JobTransferred
title: IBackgroundCopyCallback::JobTransferred
author: windows-sdk-content
description: BITS calls your implementation of the JobTransferred method when all of the files in the job have been successfully transferred.
old-location: bits\ibackgroundcopycallback_jobtransferred.htm
tech.root: Bits
ms.assetid: 04ff96c4-5b22-4935-bce8-5b9d3196cbe5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IBackgroundCopyCallback interface [BITS],JobTransferred method, IBackgroundCopyCallback.JobTransferred, IBackgroundCopyCallback::JobTransferred, JobTransferred, JobTransferred method [BITS], JobTransferred method [BITS],IBackgroundCopyCallback interface, _drz_ibackgroundcopycallback_jobtransferred, bits.ibackgroundcopycallback_jobtransferred, bits/IBackgroundCopyCallback::JobTransferred
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bits.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
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

Note that if this method fails and you   called the <a href="https://msdn.microsoft.com/en-us/library/Aa362988(v=VS.85).aspx">IBackgroundCopyJob2::SetNotifyCmdLine</a> method, the command line is executed and this method is not called again.




## -remarks



Typically, your implementation should call the 
<a href="https://msdn.microsoft.com/en-us/library/Aa363021(v=VS.85).aspx">IBackgroundCopyJob::Complete</a> method to acknowledge that BITS successfully transferred the files. Download files and the reply file are not available on the client until you call the 
<b>Complete</b> method.

If you do not call the <a href="https://msdn.microsoft.com/en-us/library/Aa363021(v=VS.85).aspx">Complete</a> method or the 
<a href="https://msdn.microsoft.com/en-us/library/Aa363020(v=VS.85).aspx">IBackgroundCopyJob::Cancel</a> method within 90 days (default <a href="https://msdn.microsoft.com/en-us/library/Aa362844(v=VS.85).aspx">JobInactivityTimeout</a> Group Policy), BITS cancels the job and deletes the downloaded files and reply file; job cancellation does not affect files that have been successfully uploaded.

If you want to retrieve the reply data in your callback, query <i>pJob</i> for the 
<a href="https://msdn.microsoft.com/en-us/library/Aa362981(v=VS.85).aspx">IBackgroundCopyJob2</a> interface and call its 
<a href="https://msdn.microsoft.com/en-us/library/Aa362983(v=VS.85).aspx">GetReplyData</a> method. To retrieve the name of the file that contains the reply data, call the 
<a href="https://msdn.microsoft.com/en-us/library/Aa362984(v=VS.85).aspx">GetReplyFileName</a> method.

BITS does not guarantee the integrity of the transferred files against third-party intrusions. Clients can implement integrity checks to validate transferred files before calling the <a href="https://msdn.microsoft.com/en-us/library/Aa363021(v=VS.85).aspx">Complete</a>  method. To get notification when a file is transferred, implement the <a href="https://msdn.microsoft.com/en-us/library/Aa362871(v=VS.85).aspx">IBackgroundCopyCallback2::FileTransferred</a> method. Inside the callback, call the <a href="https://msdn.microsoft.com/en-us/library/Aa362953(v=VS.85).aspx">IBackgroundCopyFile3::GetTemporaryName</a> method to get the name of the temporary file that contains the downloaded content. Validate the contents and then call the <a href="https://msdn.microsoft.com/en-us/library/Aa362955(v=VS.85).aspx">IBackgroundCopyFile3::SetValidationState</a> method to indicate if the content is valid. If the content is not valid and BITS downloaded the file from the origin server, the job goes in the error state. If the job was downloaded from a peer, BITS downloads the file from the origin server.

<div class="alert"><b>Note</b>  BITS supports up to four simultaneous notifications per user. If one or more applications  block all four notifications for a user from returning, an application running as the same user will not receive  notifications until one or more of the blocking notifications return. To reduce the chance that your callback blocks other notifications, keep your implementation short.</div>
<div> </div>

#### Examples

See the example code for the 
<a href="https://msdn.microsoft.com/en-us/library/Aa362867(v=VS.85).aspx">IBackgroundCopyCallback</a> interface.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362867(v=VS.85).aspx">IBackgroundCopyCallback</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362973(v=VS.85).aspx">IBackgroundCopyJob</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363020(v=VS.85).aspx">IBackgroundCopyJob::Cancel</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363021(v=VS.85).aspx">IBackgroundCopyJob::Complete</a>
 

 

