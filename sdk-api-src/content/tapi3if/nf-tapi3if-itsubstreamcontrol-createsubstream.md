---
UID: NF:tapi3if.ITSubStreamControl.CreateSubStream
title: ITSubStreamControl::CreateSubStream (tapi3if.h)
description: The CreateSubStream method creates a substream.
helpviewer_keywords: ["CreateSubStream","CreateSubStream method [TAPI 2.2]","CreateSubStream method [TAPI 2.2]","ITSubStreamControl interface","ITSubStreamControl interface [TAPI 2.2]","CreateSubStream method","ITSubStreamControl.CreateSubStream","ITSubStreamControl::CreateSubStream","_tapi3_itsubstreamcontrol_createsubstream","tapi3.itsubstreamcontrol_createsubstream","tapi3if/ITSubStreamControl::CreateSubStream"]
old-location: tapi3\itsubstreamcontrol_createsubstream.htm
tech.root: tapi3
ms.assetid: 00fe0f8f-c814-4ae6-a60b-c58f3dc60b67
ms.date: 12/05/2018
ms.keywords: CreateSubStream, CreateSubStream method [TAPI 2.2], CreateSubStream method [TAPI 2.2],ITSubStreamControl interface, ITSubStreamControl interface [TAPI 2.2],CreateSubStream method, ITSubStreamControl.CreateSubStream, ITSubStreamControl::CreateSubStream, _tapi3_itsubstreamcontrol_createsubstream, tapi3.itsubstreamcontrol_createsubstream, tapi3if/ITSubStreamControl::CreateSubStream
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
 - ITSubStreamControl::CreateSubStream
 - tapi3if/ITSubStreamControl::CreateSubStream
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
 - ITSubStreamControl.CreateSubStream
---

# ITSubStreamControl::CreateSubStream


## -description

The 
<b>CreateSubStream</b> method creates a substream.

## -parameters

### -param ppSubStream [out]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itsubstream">ITSubStream</a> interface created.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppSubStream</i> parameter is not a valid pointer.

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
<dt><b>TAPI_E_MAXSTREAMS</b></dt>
</dl>
</td>
<td width="60%">
Substream cannot be created because the maximum number of streams has already been reached.

</td>
</tr>
</table>

## -remarks

Many MSPs do not support dynamic creation of substreams, and simply return TAPI_E_MAXSTREAMS in their implementation of this method.

TAPI calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itsubstream">ITSubStream</a> interface returned by <b>ITSubStreamControl::CreateSubStream</b>. The application must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the 
<b>ITSubStream</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itsubstreamcontrol">ITSubStreamControl</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>