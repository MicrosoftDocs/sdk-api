---
UID: NE:mswsock._RIO_NOTIFICATION_COMPLETION_TYPE
title: "_RIO_NOTIFICATION_COMPLETION_TYPE"
author: windows-sdk-content
description: Specifies the type of completion queue notifications to use with the RIONotify function when sending or receiving data using the Winsock registered I/O extensions.
old-location: winsock\rio_notification_completion_type.htm
old-project: WinSock
ms.assetid: F60DC5AD-9114-46FA-BCFF-981D637B3683
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: "*PRIO_NOTIFICATION_COMPLETION_TYPE, RIO_EVENT_COMPLETION, RIO_IOCP_COMPLETION, RIO_NOTIFICATION_COMPLETION_TYPE, RIO_NOTIFICATION_COMPLETION_TYPE enumeration [Winsock], _RIO_NOTIFICATION_COMPLETION_TYPE, mswsock/RIO_EVENT_COMPLETION, mswsock/RIO_IOCP_COMPLETION, mswsock/RIO_NOTIFICATION_COMPLETION_TYPE, winsock.rio_notification_completion_type"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: RIO_NOTIFICATION_COMPLETION_TYPE, *PRIO_NOTIFICATION_COMPLETION_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mswsock.h
api_name:
 - RIO_NOTIFICATION_COMPLETION_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _RIO_NOTIFICATION_COMPLETION_TYPE enumeration


## -description


The <b>RIO_NOTIFICATION_COMPLETION_TYPE</b> enumeration specifies the type of completion queue notifications to use with the <a href="https://msdn.microsoft.com/02264DAC-A3A1-4F7D-9728-17BE7F10E859">RIONotify</a> function when sending or receiving data using the Winsock registered I/O extensions. 


## -enum-fields




### -field RIO_EVENT_COMPLETION

An event handle is used to signal completion queue notifications. 

An event handle is provided as the <b>EventNotify.EventHandle</b> member in the <a href="https://msdn.microsoft.com/85D3D68F-A914-4126-8D3D-4A6E3F970A4B">RIO_NOTIFICATION_COMPLETION</a> structure passed to the <a href="https://msdn.microsoft.com/ABCA52BA-FB5F-427A-9EFA-A7AA4E8D98A4">RIOCreateCompletionQueue</a> function when the <a href="https://msdn.microsoft.com/9196F8AF-3C48-445D-B2D5-E22A99759D92">RIO_CQ</a> is created. The completion of the <a href="https://msdn.microsoft.com/02264DAC-A3A1-4F7D-9728-17BE7F10E859">RIONotify</a> function for this <b>RIO_CQ</b> will signal the event.  The  <b>Event.NotifyReset</b> member in the <b>RIO_NOTIFICATION_COMPLETION</b> structure passed to the <b>RIOCreateCompletionQueue</b> function when the <b>RIO_CQ</b> is created indicates whether or not the event should be reset as part of a call to the <b>RIONotify</b> function.


### -field RIO_IOCP_COMPLETION

An I/O completion port handle is used to signal completion queue notifications.

An I/O completion port handle is provided as the <b>Iocp.IocpHandle</b> member in the <a href="https://msdn.microsoft.com/85D3D68F-A914-4126-8D3D-4A6E3F970A4B">RIO_NOTIFICATION_COMPLETION</a> structure passed to the <a href="https://msdn.microsoft.com/ABCA52BA-FB5F-427A-9EFA-A7AA4E8D98A4">RIOCreateCompletionQueue</a> function when the <a href="https://msdn.microsoft.com/9196F8AF-3C48-445D-B2D5-E22A99759D92">RIO_CQ</a> is created. The completion of the <a href="https://msdn.microsoft.com/02264DAC-A3A1-4F7D-9728-17BE7F10E859">RIONotify</a> function for this <b>RIO_CQ</b> will queue an entry to the I/O completion port which can be retrieved using the <a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a> or <a href="https://msdn.microsoft.com/3996c02c-562c-4697-a091-e241ad54b239">GetQueuedCompletionStatusEx</a> function.  The queued entry will have the returned <i>lpCompletionKey</i> parameter value set to the value specified in the <b>Iocp.CompletionKey</b> member of the <b>RIO_NOTIFICATION_COMPLETION</b> and the returned <i>lpOverlapped</i> parameter value set to the value specified in the <b>Iocp.Overlapped</b> member in <b>RIO_NOTIFICATION_COMPLETION</b> structure.  The <b>Iocp.Overlapped</b> member in the <b>RIO_NOTIFICATION_COMPLETION</b> will be a non-NULL value.


