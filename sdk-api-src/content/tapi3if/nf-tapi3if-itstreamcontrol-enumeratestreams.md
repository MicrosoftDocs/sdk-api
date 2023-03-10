---
UID: NF:tapi3if.ITStreamControl.EnumerateStreams
title: ITStreamControl::EnumerateStreams (tapi3if.h)
description: The EnumerateStreams method enumerates currently available media streams. Provided for C and C++ applications. Automation client applications such as Visual Basic must use the get_Streams method.
helpviewer_keywords: ["EnumerateStreams","EnumerateStreams method [TAPI 2.2]","EnumerateStreams method [TAPI 2.2]","ITStreamControl interface","ITStreamControl interface [TAPI 2.2]","EnumerateStreams method","ITStreamControl.EnumerateStreams","ITStreamControl::EnumerateStreams","_tapi3_itstreamcontrol_enumeratestreams","tapi3.itstreamcontrol_enumeratestreams","tapi3if/ITStreamControl::EnumerateStreams"]
old-location: tapi3\itstreamcontrol_enumeratestreams.htm
tech.root: tapi3
ms.assetid: de018f3e-d3b9-4093-a2b5-4929ac4d1d2a
ms.date: 12/05/2018
ms.keywords: EnumerateStreams, EnumerateStreams method [TAPI 2.2], EnumerateStreams method [TAPI 2.2],ITStreamControl interface, ITStreamControl interface [TAPI 2.2],EnumerateStreams method, ITStreamControl.EnumerateStreams, ITStreamControl::EnumerateStreams, _tapi3_itstreamcontrol_enumeratestreams, tapi3.itstreamcontrol_enumeratestreams, tapi3if/ITStreamControl::EnumerateStreams
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
 - ITStreamControl::EnumerateStreams
 - tapi3if/ITStreamControl::EnumerateStreams
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
 - ITStreamControl.EnumerateStreams
---

# ITStreamControl::EnumerateStreams


## -description

The <b>EnumerateStreams</b> method enumerates currently available media streams. Provided for C and C++ applications. Automation client applications such as Visual Basic must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstreamcontrol-get_streams">get_Streams</a> method.

## -parameters

### -param ppEnumStream [out]

Pointer to pointer for 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream">IEnumStream</a> enumerator.

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
The <i>ppEnumStream</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

TAPI calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream">IEnumStream</a> interface returned by <b>ITStreamControl::EnumerateStreams</b>. The application must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the 
<b>IEnumStream</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstreamcontrol">ITStreamControl</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>