---
UID: NF:rdpencomapi.IRDPViewerInputSink.SendMouseButtonEvent
title: IRDPViewerInputSink::SendMouseButtonEvent (rdpencomapi.h)
description: Sends a mouse button event message.
helpviewer_keywords: ["IRDPViewerInputSink interface [RDP]","SendMouseButtonEvent method","IRDPViewerInputSink.SendMouseButtonEvent","IRDPViewerInputSink::SendMouseButtonEvent","SendMouseButtonEvent","SendMouseButtonEvent method [RDP]","SendMouseButtonEvent method [RDP]","IRDPViewerInputSink interface","rdp.irdpviewerinputsink_sendmousebuttonevent","rdpencomapi/IRDPViewerInputSink::SendMouseButtonEvent"]
old-location: rdp\irdpviewerinputsink_sendmousebuttonevent.htm
tech.root: rdp
ms.assetid: 2BC93D69-7DBC-4C38-9980-EEB9775A083E
ms.date: 12/05/2018
ms.keywords: IRDPViewerInputSink interface [RDP],SendMouseButtonEvent method, IRDPViewerInputSink.SendMouseButtonEvent, IRDPViewerInputSink::SendMouseButtonEvent, SendMouseButtonEvent, SendMouseButtonEvent method [RDP], SendMouseButtonEvent method [RDP],IRDPViewerInputSink interface, rdp.irdpviewerinputsink_sendmousebuttonevent, rdpencomapi/IRDPViewerInputSink::SendMouseButtonEvent
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
 - IRDPViewerInputSink::SendMouseButtonEvent
 - rdpencomapi/IRDPViewerInputSink::SendMouseButtonEvent
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
 - IRDPViewerInputSink.SendMouseButtonEvent
---

# IRDPViewerInputSink::SendMouseButtonEvent


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpviewerinputsink">IRDPViewerInputSink</a> interface is no longer available for use for UWP applications as of Windows 10, version 1709. It is still supported for Desktop apps.]

Sends a mouse button event message.

## -parameters

### -param buttonType [in]

The button that is pressed or released.

### -param vbButtonDown [in]

The button state:  <b>TRUE</b> if the button is down and <b>FALSE</b> otherwise.

### -param xPos [in]

The mouse position in  pixels along the horizontal axis.

### -param yPos [in]

The mouse position in pixels along the vertical axis.

## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpviewerinputsink">IRDPViewerInputSink</a>