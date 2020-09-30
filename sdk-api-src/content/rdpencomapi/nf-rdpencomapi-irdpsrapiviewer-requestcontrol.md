---
UID: NF:rdpencomapi.IRDPSRAPIViewer.RequestControl
title: IRDPSRAPIViewer::RequestControl (rdpencomapi.h)
description: Requests the sharer to change the control level of the viewer.
helpviewer_keywords: ["IRDPSRAPIViewer interface [RDP]","RequestControl method","IRDPSRAPIViewer.RequestControl","IRDPSRAPIViewer::RequestControl","RequestControl","RequestControl method [RDP]","RequestControl method [RDP]","IRDPSRAPIViewer interface","rdp.irdpsrapiviewer_requestcontrol","rdpencomapi/IRDPSRAPIViewer::RequestControl"]
old-location: rdp\irdpsrapiviewer_requestcontrol.htm
tech.root: rdp
ms.assetid: be913f3c-9a5b-46bd-be9a-1ba0b0c20211
ms.date: 12/05/2018
ms.keywords: IRDPSRAPIViewer interface [RDP],RequestControl method, IRDPSRAPIViewer.RequestControl, IRDPSRAPIViewer::RequestControl, RequestControl, RequestControl method [RDP], RequestControl method [RDP],IRDPSRAPIViewer interface, rdp.irdpsrapiviewer_requestcontrol, rdpencomapi/IRDPSRAPIViewer::RequestControl
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IRDPSRAPIViewer::RequestControl
 - rdpencomapi/IRDPSRAPIViewer::RequestControl
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
 - IRDPSRAPIViewer.RequestControl
---

# IRDPSRAPIViewer::RequestControl


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiviewer">IRDPSRAPIViewer</a> interface is no longer available for use for UWP applications as of Windows 10, version 1709. It is still supported for Desktop apps.]

Requests the sharer to change the control level of the viewer. After this method is called, a message is sent to the sharer to notify the sharer that a viewer is requesting a control level change. After the sharer receives the message, an event is raised on the sharer side to notify the application that an attendee is requesting a change in control level. The application or user can then decide whether to allow the requested level of control for an attendee.

## -parameters

### -param CtrlLevel [in]

Type: <b>CTRL_LEVEL</b>

One of the values of the <a href="/windows/win32/api/rdpencomapi/ne-rdpencomapi-ctrl_level">CTRL_LEVEL</a> enumeration.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiviewer">IRDPSRAPIViewer</a>