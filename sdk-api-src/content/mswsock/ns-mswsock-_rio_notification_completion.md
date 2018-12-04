---
UID: NS:mswsock._RIO_NOTIFICATION_COMPLETION
title: "_RIO_NOTIFICATION_COMPLETION"
author: windows-sdk-content
description: Specifies the method for I/O completion to be used with a RIONotify function for sending or receiving network data with the Winsock registered I/O extensions.
old-location: winsock\rio_notification_completion.htm
tech.root: winsock
ms.assetid: 85D3D68F-A914-4126-8D3D-4A6E3F970A4B
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: "*PRIO_NOTIFICATION_COMPLETION, PRIO_NOTIFICATION_COMPLETION, PRIO_NOTIFICATION_COMPLETION structure pointer [Winsock], RIO_NOTIFICATION_COMPLETION, RIO_NOTIFICATION_COMPLETION structure [Winsock], _RIO_NOTIFICATION_COMPLETION, mswsock/PRIO_NOTIFICATION_COMPLETION, mswsock/RIO_NOTIFICATION_COMPLETION, winsock.rio_notification_completion"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mswsock.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - HeaderDef
api_location:
 - Mswsock.h
api_name:
 - RIO_NOTIFICATION_COMPLETION
product: Windows
targetos: Windows
req.typenames: RIO_NOTIFICATION_COMPLETION, *PRIO_NOTIFICATION_COMPLETION
req.redist: 
---

# _RIO_NOTIFICATION_COMPLETION structure


## -description


The <b>RIO_NOTIFICATION_COMPLETION</b> structure specifies the method for I/O completion to be used with a <a href="https://msdn.microsoft.com/02264DAC-A3A1-4F7D-9728-17BE7F10E859">RIONotify</a> function for sending or receiving network data with the Winsock registered I/O extensions.


## -struct-fields




### -field Type

The type of completion to use with the <a href="https://msdn.microsoft.com/02264DAC-A3A1-4F7D-9728-17BE7F10E859">RIONotify</a> function when sending or receiving data.


### -field Event


### -field Event.EventHandle

The handle for the event to set following a completed <a href="https://msdn.microsoft.com/02264DAC-A3A1-4F7D-9728-17BE7F10E859">RIONotify</a> request.

This value is valid when the <b>Type </b> member is set to <b>RIO_EVENT_COMPLETION</b>.  


### -field Event.NotifyReset

The boolean value that causes the associated event to be reset when the <a href="https://msdn.microsoft.com/02264DAC-A3A1-4F7D-9728-17BE7F10E859">RIONotify</a> function is called. A non-zero value cause the associated event to be reset. 

This value is valid when the <b>Type </b> member is set to <b>RIO_EVENT_COMPLETION</b>.  


### -field Iocp


### -field Iocp.IocpHandle

The handle for the I/O completion port to use for queuing a <a href="https://msdn.microsoft.com/02264DAC-A3A1-4F7D-9728-17BE7F10E859">RIONotify</a> request completion. 

This value is valid when the <b>Type </b> member is set to <b>RIO_IOCP_COMPLETION</b>.  


### -field Iocp.CompletionKey

The value to use for <i>lpCompletionKey</i> parameter returned by the <a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a> or <a href="https://msdn.microsoft.com/3996c02c-562c-4697-a091-e241ad54b239">GetQueuedCompletionStatusEx</a> function when queuing a <a href="https://msdn.microsoft.com/02264DAC-A3A1-4F7D-9728-17BE7F10E859">RIONotify</a> request. 

This value is valid when the <b>Type </b> member is set to <b>RIO_IOCP_COMPLETION</b>.  


### -field Iocp.Overlapped

A pointer to the <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure to use when queuing a <a href="https://msdn.microsoft.com/02264DAC-A3A1-4F7D-9728-17BE7F10E859">RIONotify</a> request completion.  This member must point to a valid <b>OVERLAPPED</b> structure.  

This value is valid when the <b>Type </b> member is set to <b>RIO_IOCP_COMPLETION</b>.  


## -remarks



The <b>RIO_NOTIFICATION_COMPLETION</b> structure is used to specify the behavior of the <a href="https://msdn.microsoft.com/02264DAC-A3A1-4F7D-9728-17BE7F10E859">RIONotify</a> function used with the Winsock registered I/O extensions. 

The <b>RIO_NOTIFICATION_COMPLETION</b> structure is passed to the <a href="https://msdn.microsoft.com/ABCA52BA-FB5F-427A-9EFA-A7AA4E8D98A4">RIOCreateCompletionQueue</a> function when a  <a href="https://msdn.microsoft.com/9196F8AF-3C48-445D-B2D5-E22A99759D92">RIO_CQ</a> is created. If an application does not call the <a href="https://msdn.microsoft.com/02264DAC-A3A1-4F7D-9728-17BE7F10E859">RIONotify</a> function for a completion queue, the completion queue can be created without a <b>RIO_NOTIFICATION_COMPLETION</b> object.

