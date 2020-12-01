---
UID: NF:rdpencomapi.IRDPViewerInputSink.SendMouseMoveEvent
title: IRDPViewerInputSink::SendMouseMoveEvent (rdpencomapi.h)
description: Sends a mouse move event message.
helpviewer_keywords: ["IRDPViewerInputSink interface [RDP]","SendMouseMoveEvent method","IRDPViewerInputSink.SendMouseMoveEvent","IRDPViewerInputSink::SendMouseMoveEvent","SendMouseMoveEvent","SendMouseMoveEvent method [RDP]","SendMouseMoveEvent method [RDP]","IRDPViewerInputSink interface","rdp.irdpviewerinputsink_sendmousemoveevent","rdpencomapi/IRDPViewerInputSink::SendMouseMoveEvent"]
old-location: rdp\irdpviewerinputsink_sendmousemoveevent.htm
tech.root: rdp
ms.assetid: 0888E762-A0B3-48EA-B928-42E3E801AF15
ms.date: 12/05/2018
ms.keywords: IRDPViewerInputSink interface [RDP],SendMouseMoveEvent method, IRDPViewerInputSink.SendMouseMoveEvent, IRDPViewerInputSink::SendMouseMoveEvent, SendMouseMoveEvent, SendMouseMoveEvent method [RDP], SendMouseMoveEvent method [RDP],IRDPViewerInputSink interface, rdp.irdpviewerinputsink_sendmousemoveevent, rdpencomapi/IRDPViewerInputSink::SendMouseMoveEvent
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
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRDPViewerInputSink::SendMouseMoveEvent
 - rdpencomapi/IRDPViewerInputSink::SendMouseMoveEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPViewerInputSink.SendMouseMoveEvent
---

# IRDPViewerInputSink::SendMouseMoveEvent


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpviewerinputsink">IRDPViewerInputSink</a> interface is no longer available for use for UWP applications as of Windows 10, version 1709. It is still supported for Desktop apps.]

Sends a mouse move event message.

## -parameters

### -param xPos [in]

The mouse position in  pixels along the horizontal axis.

### -param yPos [in]

The mouse position in pixels along the vertical axis.

## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpviewerinputsink">IRDPViewerInputSink</a>