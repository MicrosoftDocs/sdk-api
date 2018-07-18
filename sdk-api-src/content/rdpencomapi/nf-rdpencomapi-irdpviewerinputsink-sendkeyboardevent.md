---
UID: NF:rdpencomapi.IRDPViewerInputSink.SendKeyboardEvent
title: IRDPViewerInputSink::SendKeyboardEvent
author: windows-sdk-content
description: Sends a keyboard event message.
old-location: rdp\irdpviewerinputsink_sendkeyboardevent.htm
old-project: rdp
ms.assetid: 28EDA0AD-9669-4232-BD41-4ADEC90CA3A7
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IRDPViewerInputSink interface [RDP],SendKeyboardEvent method, IRDPViewerInputSink.SendKeyboardEvent, IRDPViewerInputSink::SendKeyboardEvent, SendKeyboardEvent, SendKeyboardEvent method [RDP], SendKeyboardEvent method [RDP],IRDPViewerInputSink interface, rdp.irdpviewerinputsink_sendkeyboardevent, rdpencomapi/IRDPViewerInputSink::SendKeyboardEvent
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: RDPENCOMAPI_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPViewerInputSink.SendKeyboardEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
req.product: ADAM
---

# IRDPViewerInputSink::SendKeyboardEvent


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/364EC709-C41C-4ADD-8E7D-6A635E5BCCDA">IRDPViewerInputSink</a> interface is no longer available for use for UWP applications as of Windows 10, version 1709. It is still supported for Desktop apps.]

Sends a keyboard event message.


## -parameters




### -param codeType

The encoding of the key code.


### -param keycode

The key code of the pressed or released key.


### -param vbKeyUp

The state of the key:  <b>TRUE</b> if the key is released, <b>FALSE</b> if the key is pressed.


### -param vbRepeat

The key code is a repeated code:  <b>FALSE</b> if this is the initial key code from a key press, <b>TRUE</b> if this is repeated code from a single key press.


### -param vbExtended

The key code is extended:  <b>TRUE</b> if the code is extended, <b>FALSE</b> otherwise.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.




## -see-also




<a href="https://msdn.microsoft.com/364EC709-C41C-4ADD-8E7D-6A635E5BCCDA">IRDPViewerInputSink</a>
 

 

