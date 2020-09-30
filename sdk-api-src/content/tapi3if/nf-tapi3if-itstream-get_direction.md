---
UID: NF:tapi3if.ITStream.get_Direction
title: ITStream::get_Direction (tapi3if.h)
description: The get_Direction method gets the stream's terminal direction.
helpviewer_keywords: ["ITStream interface [TAPI 2.2]","get_Direction method","ITStream.get_Direction","ITStream::get_Direction","_tapi3_itstream_get_direction","get_Direction","get_Direction method [TAPI 2.2]","get_Direction method [TAPI 2.2]","ITStream interface","tapi3.itstream_get_direction","tapi3if/ITStream::get_Direction"]
old-location: tapi3\itstream_get_direction.htm
tech.root: tapi3
ms.assetid: 196abe2a-d88d-4b2d-8867-4e6cc15dee33
ms.date: 12/05/2018
ms.keywords: ITStream interface [TAPI 2.2],get_Direction method, ITStream.get_Direction, ITStream::get_Direction, _tapi3_itstream_get_direction, get_Direction, get_Direction method [TAPI 2.2], get_Direction method [TAPI 2.2],ITStream interface, tapi3.itstream_get_direction, tapi3if/ITStream::get_Direction
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
 - ITStream::get_Direction
 - tapi3if/ITStream::get_Direction
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
 - ITStream.get_Direction
---

# ITStream::get_Direction


## -description

The 
<b>get_Direction</b> method gets the stream's 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-terminal_direction">terminal direction</a>.

## -parameters

### -param pTD [out]

Pointer to 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-terminal_direction">TERMINAL_DIRECTION</a> descriptor.

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
The <i>pTD</i> parameter is not a valid pointer.

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

Terminals of either direction can, in general, be selected on any stream whose media type matches the terminal's media type. However, some MSPs allow only terminals whose terminal direction matches the stream's terminal direction to be selected on a stream.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-terminal_direction">TERMINAL_DIRECTION</a>