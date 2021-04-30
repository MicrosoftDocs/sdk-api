---
UID: NF:tapi3if.ITStreamControl.CreateStream
title: ITStreamControl::CreateStream (tapi3if.h)
description: The CreateStream method creates a new media stream.
helpviewer_keywords: ["CreateStream","CreateStream method [TAPI 2.2]","CreateStream method [TAPI 2.2]","ITStreamControl interface","ITStreamControl interface [TAPI 2.2]","CreateStream method","ITStreamControl.CreateStream","ITStreamControl::CreateStream","_tapi3_itstreamcontrol_createstream","tapi3.itstreamcontrol_createstream","tapi3if/ITStreamControl::CreateStream"]
old-location: tapi3\itstreamcontrol_createstream.htm
tech.root: tapi3
ms.assetid: 402cde43-6b2a-4e4e-bf46-97fcafb7574a
ms.date: 12/05/2018
ms.keywords: CreateStream, CreateStream method [TAPI 2.2], CreateStream method [TAPI 2.2],ITStreamControl interface, ITStreamControl interface [TAPI 2.2],CreateStream method, ITStreamControl.CreateStream, ITStreamControl::CreateStream, _tapi3_itstreamcontrol_createstream, tapi3.itstreamcontrol_createstream, tapi3if/ITStreamControl::CreateStream
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
 - ITStreamControl::CreateStream
 - tapi3if/ITStreamControl::CreateStream
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
 - ITStreamControl.CreateStream
---

# ITStreamControl::CreateStream


## -description

The 
<b>CreateStream</b> method creates a new media stream.

## -parameters

### -param lMediaType [in]

Indicates 
<a href="/windows/desktop/Tapi/tapimediatype--constants">media type</a> for stream.

### -param td [in]

Indicates the 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-terminal_direction">TERMINAL_DIRECTION</a>.

### -param ppStream [out]

Pointer to pointer for newly created 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a> interface.

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
The <i>ppStream</i> parameter is not a valid pointer.

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
<dt><b>TAPI_E_INVALIDMEDIATYPE</b></dt>
</dl>
</td>
<td width="60%">
The <i>lMediaType</i> parameter is not a valid media type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_INVALIDDIRECTION</b></dt>
</dl>
</td>
<td width="60%">
The <i>td</i> parameter is not a valid terminal direction.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_MAXSTREAMS</b></dt>
</dl>
</td>
<td width="60%">
The maximum number of streams supported has already been reached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
This operation is not supported.

</td>
</tr>
</table>

## -remarks

Many MSPs do not support dynamic creation of streams, and simply return TAPI_E_MAXSTREAMS in their implementation of this method. Default streams are automatically available when a call is created, so most applications do not have to use this method.

Stream creation or removal may involve interaction with a remote endpoint, resulting in a CMC_REMOTE_REQUEST rather than the CMC_LOCAL_REQUEST messages that are received when a stream is stopped or started.

TAPI calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a> interface returned by <b>ITStreamControl::CreateStream</b>. The application must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the 
<b>ITStream</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstreamcontrol">ITStreamControl</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-terminal_direction">TERMINAL_DIRECTION</a>



<a href="/windows/desktop/Tapi/tapimediatype--constants">media type</a>