---
UID: NN:bits.IBackgroundCopyJob
title: IBackgroundCopyJob
author: windows-sdk-content
description: Use the IBackgroundCopyJob interface to add files to the job, set the priority level of the job, determine the state of the job, and to start and stop the job.
old-location: bits\ibackgroundcopyjob.htm
tech.root: bits
ms.assetid: 91dd1ae1-1740-4d95-a476-fc18aead1dc2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBackgroundCopyJob, IBackgroundCopyJob interface [BITS], IBackgroundCopyJob interface [BITS],described, _drz_ibackgroundcopyjob, bits.ibackgroundcopyjob, bits/IBackgroundCopyJob
ms.prod: windows-hardware
ms.technology: windows-devices
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
<a href="https://msdn.microsoft.com/6d23e3c0-673b-4f37-b6a0-e364b2d73886">IBackgroundCopyManager::CreateJob</a> method. To get an 
<b>IBackgroundCopyJob</b> interface pointer to an existing job, call the 
<a href="https://msdn.microsoft.com/dbb7cae6-7e9c-4ac5-8f02-372acaa4fb4d">IBackgroundCopyManager::GetJob</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyJob</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBackgroundCopyJob</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/0dada1d3-49b6-41af-b17f-612f27ea4d56">AddFile</a>
</td>
<td align="left" width="63%">
Adds a single file to the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe2f9b47-0f0a-48ab-be0e-658307cfec5f">AddFileSet</a>
</td>
<td align="left" width="63%">
Adds multiple files to the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb3f32d9-298a-4099-8d87-4057ddefb0ba">Cancel</a>
</td>
<td align="left" width="63%">
Cancels the job and removes temporary files from the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d57b0b2e-1181-45ed-b7fc-d002d14527cf">Complete</a>
</td>
<td align="left" width="63%">
Ends the job and saves the transferred files on the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6b8ef69-9c67-447f-9f90-b6905a5a5a19">EnumFiles</a>
</td>
<td align="left" width="63%">
Returns an interface pointer to an enumerator object that you use to enumerate the files in the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a791390-2bd8-4732-98a2-74f740cfd822">GetDescription</a>
</td>
<td align="left" width="63%">
Retrieves the description of the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/934cff3e-d4b8-4b76-96e1-fd7ded1842eb">GetDisplayName</a>
</td>
<td align="left" width="63%">
Retrieves the display name that identifies the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ad4c913-2d1e-4490-968c-960178a57e3b">GetError</a>
</td>
<td align="left" width="63%">
Retrieves an interface pointer to the error object after an error occurs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04ca4752-8c4d-4f54-9dfa-3c9f567d7980">GetErrorCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of times the job was interrupted by network failure or server unavailability.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc214b2e-fbf3-446e-abce-56e515dcfadf">GetId</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the job in the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af599174-44f8-4d5e-b9ff-61ddbb330580">GetMinimumRetryDelay</a>
</td>
<td align="left" width="63%">
Retrieves the minimum length of time that BITS waits after encountering a transient error condition before trying to transfer the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4881e5f7-a835-40d5-a056-d6b23e3cd84c">GetNoProgressTimeout</a>
</td>
<td align="left" width="63%">
Retrieves the length of time that BITS continues to try to transfer the file after encountering a transient error condition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4407816-a4c5-4734-9686-46d5a8133c2f">GetNotifyFlags</a>
</td>
<td align="left" width="63%">
Retrieves the event notification (callback) flags you have set for your application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a954fbc-baf6-4efa-bec0-dd86b4b7a916">GetNotifyInterface</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to your implementation of the 
<a href="https://msdn.microsoft.com/e1aa6775-d1e5-4463-ae0f-32c0498881e1">IBackgroundCopyCallback</a> interface (callbacks).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20a645d4-57ab-4b9c-b31a-b8dbb98ea550">GetOwner</a>
</td>
<td align="left" width="63%">
Retrieves the job owner's identity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8602ed59-a372-4cb3-bbda-cf1c7afc3669">GetPriority</a>
</td>
<td align="left" width="63%">
Retrieves the priority level you have set for the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30aae990-1cc1-468b-9e5f-7ef5ce6eeb9a">GetProgress</a>
</td>
<td align="left" width="63%">
Retrieves job-related progress information, such as the number of bytes and files transferred to the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c2d0ec9b-eaa1-4f78-9ccc-4e91d045cd94">GetProxySettings</a>
</td>
<td align="left" width="63%">
Retrieves the proxy settings the job uses to transfer the files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32789bd2-2368-473b-accf-ac6e317d0172">GetState</a>
</td>
<td align="left" width="63%">
Retrieves the state of the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/acc29cc2-b437-4799-9cdb-388a60f117e9">GetTimes</a>
</td>
<td align="left" width="63%">
Retrieves time stamps for activities related to the job, such as the time the job was created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b84c45c2-379a-40d0-91ab-0124f0ef6b00">GetType</a>
</td>
<td align="left" width="63%">
Retrieves the type of transfer being performed, such as a file download.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a9e6f057-0a51-4f2d-810b-edbb3e019370">Resume</a>
</td>
<td align="left" width="63%">
Restarts a suspended job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9148ec9b-7a03-4bb3-9644-e52f6cd13073">SetDescription</a>
</td>
<td align="left" width="63%">
Specifies a description of the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/504b0096-891c-4bf7-a311-9d351b359210">SetDisplayName</a>
</td>
<td align="left" width="63%">
Specifies a display name that identifies the job in a user interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52d2b7a1-6f68-424e-9c0b-a9f8df4a5ad6">SetMinimumRetryDelay</a>
</td>
<td align="left" width="63%">
Specifies the minimum length of time that BITS waits after encountering a transient error condition before trying to transfer the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3fcf46ed-197f-46ad-ac62-2c4a2e8b27ef">SetNoProgressTimeout</a>
</td>
<td align="left" width="63%">
Specifies the length of time that BITS continues to try to transfer the file after encountering a transient error condition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24aa6445-d7bd-4825-9121-402e63ae6f69">SetNotifyFlags</a>
</td>
<td align="left" width="63%">
Specifies the type of event notification to receive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34d51546-ec27-471f-9da5-3bec7ed4e1ea">SetNotifyInterface</a>
</td>
<td align="left" width="63%">
Specifies a pointer to your implementation of the 
<a href="https://msdn.microsoft.com/e1aa6775-d1e5-4463-ae0f-32c0498881e1">IBackgroundCopyCallback</a> interface (callbacks). The interface receives notification based on the event notification flags you set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b59128d-7e63-45dc-af0f-54ea844dac98">SetPriority</a>
</td>
<td align="left" width="63%">
Specifies the priority of the job relative to other jobs in the transfer queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd21a17b-1049-4dd9-a08b-da84699b8006">SetProxySettings</a>
</td>
<td align="left" width="63%">
Specifies which proxy to use to transfer the files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88429730-b8e5-4969-934c-f0945fdd46a6">Suspend</a>
</td>
<td align="left" width="63%">
Pauses the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12ac2dd8-516b-4b5d-a2bf-0abb55d18ee0">TakeOwnership</a>
</td>
<td align="left" width="63%">
Changes the ownership of the job to the current user.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fae9cf56-c211-445b-b962-9a9d7d67c59c">IBackgroundCopyFile</a>



<a href="https://msdn.microsoft.com/9fd422ba-a68c-40e3-8b21-3077b271e58e">IBackgroundCopyJob2</a>



<a href="https://msdn.microsoft.com/46e115bb-2634-4b79-b307-45720d8cb2be">IBackgroundCopyJob3</a>



<a href="https://msdn.microsoft.com/fc98dfb3-7e10-421d-b722-223bd8a65330">IBackgroundCopyManager</a>



<a href="https://msdn.microsoft.com/21ff88da-9fae-478f-bcba-488ed7a89608">IEnumBackgroundCopyJobs</a>
 

 

