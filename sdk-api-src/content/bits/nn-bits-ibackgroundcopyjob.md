---
UID: NN:bits.IBackgroundCopyJob
title: IBackgroundCopyJob
author: windows-sdk-content
description: Use the IBackgroundCopyJob interface to add files to the job, set the priority level of the job, determine the state of the job, and to start and stop the job.
old-location: bits\ibackgroundcopyjob.htm
tech.root: Bits
ms.assetid: 91dd1ae1-1740-4d95-a476-fc18aead1dc2
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IBackgroundCopyJob, IBackgroundCopyJob interface [BITS], IBackgroundCopyJob interface [BITS],described, _drz_ibackgroundcopyjob, bits.ibackgroundcopyjob, bits/IBackgroundCopyJob
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyJob interface


## -description


Use the 
<b>IBackgroundCopyJob</b> interface to add files to the job, set the priority level of the job, determine the state of the job, and to start and stop the job.

To create a job, call the 
<a href="https://msdn.microsoft.com/en-us/library/Aa363051(v=VS.85).aspx">IBackgroundCopyManager::CreateJob</a> method. To get an 
<b>IBackgroundCopyJob</b> interface pointer to an existing job, call the 
<a href="https://msdn.microsoft.com/en-us/library/Aa363060(v=VS.85).aspx">IBackgroundCopyManager::GetJob</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyJob</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IBackgroundCopyJob</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa363017(v=VS.85).aspx">AddFile</a>
</td>
<td align="left" width="63%">
Adds a single file to the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363019(v=VS.85).aspx">AddFileSet</a>
</td>
<td align="left" width="63%">
Adds multiple files to the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363020(v=VS.85).aspx">Cancel</a>
</td>
<td align="left" width="63%">
Cancels the job and removes temporary files from the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363021(v=VS.85).aspx">Complete</a>
</td>
<td align="left" width="63%">
Ends the job and saves the transferred files on the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363022(v=VS.85).aspx">EnumFiles</a>
</td>
<td align="left" width="63%">
Returns an interface pointer to an enumerator object that you use to enumerate the files in the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363023(v=VS.85).aspx">GetDescription</a>
</td>
<td align="left" width="63%">
Retrieves the description of the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363024(v=VS.85).aspx">GetDisplayName</a>
</td>
<td align="left" width="63%">
Retrieves the display name that identifies the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363025(v=VS.85).aspx">GetError</a>
</td>
<td align="left" width="63%">
Retrieves an interface pointer to the error object after an error occurs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363026(v=VS.85).aspx">GetErrorCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of times the job was interrupted by network failure or server unavailability.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363027(v=VS.85).aspx">GetId</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the job in the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363028(v=VS.85).aspx">GetMinimumRetryDelay</a>
</td>
<td align="left" width="63%">
Retrieves the minimum length of time that BITS waits after encountering a transient error condition before trying to transfer the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363029(v=VS.85).aspx">GetNoProgressTimeout</a>
</td>
<td align="left" width="63%">
Retrieves the length of time that BITS continues to try to transfer the file after encountering a transient error condition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363030(v=VS.85).aspx">GetNotifyFlags</a>
</td>
<td align="left" width="63%">
Retrieves the event notification (callback) flags you have set for your application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363031(v=VS.85).aspx">GetNotifyInterface</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to your implementation of the 
<a href="https://msdn.microsoft.com/en-us/library/Aa362867(v=VS.85).aspx">IBackgroundCopyCallback</a> interface (callbacks).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363032(v=VS.85).aspx">GetOwner</a>
</td>
<td align="left" width="63%">
Retrieves the job owner's identity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363033(v=VS.85).aspx">GetPriority</a>
</td>
<td align="left" width="63%">
Retrieves the priority level you have set for the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363034(v=VS.85).aspx">GetProgress</a>
</td>
<td align="left" width="63%">
Retrieves job-related progress information, such as the number of bytes and files transferred to the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363035(v=VS.85).aspx">GetProxySettings</a>
</td>
<td align="left" width="63%">
Retrieves the proxy settings the job uses to transfer the files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363036(v=VS.85).aspx">GetState</a>
</td>
<td align="left" width="63%">
Retrieves the state of the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363037(v=VS.85).aspx">GetTimes</a>
</td>
<td align="left" width="63%">
Retrieves time stamps for activities related to the job, such as the time the job was created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363038(v=VS.85).aspx">GetType</a>
</td>
<td align="left" width="63%">
Retrieves the type of transfer being performed, such as a file download.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363039(v=VS.85).aspx">Resume</a>
</td>
<td align="left" width="63%">
Restarts a suspended job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363040(v=VS.85).aspx">SetDescription</a>
</td>
<td align="left" width="63%">
Specifies a description of the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363041(v=VS.85).aspx">SetDisplayName</a>
</td>
<td align="left" width="63%">
Specifies a display name that identifies the job in a user interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363042(v=VS.85).aspx">SetMinimumRetryDelay</a>
</td>
<td align="left" width="63%">
Specifies the minimum length of time that BITS waits after encountering a transient error condition before trying to transfer the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363043(v=VS.85).aspx">SetNoProgressTimeout</a>
</td>
<td align="left" width="63%">
Specifies the length of time that BITS continues to try to transfer the file after encountering a transient error condition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363044(v=VS.85).aspx">SetNotifyFlags</a>
</td>
<td align="left" width="63%">
Specifies the type of event notification to receive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363045(v=VS.85).aspx">SetNotifyInterface</a>
</td>
<td align="left" width="63%">
Specifies a pointer to your implementation of the 
<a href="https://msdn.microsoft.com/en-us/library/Aa362867(v=VS.85).aspx">IBackgroundCopyCallback</a> interface (callbacks). The interface receives notification based on the event notification flags you set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363046(v=VS.85).aspx">SetPriority</a>
</td>
<td align="left" width="63%">
Specifies the priority of the job relative to other jobs in the transfer queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363047(v=VS.85).aspx">SetProxySettings</a>
</td>
<td align="left" width="63%">
Specifies which proxy to use to transfer the files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363048(v=VS.85).aspx">Suspend</a>
</td>
<td align="left" width="63%">
Pauses the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa363049(v=VS.85).aspx">TakeOwnership</a>
</td>
<td align="left" width="63%">
Changes the ownership of the job to the current user.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362881(v=VS.85).aspx">IBackgroundCopyFile</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362981(v=VS.85).aspx">IBackgroundCopyJob2</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362990(v=VS.85).aspx">IBackgroundCopyJob3</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363050(v=VS.85).aspx">IBackgroundCopyManager</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363109(v=VS.85).aspx">IEnumBackgroundCopyJobs</a>
 

 

