---
UID: NF:tapi3if.ITSubStreamControl.RemoveSubStream
title: ITSubStreamControl::RemoveSubStream (tapi3if.h)
description: The RemoveSubStream method removes a substream.
helpviewer_keywords: ["ITSubStreamControl interface [TAPI 2.2]","RemoveSubStream method","ITSubStreamControl.RemoveSubStream","ITSubStreamControl::RemoveSubStream","RemoveSubStream","RemoveSubStream method [TAPI 2.2]","RemoveSubStream method [TAPI 2.2]","ITSubStreamControl interface","_tapi3_itsubstreamcontrol_removesubstream","tapi3.itsubstreamcontrol_removesubstream","tapi3if/ITSubStreamControl::RemoveSubStream"]
old-location: tapi3\itsubstreamcontrol_removesubstream.htm
tech.root: tapi3
ms.assetid: 1a1be17c-2cae-4eea-a20a-3344915c5234
ms.date: 12/05/2018
ms.keywords: ITSubStreamControl interface [TAPI 2.2],RemoveSubStream method, ITSubStreamControl.RemoveSubStream, ITSubStreamControl::RemoveSubStream, RemoveSubStream, RemoveSubStream method [TAPI 2.2], RemoveSubStream method [TAPI 2.2],ITSubStreamControl interface, _tapi3_itsubstreamcontrol_removesubstream, tapi3.itsubstreamcontrol_removesubstream, tapi3if/ITSubStreamControl::RemoveSubStream
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITSubStreamControl::RemoveSubStream
 - tapi3if/ITSubStreamControl::RemoveSubStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tapi3if.h
api_name:
 - ITSubStreamControl.RemoveSubStream
---

# ITSubStreamControl::RemoveSubStream


## -description

The 
<b>RemoveSubStream</b> method removes a substream.

## -parameters

### -param pSubStream [in]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itsubstream">ITSubStream</a> to be removed.

## -returns

This method can return one of these values.

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
The <i>pSubStream</i> parameter does not point to a valid interface.

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
<dt><b>TAPI_E_INVALIDSTREAM</b></dt>
</dl>
</td>
<td width="60%">
The <i>pSubStream</i> parameter does not point to a valid substream.

</td>
</tr>
</table>

## -remarks

Some MSPs may not support the advanced concept of creating and removing substreams, and simply return TAPI_E_NOTSUPPORTED.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itsubstreamcontrol">ITSubStreamControl</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>