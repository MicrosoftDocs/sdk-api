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

# _COMSTAT structure


## -description


Contains information about a communications device. This structure is filled by the 
<a href="https://msdn.microsoft.com/9cc52104-aa5e-4baa-86f1-8c6dcdd661ef">ClearCommError</a> function.


## -struct-fields




### -field fCtsHold

If this member is <b>TRUE</b>, transmission is waiting for the CTS (clear-to-send) signal to be sent.


### -field fDsrHold

If this member is <b>TRUE</b>, transmission is waiting for the DSR (data-set-ready) signal to be sent.


### -field fRlsdHold

If this member is <b>TRUE</b>, transmission is waiting for the RLSD (receive-line-signal-detect) signal to be sent.


### -field fXoffHold

If this member is <b>TRUE</b>, transmission is waiting because the XOFF character was received.


### -field fXoffSent

If this member is <b>TRUE</b>, transmission is waiting because the XOFF character was transmitted. (Transmission halts when the XOFF character is transmitted to a system that takes the next character as XON, regardless of the actual character.)


### -field fEof

If this member is <b>TRUE</b>, the end-of-file (EOF) character has been received.


### -field fTxim

If this member is <b>TRUE</b>, there is a character queued for transmission that has come to the communications device by way of the 
<a href="https://msdn.microsoft.com/599c3d04-6cd3-41ac-88a8-752f4b83d46b">TransmitCommChar</a> function. The communications device transmits such a character ahead of other characters in the device's output buffer.


### -field fReserved

Reserved; do not use.


### -field cbInQue

The number of bytes received by the serial provider but not yet read by a 
<a href="https://msdn.microsoft.com/4ad4580d-c002-44a4-a5f6-757e83ed8732">ReadFile</a> operation.


### -field cbOutQue

The number of bytes of user data remaining to be transmitted for all write operations. This value will be zero for a nonoverlapped write.


## -see-also




<a href="https://msdn.microsoft.com/9cc52104-aa5e-4baa-86f1-8c6dcdd661ef">ClearCommError</a>



<a href="https://msdn.microsoft.com/4ad4580d-c002-44a4-a5f6-757e83ed8732">ReadFile</a>



<a href="https://msdn.microsoft.com/599c3d04-6cd3-41ac-88a8-752f4b83d46b">TransmitCommChar</a>
 

 

