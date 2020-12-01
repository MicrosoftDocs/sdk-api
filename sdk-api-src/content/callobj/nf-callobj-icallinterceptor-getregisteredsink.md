---
UID: NF:callobj.ICallInterceptor.GetRegisteredSink
title: ICallInterceptor::GetRegisteredSink (callobj.h)
description: Retrieves the registered event sink.
helpviewer_keywords: ["GetRegisteredSink","GetRegisteredSink method [COM]","GetRegisteredSink method [COM]","ICallInterceptor interface","ICallInterceptor interface [COM]","GetRegisteredSink method","ICallInterceptor.GetRegisteredSink","ICallInterceptor::GetRegisteredSink","_com_icallinterceptor_getregisteredsink","callobj/ICallInterceptor::GetRegisteredSink","com.icallinterceptor_getregisteredsink"]
old-location: com\icallinterceptor_getregisteredsink.htm
tech.root: com
ms.assetid: 65f33bc3-9fcb-4ad5-908d-3ac06b9f8c6c
ms.date: 12/05/2018
ms.keywords: GetRegisteredSink, GetRegisteredSink method [COM], GetRegisteredSink method [COM],ICallInterceptor interface, ICallInterceptor interface [COM],GetRegisteredSink method, ICallInterceptor.GetRegisteredSink, ICallInterceptor::GetRegisteredSink, _com_icallinterceptor_getregisteredsink, callobj/ICallInterceptor::GetRegisteredSink, com.icallinterceptor_getregisteredsink
req.header: callobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Callobj.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICallInterceptor::GetRegisteredSink
 - callobj/ICallInterceptor::GetRegisteredSink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Callobj.h
api_name:
 - ICallInterceptor.GetRegisteredSink
---

# ICallInterceptor::GetRegisteredSink


## -description

Retrieves the registered event sink.

## -parameters

### -param ppsink [out]

A pointer to a pointer to the event sink. See <a href="/windows/desktop/api/callobj/nn-callobj-icallframeevents">ICallFrameEvents</a>.

## -returns

This method can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_OBJNOTREG</b></dt>
</dl>
</td>
<td width="60%">
No event sink is registered with this interceptor.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/callobj/nn-callobj-icallinterceptor">ICallInterceptor</a>