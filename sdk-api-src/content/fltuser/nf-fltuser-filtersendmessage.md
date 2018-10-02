---
UID: NF:fltuser.FilterSendMessage
title: FilterSendMessage function
author: windows-sdk-content
description: The FilterSendMessage function sends a message to a kernel-mode minifilter.
old-location: ifsk\filtersendmessage.htm
tech.root: ifsk
ms.assetid: e0a5d790-280d-43ff-a170-14b28b3da02a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FilterSendMessage, FilterSendMessage function [Installable File System Drivers], FltWin32ApiRef_7d1d856f-6ed8-4c55-8524-05d99ab7d626.xml, fltuser/FilterSendMessage, ifsk.filtersendmessage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: fltuser.h
req.include-header: Fltuser.h
req.target-type: Universal
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
req.lib: FltLib.lib
req.dll: FltLib.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FltLib.dll
api_name:
 - FilterSendMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FilterSendMessage function


## -description


The <b>FilterSendMessage</b> function sends a message to a kernel-mode minifilter. 


## -parameters




### -param hPort [in]

Communication port handle returned by a previous call to <a href="https://msdn.microsoft.com/294783f2-2cbf-4eea-82ae-a396c62f911a">FilterConnectCommunicationPort</a>. This parameter is required and cannot be <b>NULL</b>. 


### -param lpInBuffer [in, optional]

Pointer to a caller-allocated buffer containing the message to be sent to the minifilter. The message format is caller-defined. This parameter is required and cannot be <b>NULL</b>.


### -param dwInBufferSize [in]

Size, in bytes, of the buffer pointed to by <i>lpInBuffer</i>.


### -param lpOutBuffer [out]

Pointer to a caller-allocated buffer that receives the reply (if any) from the minifilter. 


### -param dwOutBufferSize [in]

Size, in bytes, of the buffer pointed to by <i>lpOutBuffer</i>. This value is ignored if <i>lpOutBuffer</i> is <b>NULL</b>. 


### -param lpBytesReturned [out]

Pointer to a caller-allocated variable that receives the number of bytes returned in the buffer that <i>lpOutBuffer</i> points to if the call to <b>FilterSendMessage</b> succeeds. This parameter is required and cannot be <b>NULL</b>. 


## -returns



<b>FilterSendMessage</b> returns S_OK if successful. Otherwise, it returns an error value. 




## -remarks



The <b>FilterSendMessage</b> function sends a message to a minifilter. The message is passed to the minifilter's message notification callback routine, which processes the message. (The minifilter registers its message callback notification routine by passing it as the <i>MessageNotifyCallback</i> parameter to <a href="https://msdn.microsoft.com/9987ed6b-7792-4035-9640-9ee9595e854a">FltCreateCommunicationPort</a>.) 

<b>FilterSendMessage</b> is synchronous. The caller is put into a wait state until the message is delivered and the minifilter's reply (if any) is received. 

If the caller expects a reply, it must pass a non-<b>NULL</b> buffer for the <i>lpOutBuffer</i> parameter and a positive value for the <i>dwOutBufferSize</i> parameter. 

To get a message from a minifilter, call <a href="https://msdn.microsoft.com/2738e237-835c-471f-9129-26c4da5fe839">FilterGetMessage</a>. 

To reply to a message from a minifilter, call <a href="https://msdn.microsoft.com/e0a0033c-2ea8-4e5b-bcae-680247ea6157">FilterReplyMessage</a>. 

A minifilter sends a message to a user-mode application by calling <a href="https://msdn.microsoft.com/83e8389f-1960-4fe0-9a33-526311ecba82">FltSendMessage</a>. 




## -see-also




<a href="https://msdn.microsoft.com/294783f2-2cbf-4eea-82ae-a396c62f911a">FilterConnectCommunicationPort</a>



<a href="https://msdn.microsoft.com/2738e237-835c-471f-9129-26c4da5fe839">FilterGetMessage</a>



<a href="https://msdn.microsoft.com/e0a0033c-2ea8-4e5b-bcae-680247ea6157">FilterReplyMessage</a>



<a href="https://msdn.microsoft.com/9987ed6b-7792-4035-9640-9ee9595e854a">FltCreateCommunicationPort</a>



<a href="https://msdn.microsoft.com/83e8389f-1960-4fe0-9a33-526311ecba82">FltSendMessage</a>
 

 

