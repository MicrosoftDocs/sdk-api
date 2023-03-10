---
UID: NF:tapi3if.ITStreamControl.get_Streams
title: ITStreamControl::get_Streams (tapi3if.h)
description: The get_Streams method creates a collection of media streams currently available on the call. Provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the EnumerateStreams method.
helpviewer_keywords: ["ITStreamControl interface [TAPI 2.2]","get_Streams method","ITStreamControl.get_Streams","ITStreamControl::get_Streams","_tapi3_itstreamcontrol_get_streams","get_Streams","get_Streams method [TAPI 2.2]","get_Streams method [TAPI 2.2]","ITStreamControl interface","tapi3.itstreamcontrol_get_streams","tapi3if/ITStreamControl::get_Streams"]
old-location: tapi3\itstreamcontrol_get_streams.htm
tech.root: tapi3
ms.assetid: 4d001f5a-7731-47b9-8c68-e4dd2d0bf02f
ms.date: 12/05/2018
ms.keywords: ITStreamControl interface [TAPI 2.2],get_Streams method, ITStreamControl.get_Streams, ITStreamControl::get_Streams, _tapi3_itstreamcontrol_get_streams, get_Streams, get_Streams method [TAPI 2.2], get_Streams method [TAPI 2.2],ITStreamControl interface, tapi3.itstreamcontrol_get_streams, tapi3if/ITStreamControl::get_Streams
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
 - ITStreamControl::get_Streams
 - tapi3if/ITStreamControl::get_Streams
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
 - ITStreamControl.get_Streams
---

# ITStreamControl::get_Streams


## -description

The 
<b>get_Streams</b> method creates a collection of media streams currently available on the call. Provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstreamcontrol-enumeratestreams">EnumerateStreams</a> method.

## -parameters

### -param pVariant [out]

Pointer to <b>VARIANT</b> containing an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a> interface pointers.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pVariant</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

TAPI calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a> interface returned by <b>ITStreamControl::get_Stream</b>. The application must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the 
<b>ITStream</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstreamcontrol">ITStreamControl</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>