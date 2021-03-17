---
UID: NF:rdpencomapi.IRDPViewerInputSink.SendMouseWheelEvent
title: IRDPViewerInputSink::SendMouseWheelEvent (rdpencomapi.h)
description: Sends a mouse wheel event message.
helpviewer_keywords: ["IRDPViewerInputSink interface [RDP]","SendMouseWheelEvent method","IRDPViewerInputSink.SendMouseWheelEvent","IRDPViewerInputSink::SendMouseWheelEvent","SendMouseWheelEvent","SendMouseWheelEvent method [RDP]","SendMouseWheelEvent method [RDP]","IRDPViewerInputSink interface","rdp.irdpviewerinputsink_sendmousewheelevent","rdpencomapi/IRDPViewerInputSink::SendMouseWheelEvent"]
old-location: rdp\irdpviewerinputsink_sendmousewheelevent.htm
tech.root: rdp
ms.assetid: CEC54C27-F49E-4B41-A18D-69F0414955A1
ms.date: 12/05/2018
ms.keywords: IRDPViewerInputSink interface [RDP],SendMouseWheelEvent method, IRDPViewerInputSink.SendMouseWheelEvent, IRDPViewerInputSink::SendMouseWheelEvent, SendMouseWheelEvent, SendMouseWheelEvent method [RDP], SendMouseWheelEvent method [RDP],IRDPViewerInputSink interface, rdp.irdpviewerinputsink_sendmousewheelevent, rdpencomapi/IRDPViewerInputSink::SendMouseWheelEvent
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
 - IRDPViewerInputSink::SendMouseWheelEvent
 - rdpencomapi/IRDPViewerInputSink::SendMouseWheelEvent
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
 - IRDPViewerInputSink.SendMouseWheelEvent
---

# IRDPViewerInputSink::SendMouseWheelEvent


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpviewerinputsink">IRDPViewerInputSink</a> interface is no longer available for use for UWP applications as of Windows 10, version 1709. It is still supported for Desktop apps.]

Sends a mouse wheel event message.

## -parameters

### -param wheelRotation

The number of increments that the wheel is moved.

## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpviewerinputsink">IRDPViewerInputSink</a>