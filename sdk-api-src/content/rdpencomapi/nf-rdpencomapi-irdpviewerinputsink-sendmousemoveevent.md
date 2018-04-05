---
UID: NF:rdpencomapi.IRDPViewerInputSink.SendMouseMoveEvent
title: IRDPViewerInputSink::SendMouseMoveEvent method
author: windows-driver-content
description: Sends a mouse move event message.
old-location: rdp\irdpviewerinputsink_sendmousemoveevent.htm
old-project: Rdp
ms.assetid: 0888E762-A0B3-48EA-B928-42E3E801AF15
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: IRDPViewerInputSink, IRDPViewerInputSink interface [RDP], SendMouseMoveEvent method, IRDPViewerInputSink::SendMouseMoveEvent, SendMouseMoveEvent method [RDP], SendMouseMoveEvent method [RDP], IRDPViewerInputSink interface, SendMouseMoveEvent,IRDPViewerInputSink.SendMouseMoveEvent, rdp.irdpviewerinputsink_sendmousemoveevent, rdpencomapi/IRDPViewerInputSink::SendMouseMoveEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
req.typenames: RDPENCOMAPI_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	RdpEncom.dll
api_name:
-	IRDPViewerInputSink.SendMouseMoveEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IRDPViewerInputSink::SendMouseMoveEvent method


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/364EC709-C41C-4ADD-8E7D-6A635E5BCCDA">IRDPViewerInputSink</a> interface is no longer available for use for UWP applications as of Windows 10, version 1709. It is still supported for Desktop apps.]

Sends a mouse move event message.


## -parameters




### -param xPos [in]

The mouse position in  pixels along the horizontal axis.


### -param yPos [in]

The mouse position in pixels along the vertical axis.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.




## -see-also




<a href="https://msdn.microsoft.com/364EC709-C41C-4ADD-8E7D-6A635E5BCCDA">IRDPViewerInputSink</a>
 

 

