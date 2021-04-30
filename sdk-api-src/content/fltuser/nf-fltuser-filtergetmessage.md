---
UID: NF:fltuser.FilterGetMessage
title: FilterGetMessage function (fltuser.h)
description: The FilterGetMessage function gets a message from a kernel-mode minifilter.
helpviewer_keywords: ["FilterGetMessage","FilterGetMessage function [Installable File System Drivers]","FltWin32ApiRef_2a4730dd-cee5-4a3e-b904-c19683fc314a.xml","fltuser/FilterGetMessage","ifsk.filtergetmessage"]
old-location: ifsk\filtergetmessage.htm
tech.root: ifsk
ms.assetid: 2738e237-835c-471f-9129-26c4da5fe839
ms.date: 12/05/2018
ms.keywords: FilterGetMessage, FilterGetMessage function [Installable File System Drivers], FltWin32ApiRef_2a4730dd-cee5-4a3e-b904-c19683fc314a.xml, fltuser/FilterGetMessage, ifsk.filtergetmessage
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
 - FilterGetMessage
 - fltuser/FilterGetMessage
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
 - FilterGetMessage
---

# FilterGetMessage function


## -description

The <b>FilterGetMessage</b> function gets a message from a kernel-mode minifilter.

## -parameters

### -param hPort [in]

Communication port handle returned by a previous call to <a href="/windows/desktop/api/fltuser/nf-fltuser-filterconnectcommunicationport">FilterConnectCommunicationPort</a>. This parameter is required and cannot be <b>NULL</b>.

### -param lpMessageBuffer [out]

Pointer to a caller-allocated buffer that receives the message from the minifilter. The message must contain a <a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_filter_message_header">FILTER_MESSAGE_HEADER</a> structure, but otherwise its format is caller-defined. This parameter is required and cannot be <b>NULL</b>.

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

After receiving the message from the minifilter, the caller can send a reply by calling <a href="/windows/desktop/api/fltuser/nf-fltuser-filterreplymessage">FilterReplyMessage</a>. 

A minifilter or instance sends a message to a user-mode application by calling <a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltsendmessage">FltSendMessage</a>.

## -see-also

<a href="/windows/win32/api/synchapi/nf-synchapi-createeventa">CreateEvent</a>



<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_filter_message_header">FILTER_MESSAGE_HEADER</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filterconnectcommunicationport">FilterConnectCommunicationPort</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filterreplymessage">FilterReplyMessage</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filtersendmessage">FilterSendMessage</a>



<a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltsendmessage">FltSendMessage</a>



<a href="/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>



<a href="/windows/win32/api/winbase/nf-winbase-hasoverlappediocompleted">HasOverlappedIoCompleted</a>