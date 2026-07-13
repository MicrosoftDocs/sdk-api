---
UID: NF:tapi3.ITAMMediaFormat.get_MediaFormat
title: ITAMMediaFormat::get_MediaFormat (tapi3.h)
description: The ITAMMediaFormat::get_MediaFormat (tapi3.h) method gets the media format.
helpviewer_keywords: ["ITAMMediaFormat interface [TAPI 2.2]","get_MediaFormat method","ITAMMediaFormat.get_MediaFormat","ITAMMediaFormat::get_MediaFormat","_tapi3_itammediaformat_get_mediaformat","get_MediaFormat","get_MediaFormat method [TAPI 2.2]","get_MediaFormat method [TAPI 2.2]","ITAMMediaFormat interface","tapi3.itammediaformat_get_mediaformat","tapi3ds/ITAMMediaFormat::get_MediaFormat"]
old-location: tapi3\itammediaformat_get_mediaformat.htm
tech.root: tapi3
ms.assetid: 384cd41e-b59a-4ac4-9687-cf0f0738dfe0
ms.date: 08/09/2022
ms.keywords: ITAMMediaFormat interface [TAPI 2.2],get_MediaFormat method, ITAMMediaFormat.get_MediaFormat, ITAMMediaFormat::get_MediaFormat, _tapi3_itammediaformat_get_mediaformat, get_MediaFormat, get_MediaFormat method [TAPI 2.2], get_MediaFormat method [TAPI 2.2],ITAMMediaFormat interface, tapi3.itammediaformat_get_mediaformat, tapi3ds/ITAMMediaFormat::get_MediaFormat
req.header: tapi3.h
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
 - ITAMMediaFormat::get_MediaFormat
 - tapi3/ITAMMediaFormat::get_MediaFormat
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
 - ITAMMediaFormat.get_MediaFormat
---

# ITAMMediaFormat::get_MediaFormat


## -description

The 
<b>get_MediaFormat</b> method gets the media format.

## -parameters

### -param ppmt [out]

Pointer to an array of 
<b>AM_MEDIA_TYPE</b> structures. For more information on <b>AM_MEDIA_TYPE</b>, see the DirectX documentation.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3/nn-tapi3-itammediaformat">ITAMMediaFormat</a>



<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>



<a href="/windows/desktop/api/tapi3/nf-tapi3-itammediaformat-put_mediaformat">put_MediaFormat</a>
