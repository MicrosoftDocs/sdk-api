---
UID: NF:vswriter.CVssWriterEx.SubscribeEx
title: CVssWriterEx::SubscribeEx (vswriter.h)
description: Causes the writer to subscribe to VSS events.
helpviewer_keywords: ["CVssWriterEx interface","SubscribeEx method","CVssWriterEx.SubscribeEx","CVssWriterEx::SubscribeEx","SubscribeEx","SubscribeEx method","SubscribeEx method","CVssWriterEx interface","base.cvsswriterex_subscribeex","vswriter/CVssWriterEx::SubscribeEx"]
old-location: base\cvsswriterex_subscribeex.htm
tech.root: base
ms.assetid: b60ca619-c92b-4700-a048-7c74fad3d0e9
ms.date: 12/05/2018
ms.keywords: CVssWriterEx interface,SubscribeEx method, CVssWriterEx.SubscribeEx, CVssWriterEx::SubscribeEx, SubscribeEx, SubscribeEx method, SubscribeEx method,CVssWriterEx interface, base.cvsswriterex_subscribeex, vswriter/CVssWriterEx::SubscribeEx
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CVssWriterEx::SubscribeEx
 - vswriter/CVssWriterEx::SubscribeEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - CVssWriterEx.SubscribeEx
---

# CVssWriterEx::SubscribeEx


## -description

Causes the writer to subscribe to VSS events.

## -parameters

### -param dwUnsubscribeTimeout [in]

The length of time, in milliseconds, that the method will wait before timing out.

### -param dwEventFlags [in]

A bitmask of 
<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_subscribe_mask">VSS_SUBSCRIBE_MASK</a> values indicating the events that VSS should notify the writer about. 




The default value for this argument is (<b>VSS_SM_BACKUP_EVENTS_FLAG</b> | <b>VSS_SM_RESTORE_EVENTS_FLAG</b>). Currently, the caller should not override the default value.

This parameter is reserved for future use.

## -returns

The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The writer has successfully subscribed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient backup privileges or is not an administrator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error. The error code is logged in the error log file. For more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_WRITER_ALREADY_SUBSCRIBED</b></dt>
</dl>
</td>
<td width="60%">
The writer has previously called this method.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-subscribe">CVssWriter::Subscribe</a>



<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriterex">CVssWriterEx</a>