---
UID: NF:rdpencomapi.IRDPSRAPIViewer.RequestControl
title: IRDPSRAPIViewer::RequestControl
author: windows-sdk-content
description: Requests the sharer to change the control level of the viewer.
old-location: rdp\irdpsrapiviewer_requestcontrol.htm
tech.root: rdp
ms.assetid: be913f3c-9a5b-46bd-be9a-1ba0b0c20211
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IRDPSRAPIViewer interface [RDP],RequestControl method, IRDPSRAPIViewer.RequestControl, IRDPSRAPIViewer::RequestControl, RequestControl, RequestControl method [RDP], RequestControl method [RDP],IRDPSRAPIViewer interface, rdp.irdpsrapiviewer_requestcontrol, rdpencomapi/IRDPSRAPIViewer::RequestControl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPIViewer.RequestControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRDPSRAPIViewer::RequestControl


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/6bafe380-2ef4-4e93-a6cd-143798437615">IRDPSRAPIViewer</a> interface is no longer available for use for UWP applications as of Windows 10, version 1709. It is still supported for Desktop apps.]

Requests the sharer to change the control level of the viewer. After this method is called, a message is sent to the sharer to notify the sharer that a viewer is requesting a control level change. After the sharer receives the message, an event is raised on the sharer side to notify the application that an attendee is requesting a change in control level. The application or user can then decide whether to allow the requested level of control for an attendee.


## -parameters




### -param CtrlLevel [in]

Type: <b>CTRL_LEVEL</b>

One of the values of the <a href="https://msdn.microsoft.com/f97b0493-82bf-487e-adc1-2dc40eeeb36c">CTRL_LEVEL</a> enumeration.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.




## -see-also




<a href="https://msdn.microsoft.com/6bafe380-2ef4-4e93-a6cd-143798437615">IRDPSRAPIViewer</a>
 

 

