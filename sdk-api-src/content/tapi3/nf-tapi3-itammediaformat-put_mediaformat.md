---
UID: NF:tapi3.ITAMMediaFormat.put_MediaFormat
title: ITAMMediaFormat::put_MediaFormat (tapi3.h)
description: The ITAMMediaFormat::put_MediaFormat (tapi3.h) method sets the media format.
helpviewer_keywords: ["ITAMMediaFormat interface [TAPI 2.2]","put_MediaFormat method","ITAMMediaFormat.put_MediaFormat","ITAMMediaFormat::put_MediaFormat","_tapi3_itammediaformat_put_mediaformat","put_MediaFormat","put_MediaFormat method [TAPI 2.2]","put_MediaFormat method [TAPI 2.2]","ITAMMediaFormat interface","tapi3.itammediaformat_put_mediaformat","tapi3ds/ITAMMediaFormat::put_MediaFormat"]
old-location: tapi3\itammediaformat_put_mediaformat.htm
tech.root: tapi3
ms.assetid: 692df069-3016-46a2-9f33-4c709e85be1b
ms.date: 08/09/2022
ms.keywords: ITAMMediaFormat interface [TAPI 2.2],put_MediaFormat method, ITAMMediaFormat.put_MediaFormat, ITAMMediaFormat::put_MediaFormat, _tapi3_itammediaformat_put_mediaformat, put_MediaFormat, put_MediaFormat method [TAPI 2.2], put_MediaFormat method [TAPI 2.2],ITAMMediaFormat interface, tapi3.itammediaformat_put_mediaformat, tapi3ds/ITAMMediaFormat::put_MediaFormat
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
 - ITAMMediaFormat::put_MediaFormat
 - tapi3/ITAMMediaFormat::put_MediaFormat
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
 - ITAMMediaFormat.put_MediaFormat
---

# ITAMMediaFormat::put_MediaFormat


## -description

The 
<b>put_MediaFormat</b> method sets the media format.

## -parameters

### -param pmt [in]

Pointer to 
<b>AM_MEDIA_TYPE</b> structure. For more information on <b>AM_MEDIA_TYPE</b>, see the DirectX documentation.

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

## -remarks

On addresses where a variety of formats are supported (such as Wave MSP addresses, which are used on most modems and voice boards), this call is mandatory or the terminal will not be able to connect.

For other addresses, such as those implemented over IP, the format may be fixed/predetermined. In that case, this call will fail if the format is not the same as the predetermined format. To retrieve such a predetermined format, an application can use 
<a href="/windows/desktop/api/tapi3/nf-tapi3-itammediaformat-get_mediaformat">get_MediaFormat</a>.

## -see-also

<a href="/windows/desktop/api/tapi3/nn-tapi3-itammediaformat">ITAMMediaFormat</a>



<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>



<a href="/windows/desktop/api/tapi3/nf-tapi3-itammediaformat-get_mediaformat">get_MediaFormat</a>
