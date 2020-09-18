---
UID: NF:fltuser.FilterSendMessage
title: FilterSendMessage function (fltuser.h)
description: The FilterSendMessage function sends a message to a kernel-mode minifilter.
helpviewer_keywords: ["FilterSendMessage","FilterSendMessage function [Installable File System Drivers]","FltWin32ApiRef_7d1d856f-6ed8-4c55-8524-05d99ab7d626.xml","fltuser/FilterSendMessage","ifsk.filtersendmessage"]
old-location: ifsk\filtersendmessage.htm
tech.root: ifsk
ms.assetid: e0a5d790-280d-43ff-a170-14b28b3da02a
ms.date: 12/05/2018
ms.keywords: FilterSendMessage, FilterSendMessage function [Installable File System Drivers], FltWin32ApiRef_7d1d856f-6ed8-4c55-8524-05d99ab7d626.xml, fltuser/FilterSendMessage, ifsk.filtersendmessage
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FilterSendMessage
 - fltuser/FilterSendMessage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FltLib.dll
api_name:
 - FilterSendMessage
---

# FilterSendMessage function


## -description

The <b>FilterSendMessage</b> function sends a message to a kernel-mode minifilter.

## -parameters

### -param hPort [in]

Communication port handle returned by a previous call to <a href="/windows/desktop/api/fltuser/nf-fltuser-filterconnectcommunicationport">FilterConnectCommunicationPort</a>. This parameter is required and cannot be <b>NULL</b>.

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

The <b>FilterSendMessage</b> function sends a message to a minifilter. The message is passed to the minifilter's message notification callback routine, which processes the message. (The minifilter registers its message callback notification routine by passing it as the <i>MessageNotifyCallback</i> parameter to <a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltcreatecommunicationport">FltCreateCommunicationPort</a>.) 

<b>FilterSendMessage</b> is synchronous. The caller is put into a wait state until the message is delivered and the minifilter's reply (if any) is received. 

If the caller expects a reply, it must pass a non-<b>NULL</b> buffer for the <i>lpOutBuffer</i> parameter and a positive value for the <i>dwOutBufferSize</i> parameter. 

To get a message from a minifilter, call <a href="/windows/desktop/api/fltuser/nf-fltuser-filtergetmessage">FilterGetMessage</a>. 

To reply to a message from a minifilter, call <a href="/windows/desktop/api/fltuser/nf-fltuser-filterreplymessage">FilterReplyMessage</a>. 

A minifilter sends a message to a user-mode application by calling <a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltsendmessage">FltSendMessage</a>.

## -see-also

<a href="/windows/desktop/api/fltuser/nf-fltuser-filterconnectcommunicationport">FilterConnectCommunicationPort</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filtergetmessage">FilterGetMessage</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filterreplymessage">FilterReplyMessage</a>



<a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltcreatecommunicationport">FltCreateCommunicationPort</a>



<a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltsendmessage">FltSendMessage</a>