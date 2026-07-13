---
UID: NF:mfidl.MFCreateSensorStream
title: MFCreateSensorStream function (mfidl.h)
description: Creates an instance of the IMFSensorStream interface.
helpviewer_keywords: ["MFCreateSensorStream","MFCreateSensorStream function [Media Foundation]","mf.mfcreatesensorstream","mfidl/MFCreateSensorStream"]
old-location: mf\mfcreatesensorstream.htm
tech.root: mf
ms.assetid: 3C260634-E722-4F1D-800C-FB32308CF605
ms.date: 12/05/2018
ms.keywords: MFCreateSensorStream, MFCreateSensorStream function [Media Foundation], mf.mfcreatesensorstream, mfidl/MFCreateSensorStream
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps \| UWP apps]
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
req.lib: mfsensorgroup.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateSensorStream
 - mfidl/MFCreateSensorStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFCreateSensorStream
---

# MFCreateSensorStream function


## -description

Creates an instance of the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorstream">IMFSensorStream</a> interface.

## -parameters

### -param StreamId

The identifier for the created stream. This is the same as setting the <a href="/windows/desktop/medfound/mf-devicestream-stream-id">MF_DEVICESTREAM_STREAM_ID</a> attribute. This value is used if <i>pAttributes</i> is null.

### -param pAttributes [in, optional]

The attribute store for the created stream.

### -param pMediaTypeCollection [in]

The collection of <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> objects specifying the media types supported by the stream.

### -param ppStream [out]

The created stream interface.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The supplied <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorgroup">IMFSensorGroup</a> is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The supplied <b>LPCWSTR</b> is null.

</td>
</tr>
</table>