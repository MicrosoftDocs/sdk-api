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

# FilterGetMessage function


## -description


The <b>FilterGetMessage</b> function gets a message from a kernel-mode minifilter. 


## -parameters




### -param hPort [in]

Communication port handle returned by a previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff540460">FilterConnectCommunicationPort</a>. This parameter is required and cannot be <b>NULL</b>. 


### -param lpMessageBuffer [out]

Pointer to a caller-allocated buffer that receives the message from the minifilter. The message must contain a <a href="https://msdn.microsoft.com/library/windows/hardware/ff541621">FILTER_MESSAGE_HEADER</a> structure, but otherwise its format is caller-defined. This parameter is required and cannot be <b>NULL</b>. 


### -param dwMessageBufferSize [in]

Size, in bytes, of the buffer that the <i>lpMessageBuffer</i> parameter points to. 


### -param lpOverlapped [in, out]

Pointer to an OVERLAPPED structure. This parameter is optional and can be <b>NULL</b>. If it is not <b>NULL</b>, the caller must initialize the <b>hEvent</b> member of the OVERLAPPED structure to a valid event handle or <b>NULL</b>. 


## -returns



<b>FilterGetMessage</b> returns S_OK if successful. Otherwise, it returns an error value. 




## -remarks



The <b>FilterGetMessage</b> function is designed for both synchronous and asynchronous (overlapped) operation. 

When <i>lpOverlapped</i> is <b>NULL</b>, and a message is available, <b>FilterGetMessage</b>  returns immediately. Otherwise, the caller is put into a wait state until a message is received.

If <i>lpOverlapped</i> is not <b>NULL</b>, <b>FilterGetMessage</b> returns ERROR_IO_PENDING. In this situation, the event object in the <i>lpOverlapped</i> structure is set to the nonsignaled state before <b>FilterGetMessage</b> returns. When the message is delivered, this event is set to the signaled state.

After receiving the message from the minifilter, the caller can send a reply by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff541508">FilterReplyMessage</a>. 

A minifilter or instance sends a message to a user-mode application by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff544378">FltSendMessage</a>.  




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=139082">CreateEvent</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541621">FILTER_MESSAGE_HEADER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540460">FilterConnectCommunicationPort</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541508">FilterReplyMessage</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541513">FilterSendMessage</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544378">FltSendMessage</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=139083">GetOverlappedResult</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=139084">HasOverlappedIoCompleted</a>
 

 

