---
UID: NF:rdpencomapi.IRDPViewerInputSink.SendSyncEvent
title: IRDPViewerInputSink::SendSyncEvent
author: windows-sdk-content
description: Sends an event message to indicate a change in the state of the keyboard, such as when the Caps Lock key is pressed.
old-location: rdp\irdpviewerinputsink_sendsyncevent.htm
tech.root: Rdp
ms.assetid: C8B59CAF-DFBE-4569-99B2-DECF1F1DBB56
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IRDPViewerInputSink interface [RDP],SendSyncEvent method, IRDPViewerInputSink.SendSyncEvent, IRDPViewerInputSink::SendSyncEvent, SendSyncEvent, SendSyncEvent method [RDP], SendSyncEvent method [RDP],IRDPViewerInputSink interface, rdp.irdpviewerinputsink_sendsyncevent, rdpencomapi/IRDPViewerInputSink::SendSyncEvent
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
 - IRDPViewerInputSink.SendSyncEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRDPViewerInputSink::SendSyncEvent


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/364EC709-C41C-4ADD-8E7D-6A635E5BCCDA">IRDPViewerInputSink</a> interface is no longer available for use for UWP applications as of Windows 10, version 1709. It is still supported for Desktop apps.]

Sends an event message to indicate a change in the state of the keyboard, such as when the Caps Lock key is pressed.


## -parameters




### -param syncFlags

For possible values, see the <a href="https://msdn.microsoft.com/0E16C482-E7D7-4477-B5B2-830D8CD9012A">RDPSRAPI_KBD_SYNC_FLAG</a> enumeration.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.




## -see-also




<a href="https://msdn.microsoft.com/364EC709-C41C-4ADD-8E7D-6A635E5BCCDA">IRDPViewerInputSink</a>
 

 

