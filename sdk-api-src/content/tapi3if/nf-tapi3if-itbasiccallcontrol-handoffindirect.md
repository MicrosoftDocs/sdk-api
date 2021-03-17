---
UID: NF:tapi3if.ITBasicCallControl.HandoffIndirect
title: ITBasicCallControl::HandoffIndirect (tapi3if.h)
description: The HandoffIndirect method hands off the call to another application based on the media type of the call.
helpviewer_keywords: ["HandoffIndirect","HandoffIndirect method [TAPI 2.2]","HandoffIndirect method [TAPI 2.2]","ITBasicCallControl interface","ITBasicCallControl interface [TAPI 2.2]","HandoffIndirect method","ITBasicCallControl.HandoffIndirect","ITBasicCallControl::HandoffIndirect","_tapi3_itbasiccallcontrol_handoffindirect","tapi3.itbasiccallcontrol_handoffindirect","tapi3if/ITBasicCallControl::HandoffIndirect"]
old-location: tapi3\itbasiccallcontrol_handoffindirect.htm
tech.root: tapi3
ms.assetid: 02579638-fafd-4c4a-91a3-460d7ebf6917
ms.date: 12/05/2018
ms.keywords: HandoffIndirect, HandoffIndirect method [TAPI 2.2], HandoffIndirect method [TAPI 2.2],ITBasicCallControl interface, ITBasicCallControl interface [TAPI 2.2],HandoffIndirect method, ITBasicCallControl.HandoffIndirect, ITBasicCallControl::HandoffIndirect, _tapi3_itbasiccallcontrol_handoffindirect, tapi3.itbasiccallcontrol_handoffindirect, tapi3if/ITBasicCallControl::HandoffIndirect
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
 - ITBasicCallControl::HandoffIndirect
 - tapi3if/ITBasicCallControl::HandoffIndirect
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
 - ITBasicCallControl.HandoffIndirect
---

# ITBasicCallControl::HandoffIndirect


## -description

The 
<b>HandoffIndirect</b> method hands off the call to another application based on the 
<a href="/windows/desktop/Tapi/tapimediatype--constants">media type</a> of the call. If multiple applications have registered as able to handle the types involved, TAPI will hand off to the highest-priority application, which is usually the one that registered first.

This indicates that the application no longer requires ownership of the call.

## -parameters

### -param lMediaType [in]

<a href="/windows/desktop/Tapi/tapimediatype--constants">Media type</a> to transfer to.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>lMediaType</i> parameter is not valid.

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
</table>

## -remarks

Some service providers do not support this operation while streaming is active. The application may need to call 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-stopstream">ITStream::StopStream</a> or 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itsubstream-stopsubstream">ITSubStream::StopSubStream</a> prior to the operation and 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-startstream">ITStream::StartStream</a> or 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itsubstream-startsubstream">ITSubStream::StartSubStream</a> following completion of the operation.

If TAPI fails to hand off the call, TAPI will call 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect">Disconnect</a>.

## -see-also

<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/Tapi/handoffs-ovr">Handoffs overview</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a>



<a href="/windows/desktop/Tapi/tapimediatype--constants">TAPIMEDIATYPE_ Constants</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linehandoff">lineHandoff</a>