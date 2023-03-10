---
UID: NF:mfidl.IMFSensorStream.GetMediaType
title: IMFSensorStream::GetMediaType (mfidl.h)
description: Retrieves an IMFMediaType representing a supported media type for the sensor stream.
helpviewer_keywords: ["GetMediaType","GetMediaType method [Media Foundation]","GetMediaType method [Media Foundation]","IMFSensorStream interface","IMFSensorStream interface [Media Foundation]","GetMediaType method","IMFSensorStream.GetMediaType","IMFSensorStream::GetMediaType","mf.imfsensorstream_getmediatype","mfidl/IMFSensorStream::GetMediaType"]
old-location: mf\imfsensorstream_getmediatype.htm
tech.root: mf
ms.assetid: 510AD624-F212-4FD7-BF30-A5C90CFA23C5
ms.date: 12/05/2018
ms.keywords: GetMediaType, GetMediaType method [Media Foundation], GetMediaType method [Media Foundation],IMFSensorStream interface, IMFSensorStream interface [Media Foundation],GetMediaType method, IMFSensorStream.GetMediaType, IMFSensorStream::GetMediaType, mf.imfsensorstream_getmediatype, mfidl/IMFSensorStream::GetMediaType
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSensorStream::GetMediaType
 - mfidl/IMFSensorStream::GetMediaType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplat.lib
 - mfplat.dll
 - mfplat.dll
 - mfplat.dll.dll
api_name:
 - IMFSensorStream.GetMediaType
---

# IMFSensorStream::GetMediaType


## -description

Retrieves an <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> representing a supported media type for the sensor stream.

## -parameters

### -param dwIndex [in]

The 0-based index of the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> to retrieve. This value must be between 0 and the value returned by <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsensorstream-getmediatypecount">GetMediaTypeCount</a> - 1.

### -param ppMediaType [out]

The retrieved media type.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

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
The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppMediaType</i> parameter is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDINDEX</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwIndex</i> is not in the allowed range.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorstream">IMFSensorStream</a>