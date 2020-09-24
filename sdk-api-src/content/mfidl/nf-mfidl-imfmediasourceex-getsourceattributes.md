---
UID: NF:mfidl.IMFMediaSourceEx.GetSourceAttributes
title: IMFMediaSourceEx::GetSourceAttributes (mfidl.h)
description: Gets an attribute store for the media source.
helpviewer_keywords: ["GetSourceAttributes","GetSourceAttributes method [Media Foundation]","GetSourceAttributes method [Media Foundation]","IMFMediaSourceEx interface","IMFMediaSourceEx interface [Media Foundation]","GetSourceAttributes method","IMFMediaSourceEx.GetSourceAttributes","IMFMediaSourceEx::GetSourceAttributes","mf.imfmediasourceex_getsourceattributes","mfidl/IMFMediaSourceEx::GetSourceAttributes"]
old-location: mf\imfmediasourceex_getsourceattributes.htm
tech.root: mf
ms.assetid: A58A2537-1ABD-4EC5-AC84-A5FFA7127CEB
ms.date: 12/05/2018
ms.keywords: GetSourceAttributes, GetSourceAttributes method [Media Foundation], GetSourceAttributes method [Media Foundation],IMFMediaSourceEx interface, IMFMediaSourceEx interface [Media Foundation],GetSourceAttributes method, IMFMediaSourceEx.GetSourceAttributes, IMFMediaSourceEx::GetSourceAttributes, mf.imfmediasourceex_getsourceattributes, mfidl/IMFMediaSourceEx::GetSourceAttributes
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IMFMediaSourceEx::GetSourceAttributes
 - mfidl/IMFMediaSourceEx::GetSourceAttributes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFMediaSourceEx.GetSourceAttributes
---

# IMFMediaSourceEx::GetSourceAttributes


## -description

Gets an attribute store for the media source.

## -parameters

### -param ppAttributes [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface. The caller must release the interface.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The media source does not support source-level attributes.

</td>
</tr>
</table>

## -remarks

Use the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> pointer to get or set attributes that apply to the entire source. For stream-level attributes, use the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes">IMFMediaSourceEx::GetStreamAttributes</a> method instead.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex">IMFMediaSourceEx</a>