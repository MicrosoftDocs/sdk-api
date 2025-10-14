---
UID: NF:rtworkq.IRtwqAsyncCallback.GetParameters
title: IRtwqAsyncCallback::GetParameters (rtworkq.h)
description: Provides configuration information to the dispatching thread for a callback. (IRtwqAsyncCallback.GetParameters)
helpviewer_keywords: ["GetParameters","GetParameters method","GetParameters method","IRtwqAsyncCallback interface","IRtwqAsyncCallback interface","GetParameters method","IRtwqAsyncCallback.GetParameters","IRtwqAsyncCallback::GetParameters","Zero","base.irtwqasynccallback_getparameters","rtworkq/IRtwqAsyncCallback::GetParameters"]
old-location: base\irtwqasynccallback_getparameters.htm
tech.root: backup
ms.assetid: C6569BC4-E722-418E-B469-B20877F44648
ms.date: 12/05/2018
ms.keywords: GetParameters, GetParameters method, GetParameters method,IRtwqAsyncCallback interface, IRtwqAsyncCallback interface,GetParameters method, IRtwqAsyncCallback.GetParameters, IRtwqAsyncCallback::GetParameters, Zero, base.irtwqasynccallback_getparameters, rtworkq/IRtwqAsyncCallback::GetParameters
req.header: rtworkq.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rtworkq.lib
req.dll: RTWorkQ.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRtwqAsyncCallback::GetParameters
 - rtworkq/IRtwqAsyncCallback::GetParameters
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTWorkQ.dll
api_name:
 - IRtwqAsyncCallback.GetParameters
---

# IRtwqAsyncCallback::GetParameters


## -description

Provides configuration information to the dispatching thread for a callback.

## -parameters

### -param pdwFlags [out]

Receives a flag indicating the behavior of the callback object's <a href="/windows/desktop/api/rtworkq/nf-rtworkq-irtwqasynccallback-invoke">IRtwqAsyncCallback::Invoke</a> method. The following values are defined. The default value is zero.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="Zero"></a><a id="zero"></a><a id="ZERO"></a><dl>
<dt><b>Zero</b></dt>
</dl>
</td>
<td width="60%">
The callback does not take a long time to complete, but has no specific restrictions on what system calls it makes. The callback generally takes less than 30 milliseconds to complete.

</td>
</tr>
</table>

### -param pdwQueue [out]

Receives the identifier of the work queue on which the callback is dispatched.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented. Assume the default behavior.
              

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rtworkq/nn-rtworkq-irtwqasynccallback">IRtwqAsyncCallback</a>
