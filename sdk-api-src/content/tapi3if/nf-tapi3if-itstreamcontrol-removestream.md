---
UID: NF:tapi3if.ITStreamControl.RemoveStream
title: ITStreamControl::RemoveStream (tapi3if.h)
description: The RemoveStream method removes a media stream.
helpviewer_keywords: ["ITStreamControl interface [TAPI 2.2]","RemoveStream method","ITStreamControl.RemoveStream","ITStreamControl::RemoveStream","RemoveStream","RemoveStream method [TAPI 2.2]","RemoveStream method [TAPI 2.2]","ITStreamControl interface","_tapi3_itstreamcontrol_removestream","tapi3.itstreamcontrol_removestream","tapi3if/ITStreamControl::RemoveStream"]
old-location: tapi3\itstreamcontrol_removestream.htm
tech.root: tapi3
ms.assetid: cd432d49-04f6-4f1f-a6a1-937658d615d6
ms.date: 12/05/2018
ms.keywords: ITStreamControl interface [TAPI 2.2],RemoveStream method, ITStreamControl.RemoveStream, ITStreamControl::RemoveStream, RemoveStream, RemoveStream method [TAPI 2.2], RemoveStream method [TAPI 2.2],ITStreamControl interface, _tapi3_itstreamcontrol_removestream, tapi3.itstreamcontrol_removestream, tapi3if/ITStreamControl::RemoveStream
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
 - ITStreamControl::RemoveStream
 - tapi3if/ITStreamControl::RemoveStream
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
 - ITStreamControl.RemoveStream
---

# ITStreamControl::RemoveStream


## -description

The 
<b>RemoveStream</b> method removes a media stream.

## -parameters

### -param pStream [in]

Pointer to 
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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pStream</i> parameter is not valid.

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

Some MSPs may not support the advanced concept of creating and removing streams, and simply return TAPI_E_NOTSUPPORTED.

Stream creation or removal may involve interaction with a remote endpoint, resulting in a CMC_REMOTE_REQUEST rather than the CMC_LOCAL_REQUEST messages that are received when a stream is stopped or started.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstreamcontrol">ITStreamControl</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>