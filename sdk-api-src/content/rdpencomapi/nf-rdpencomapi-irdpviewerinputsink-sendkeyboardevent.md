---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