For completion queues using an event, the <b>Type</b> member of the <b>RIO_NOTIFICATION_COMPLETION</b> structure is set to <b>RIO_EVENT_COMPLETION</b>. The <b>Event.EventHandle</b> member of the <b>RIO_NOTIFICATION_COMPLETION</b> structure should contain the handle for an event created by the <a href="https://msdn.microsoft.com/cff3bc31-f34c-4bb2-9004-5ec31d0a704a">WSACreateEvent</a> or <a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a> function.  To receive the <a href="https://msdn.microsoft.com/02264DAC-A3A1-4F7D-9728-17BE7F10E859">RIONotify</a> completion, the application should wait on the specified event handle using <a href="https://msdn.microsoft.com/7a978ade-6323-455b-b655-f372f4bcadc8">WSAWaitForMultipleEvents</a> or a similar wait routine.  If the application plans to reset and reuse the event, the application can reduce overhead by setting the <b>Event.NotifyReset</b> member of the <b>RIO_NOTIFICATION_COMPLETION</b> structure to a non-zero value. This causes the event to be reset by the <b>RIONotify</b> function when notification occurs. This mitigates the need to call the <a href="https://msdn.microsoft.com/99a8b0f3-977f-44cd-a224-0819d7513c90">WSAResetEvent</a> function to reset the event between calls to the <b>RIONotify</b> function.  

For completion queues using an I/O completion port, the <b>Type</b> member  of the <b>RIO_NOTIFICATION_COMPLETION</b> structure is set to <b>RIO_IOCP_COMPLETION</b>. The <b>Iocp.IocpHandle</b> member  of the <b>RIO_NOTIFICATION_COMPLETION</b> structure should contain the handle for an I/O completion port created by the <a href="https://msdn.microsoft.com/40cb47fc-7b15-47f6-bee2-2611d4686053">CreateIoCompletionPort</a> function.  To receive the <a href="https://msdn.microsoft.com/02264DAC-A3A1-4F7D-9728-17BE7F10E859">RIONotify</a> completion, the application should call the <a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a> or <a href="https://msdn.microsoft.com/3996c02c-562c-4697-a091-e241ad54b239">GetQueuedCompletionStatusEx</a> function.  The application should provide a dedicated <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> object for the completion queue, and it may also use the <b>Iocp.CompletionKey</b> member to distinguish <b>RIONotify</b> requests on the completion queue from other I/O completions including <b>RIONotify</b> completions for other completion queues.



An application using thread pools can use thread pool wait objects to get <a href="https://msdn.microsoft.com/02264DAC-A3A1-4F7D-9728-17BE7F10E859">RIONotify</a> completions via its thread pool.  In that case, the call to the <a href="https://msdn.microsoft.com/ebd0ecad-a864-43cf-a1cb-e4c2d595ef81">SetThreadpoolWait</a> function should immediately follow the call to <b>RIONotify</b>.  If the <b>SetThreadpoolWait</b> function is called before <b>RIONotify</b> and the application relies on <b>RIONotify</b> to clear the event object, this may result in spurious executions of the wait object callback.




## -see-also




<a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a>



<a href="https://msdn.microsoft.com/40cb47fc-7b15-47f6-bee2-2611d4686053">CreateIoCompletionPort</a>



<a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a>



<a href="https://msdn.microsoft.com/3996c02c-562c-4697-a091-e241ad54b239">GetQueuedCompletionStatusEx</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>



<a href="https://msdn.microsoft.com/ABCA52BA-FB5F-427A-9EFA-A7AA4E8D98A4">RIOCreateCompletionQueue</a>



<a href="https://msdn.microsoft.com/02264DAC-A3A1-4F7D-9728-17BE7F10E859">RIONotify</a>



<a href="https://msdn.microsoft.com/9196F8AF-3C48-445D-B2D5-E22A99759D92">RIO_CQ</a>



<a href="https://msdn.microsoft.com/F60DC5AD-9114-46FA-BCFF-981D637B3683">RIO_NOTIFICATION_COMPLETION_TYPE</a>



<a href="https://msdn.microsoft.com/ebd0ecad-a864-43cf-a1cb-e4c2d595ef81">SetThreadpoolWait</a>



<a href="https://msdn.microsoft.com/cff3bc31-f34c-4bb2-9004-5ec31d0a704a">WSACreateEvent</a>



<a href="https://msdn.microsoft.com/99a8b0f3-977f-44cd-a224-0819d7513c90">WSAResetEvent</a>



<a href="https://msdn.microsoft.com/7a978ade-6323-455b-b655-f372f4bcadc8">WSAWaitForMultipleEvents</a>
 

 

