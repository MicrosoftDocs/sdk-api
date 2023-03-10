---
UID: NF:fltuser.FilterReplyMessage
title: FilterReplyMessage function (fltuser.h)
description: The FilterReplyMessage function replies to a message from a kernel-mode minifilter.
helpviewer_keywords: ["FilterReplyMessage","FilterReplyMessage function [Installable File System Drivers]","FltWin32ApiRef_f89f529e-8396-4f15-ae63-6497c92aab1a.xml","fltuser/FilterReplyMessage","ifsk.filterreplymessage"]
old-location: ifsk\filterreplymessage.htm
tech.root: ifsk
ms.assetid: e0a0033c-2ea8-4e5b-bcae-680247ea6157
ms.date: 12/05/2018
ms.keywords: FilterReplyMessage, FilterReplyMessage function [Installable File System Drivers], FltWin32ApiRef_f89f529e-8396-4f15-ae63-6497c92aab1a.xml, fltuser/FilterReplyMessage, ifsk.filterreplymessage
req.header: fltuser.h
req.include-header: FltUser.h
req.target-type: Universal
req.target-min-winverclnt: Available in Microsoft Windows 2000 Update Rollup 1 for SP4, Windows XP SP2, Windows Server 2003 SP1, and later operating systems. Not available in Windows 2000 SP4 and earlier operating systems.
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
 - FilterReplyMessage
 - fltuser/FilterReplyMessage
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
 - FilterReplyMessage
---

# FilterReplyMessage function


## -description

The <b>FilterReplyMessage</b> function replies to a message from a kernel-mode minifilter.

## -parameters

### -param hPort [in]

Communication port handle returned by a previous call to <a href="/windows/desktop/api/fltuser/nf-fltuser-filterconnectcommunicationport">FilterConnectCommunicationPort</a>. This parameter is required and cannot be <b>NULL</b>.

### -param lpReplyBuffer [in]

A pointer to a caller-allocated buffer containing the reply to be sent to the minifilter. The reply must contain a <a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_filter_reply_header">FILTER_REPLY_HEADER</a> structure, but otherwise, its format is caller-defined. This parameter is required and cannot be <b>NULL</b>.

### -param dwReplyBufferSize [in]

Size, in bytes, of the buffer that the <i>lpReplyBuffer</i> parameter points to. See the Remarks section.

## -returns

<b>FilterReplyMessage</b> returns S_OK if successful. Otherwise, it returns an error value.

## -remarks

A user-mode application calls the <b>FilterReplyMessage</b> function to reply to a message received from a kernel-mode minifilter. 

To get a message from a minifilter, call <a href="/windows/desktop/api/fltuser/nf-fltuser-filtergetmessage">FilterGetMessage</a>. 

To send a message to a minifilter, call <a href="/windows/desktop/api/fltuser/nf-fltuser-filtersendmessage">FilterSendMessage</a>. 

A minifilter sends a message to a user-mode application by calling <a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltsendmessage">FltSendMessage</a>. 

<div class="alert"><b>Important</b>  <p class="note">Due to (system-specific) structure <a href="/windows-hardware/drivers/">padding</a> requirements, accuracy is required when you set the size of buffers that are associated with <a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltsendmessage">FltSendMessage</a> and <b>FilterReplyMessage</b>. As an example, assume data must be sent (via <b>FilterReplyMessage</b>) to a minifilter.  The user-mode component might declare the following structure to do so:


```cpp
typedef struct _REPLY_STRUCT
{
     FILTER_REPLY_HEADER Header;
     MY_STRUCTURE Data;  // The structure to be sent to the minifilter.
} REPLY_STRUCT, *PREPLY_STRUCT;
```


<p class="note">Given this structure, it might seem obvious that the caller of <b>FilterReplyMessage</b> would set the <i>dwReplyBufferSize</i> parameter to <code>sizeof(REPLY_STRUCT)</code> and the <i>ReplyLength</i> parameter of <a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltsendmessage">FltSendMessage</a> to the same value.  However, because of structure padding idiosyncrasies, <code>sizeof(REPLY_STRUCT)</code> might be larger than <code>sizeof(FILTER_REPLY_HEADER) + sizeof(MY_STRUCT)</code>.  If this is the case, <b>FltSendMessage</b> returns STATUS_BUFFER_OVERFLOW.

<p class="note">Therefore, we recommend that you call <b>FilterReplyMessage</b> and <a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltsendmessage">FltSendMessage</a> (leveraging the above example) by setting <i>dwReplyBufferSize</i> and <i>ReplyLength</i> both to <code>sizeof(FILTER_REPLY_HEADER) + sizeof(MY_STRUCT)</code> instead of <code>sizeof(REPLY_STRUCT)</code>. This ensures that any extra padding at the end of the <b>REPLY_STRUCT</b> structure is ignored.

</div>
<div> </div>

## -see-also

<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_filter_reply_header">FILTER_REPLY_HEADER</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filterconnectcommunicationport">FilterConnectCommunicationPort</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filtergetmessage">FilterGetMessage</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filtersendmessage">FilterSendMessage</a>



<a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltsendmessage">FltSendMessage</a>