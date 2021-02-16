---
UID: NF:tapi3if.ITBasicCallControl.SwapHold
title: ITBasicCallControl::SwapHold (tapi3if.h)
description: The SwapHold method swaps the call (which is active) with the specified call on hold.
helpviewer_keywords: ["ITBasicCallControl interface [TAPI 2.2]","SwapHold method","ITBasicCallControl.SwapHold","ITBasicCallControl::SwapHold","SwapHold","SwapHold method [TAPI 2.2]","SwapHold method [TAPI 2.2]","ITBasicCallControl interface","_tapi3_itbasiccallcontrol_swaphold","tapi3.itbasiccallcontrol_swaphold","tapi3if/ITBasicCallControl::SwapHold"]
old-location: tapi3\itbasiccallcontrol_swaphold.htm
tech.root: tapi3
ms.assetid: 372e8ca9-53fb-4ec0-aae8-52f85523b7c4
ms.date: 12/05/2018
ms.keywords: ITBasicCallControl interface [TAPI 2.2],SwapHold method, ITBasicCallControl.SwapHold, ITBasicCallControl::SwapHold, SwapHold, SwapHold method [TAPI 2.2], SwapHold method [TAPI 2.2],ITBasicCallControl interface, _tapi3_itbasiccallcontrol_swaphold, tapi3.itbasiccallcontrol_swaphold, tapi3if/ITBasicCallControl::SwapHold
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITBasicCallControl::SwapHold
 - tapi3if/ITBasicCallControl::SwapHold
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITBasicCallControl.SwapHold
---

# ITBasicCallControl::SwapHold


## -description

The 
<b>SwapHold</b> method swaps the call (which is active) with the specified call on hold.

Swapping the active call with the call on consultation hold allows the application to toggle between these two calls. This is typical in call waiting.

## -parameters

### -param pCall [in]

Call, currently on hold, that is to be made active.

## -returns

This method can return one of these values.

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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
This operation is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pCall</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pCall</i> parameter does not describe a currently existing call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OPERATIONFAILED</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The operation failed because the TAPI 3 DLL timed it out. The timeout interval is two minutes.

</td>
</tr>
</table>

## -remarks

Some service providers do not support this operation while streaming is active. The application may need to call 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-stopstream">ITStream::StopStream</a> or 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itsubstream-stopsubstream">ITSubStream::StopSubStream</a> prior to the operation and 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-startstream">ITStream::StartStream</a> or 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itsubstream-startsubstream">ITSubStream::StartSubStream</a> following completion of the operation.

## -see-also

<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineswaphold">lineSwapHold</a>