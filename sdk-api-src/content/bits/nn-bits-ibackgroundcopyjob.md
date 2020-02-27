---
UID: NN:bits.IBackgroundCopyJob
title: IBackgroundCopyJob (bits.h)
description: Use the IBackgroundCopyJob interface to add files to the job, set the priority level of the job, determine the state of the job, and to start and stop the job.
old-location: bits\ibackgroundcopyjob.htm
tech.root: Bits
ms.assetid: 91dd1ae1-1740-4d95-a476-fc18aead1dc2
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyJob, IBackgroundCopyJob interface [BITS], IBackgroundCopyJob interface [BITS],described, _drz_ibackgroundcopyjob, bits.ibackgroundcopyjob, bits/IBackgroundCopyJob
f1_keywords:
- bits/IBackgroundCopyJob
dev_langs:
- c++
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
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- QmgrPrxy.dll
api_name:
- IBackgroundCopyJob
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBackgroundCopyJob interface


## -description


Use the 
<b>IBackgroundCopyJob</b> interface to add files to the job, set the priority level of the job, determine the state of the job, and to start and stop the job.

To create a job, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-createjob">IBackgroundCopyManager::CreateJob</a> method. To get an 
<b>IBackgroundCopyJob</b> interface pointer to an existing job, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-getjob">IBackgroundCopyManager::GetJob</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyJob</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBackgroundCopyJob</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBackgroundCopyJob</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-addfile">AddFile</a>
</td>
<td align="left" width="63%">
Adds a single file to the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-addfileset">AddFileSet</a>
</td>
<td align="left" width="63%">
Adds multiple files to the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-cancel">Cancel</a>
</td>
<td align="left" width="63%">
Cancels the job and removes temporary files from the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-complete">Complete</a>
</td>
<td align="left" width="63%">
Ends the job and saves the transferred files on the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-enumfiles">EnumFiles</a>
</td>
<td align="left" width="63%">
Returns an interface pointer to an enumerator object that you use to enumerate the files in the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getdescription">GetDescription</a>
</td>
<td align="left" width="63%">
Retrieves the description of the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getdisplayname">GetDisplayName</a>
</td>
<td align="left" width="63%">
Retrieves the display name that identifies the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-geterror">GetError</a>
</td>
<td align="left" width="63%">
Retrieves an interface pointer to the error object after an error occurs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-geterrorcount">GetErrorCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of times the job was interrupted by network failure or server unavailability.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getid">GetId</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the job in the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getminimumretrydelay">GetMinimumRetryDelay</a>
</td>
<td align="left" width="63%">
Retrieves the minimum length of time that BITS waits after encountering a transient error condition before trying to transfer the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getnoprogresstimeout">GetNoProgressTimeout</a>
</td>
<td align="left" width="63%">
Retrieves the length of time that BITS continues to try to transfer the file after encountering a transient error condition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getnotifyflags">GetNotifyFlags</a>
</td>
<td align="left" width="63%">
Retrieves the event notification (callback) flags you have set for your application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getnotifyinterface">GetNotifyInterface</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to your implementation of the 
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback">IBackgroundCopyCallback</a> interface (callbacks).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getowner">GetOwner</a>
</td>
<td align="left" width="63%">
Retrieves the job owner's identity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getpriority">GetPriority</a>
</td>
<td align="left" width="63%">
Retrieves the priority level you have set for the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getprogress">GetProgress</a>
</td>
<td align="left" width="63%">
Retrieves job-related progress information, such as the number of bytes and files transferred to the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getproxysettings">GetProxySettings</a>
</td>
<td align="left" width="63%">
Retrieves the proxy settings the job uses to transfer the files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getstate">GetState</a>
</td>
<td align="left" width="63%">
Retrieves the state of the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-gettimes">GetTimes</a>
</td>
<td align="left" width="63%">
Retrieves time stamps for activities related to the job, such as the time the job was created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-gettype">GetType</a>
</td>
<td align="left" width="63%">
Retrieves the type of transfer being performed, such as a file download.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-resume">Resume</a>
</td>
<td align="left" width="63%">
Restarts a suspended job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setdescription">SetDescription</a>
</td>
<td align="left" width="63%">
Specifies a description of the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setdisplayname">SetDisplayName</a>
</td>
<td align="left" width="63%">
Specifies a display name that identifies the job in a user interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay">SetMinimumRetryDelay</a>
</td>
<td align="left" width="63%">
Specifies the minimum length of time that BITS waits after encountering a transient error condition before trying to transfer the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout">SetNoProgressTimeout</a>
</td>
<td align="left" width="63%">
Specifies the length of time that BITS continues to try to transfer the file after encountering a transient error condition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyflags">SetNotifyFlags</a>
</td>
<td align="left" width="63%">
Specifies the type of event notification to receive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyinterface">SetNotifyInterface</a>
</td>
<td align="left" width="63%">
Specifies a pointer to your implementation of the 
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback">IBackgroundCopyCallback</a> interface (callbacks). The interface receives notification based on the event notification flags you set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setpriority">SetPriority</a>
</td>
<td align="left" width="63%">
Specifies the priority of the job relative to other jobs in the transfer queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setproxysettings">SetProxySettings</a>
</td>
<td align="left" width="63%">
Specifies which proxy to use to transfer the files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-suspend">Suspend</a>
</td>
<td align="left" width="63%">
Pauses the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-takeownership">TakeOwnership</a>
</td>
<td align="left" width="63%">
Changes the ownership of the job to the current user.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bits/nn-bits-ibackgroundcopyfile">IBackgroundCopyFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2">IBackgroundCopyJob2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bits2_0/nn-bits2_0-ibackgroundcopyjob3">IBackgroundCopyJob3</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bits/nn-bits-ibackgroundcopymanager">IBackgroundCopyManager</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bits/nn-bits-ienumbackgroundcopyjobs">IEnumBackgroundCopyJobs</a>
 

 