## -remarks



The <b>RIO_NOTIFICATION_COMPLETION_TYPE</b> enumeration is used with the Winsock registered I/O extensions to specify the type of I/O completion to use with a <a href="https://msdn.microsoft.com/9196F8AF-3C48-445D-B2D5-E22A99759D92">RIO_CQ</a>. An enumeration value is set in the <a href="https://msdn.microsoft.com/85D3D68F-A914-4126-8D3D-4A6E3F970A4B">RIO_NOTIFICATION_COMPLETION</a> structure passed to the <a href="https://msdn.microsoft.com/ABCA52BA-FB5F-427A-9EFA-A7AA4E8D98A4">RIOCreateCompletionQueue</a> function when the <b>RIO_CQ</b> is created. 

When creating a <a href="https://msdn.microsoft.com/9196F8AF-3C48-445D-B2D5-E22A99759D92">RIO_CQ</a>, the <a href="https://msdn.microsoft.com/85D3D68F-A914-4126-8D3D-4A6E3F970A4B">RIO_NOTIFICATION_COMPLETION</a> structure determines how the application will receive completion queue notifications.  If the <b>RIO_NOTIFICATION_COMPLETION</b> structure is provided when creating the completion queue, the application may call the <a href="https://msdn.microsoft.com/02264DAC-A3A1-4F7D-9728-17BE7F10E859">RIONotify</a> function to request a completion queue notification.  Normally this notification occurs when the completion queue is not empty.  This may happen immediately or when the next completion entry is inserted into the completion queue.  Once a completion queue notification is issued, the application must call <b>RIONotify</b> in order to receive another completion queue notification.

Two options are available for completion queue notification. <ul>
<li>Event handles.</li>
<li>I/O completion ports</li>
</ul>


If the <b>Type</b> member of the <a href="https://msdn.microsoft.com/85D3D68F-A914-4126-8D3D-4A6E3F970A4B">RIO_NOTIFICATION_COMPLETION</a> structure is set to <b>RIO_EVENT_COMPLETION</b>, an event handle is used to signal completion queue notifications. An event handle is provided as the <b>EventNotify.EventHandle</b> member in the <b>RIO_NOTIFICATION_COMPLETION</b> structure passed to the <a href="https://msdn.microsoft.com/ABCA52BA-FB5F-427A-9EFA-A7AA4E8D98A4">RIOCreateCompletionQueue</a> function. 

If the <b>Type</b> member of the <a href="https://msdn.microsoft.com/85D3D68F-A914-4126-8D3D-4A6E3F970A4B">RIO_NOTIFICATION_COMPLETION</a> structure is set to <b>RIO_IOCP_COMPLETION</b>,  an I/O completion port is used to signal completion queue notifications. An I/O completion port handle is provided as the <b>Iocp.IocpHandle</b> member in the <b>RIO_NOTIFICATION_COMPLETION</b> structure passed to the <a href="https://msdn.microsoft.com/ABCA52BA-FB5F-427A-9EFA-A7AA4E8D98A4">RIOCreateCompletionQueue</a> function. The completion of the <a href="https://msdn.microsoft.com/02264DAC-A3A1-4F7D-9728-17BE7F10E859">RIONotify</a> function for this <a href="https://msdn.microsoft.com/9196F8AF-3C48-445D-B2D5-E22A99759D92">RIO_CQ</a> will queue an entry to the I/O completion port which can be retrieved using the <a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a> or <a href="https://msdn.microsoft.com/3996c02c-562c-4697-a091-e241ad54b239">GetQueuedCompletionStatusEx</a> function.




## -see-also




<a href="https://msdn.microsoft.com/ABCA52BA-FB5F-427A-9EFA-A7AA4E8D98A4">RIOCreateCompletionQueue</a>



<a href="https://msdn.microsoft.com/02264DAC-A3A1-4F7D-9728-17BE7F10E859">RIONotify</a>



<a href="https://msdn.microsoft.com/9196F8AF-3C48-445D-B2D5-E22A99759D92">RIO_CQ</a>



<a href="https://msdn.microsoft.com/85D3D68F-A914-4126-8D3D-4A6E3F970A4B">RIO_NOTIFICATION_COMPLETION</a>
 

 

