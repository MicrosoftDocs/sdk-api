---
UID: NF:mfidl.IMFMediaSourceEx.GetStreamAttributes
title: IMFMediaSourceEx::GetStreamAttributes (mfidl.h)
description: Gets an attribute store for a stream on the media source.
helpviewer_keywords: ["GetStreamAttributes","GetStreamAttributes method [Media Foundation]","GetStreamAttributes method [Media Foundation]","IMFMediaSourceEx interface","IMFMediaSourceEx interface [Media Foundation]","GetStreamAttributes method","IMFMediaSourceEx.GetStreamAttributes","IMFMediaSourceEx::GetStreamAttributes","mf.imfmediasourceex_getstreamattributes","mfidl/IMFMediaSourceEx::GetStreamAttributes"]
old-location: mf\imfmediasourceex_getstreamattributes.htm
tech.root: mf
ms.assetid: 360B64E6-4936-4E40-A0EB-7E9EBAF1203E
ms.date: 12/05/2018
ms.keywords: GetStreamAttributes, GetStreamAttributes method [Media Foundation], GetStreamAttributes method [Media Foundation],IMFMediaSourceEx interface, IMFMediaSourceEx interface [Media Foundation],GetStreamAttributes method, IMFMediaSourceEx.GetStreamAttributes, IMFMediaSourceEx::GetStreamAttributes, mf.imfmediasourceex_getstreamattributes, mfidl/IMFMediaSourceEx::GetStreamAttributes
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
 - IMFMediaSourceEx::GetStreamAttributes
 - mfidl/IMFMediaSourceEx::GetStreamAttributes
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
 - IMFMediaSourceEx.GetStreamAttributes
---

# IMFMediaSourceEx::GetStreamAttributes


## -description

Gets an attribute store for a stream on the media source.

## -parameters

### -param dwStreamIdentifier [in]

The identifier of the stream. To get the identifier, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier">IMFStreamDescriptor::GetStreamIdentifier</a> on the stream descriptor.

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
The media source does not support stream-level attributes.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream identifier.

</td>
</tr>
</table>

## -remarks

Use the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> pointer to get or set attributes that apply to the specified stream. For attributes that apply to the entire source, use the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getsourceattributes">IMFMediaSourceEx::GetSourceAttributes</a> method instead.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex">IMFMediaSourceEx</a>