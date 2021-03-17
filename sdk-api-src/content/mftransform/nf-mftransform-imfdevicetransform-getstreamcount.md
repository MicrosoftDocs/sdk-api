---
UID: NF:mftransform.IMFDeviceTransform.GetStreamCount
title: IMFDeviceTransform::GetStreamCount (mftransform.h)
description: The GetStreamCount method gets the current number of input and output streams on this Media Foundation transform (MFT).
helpviewer_keywords: ["GetStreamCount","GetStreamCount method [Streaming Media Devices]","GetStreamCount method [Streaming Media Devices]","IMFDeviceTransform interface","IMFDeviceTransform interface [Streaming Media Devices]","GetStreamCount method","IMFDeviceTransform.GetStreamCount","IMFDeviceTransform::GetStreamCount","mftransform/IMFDeviceTransform::GetStreamCount","stream.imfdevicetransform_getstreamcount"]
old-location: stream\imfdevicetransform_getstreamcount.htm
tech.root: stream
ms.assetid: 6FD4B393-05E6-4400-B1A3-D69B7F1B90F0
ms.date: 12/05/2018
ms.keywords: GetStreamCount, GetStreamCount method [Streaming Media Devices], GetStreamCount method [Streaming Media Devices],IMFDeviceTransform interface, IMFDeviceTransform interface [Streaming Media Devices],GetStreamCount method, IMFDeviceTransform.GetStreamCount, IMFDeviceTransform::GetStreamCount, mftransform/IMFDeviceTransform::GetStreamCount, stream.imfdevicetransform_getstreamcount
req.header: mftransform.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703
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
 - IMFDeviceTransform::GetStreamCount
 - mftransform/IMFDeviceTransform::GetStreamCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mftransform.h
api_name:
 - IMFDeviceTransform.GetStreamCount
---

# IMFDeviceTransform::GetStreamCount


## -description

The <b>GetStreamCount</b> method gets the current number of input and output streams on this Media Foundation transform (MFT).

## -parameters

### -param pcInputStreams [out]

Receives the number of input streams.

### -param pcOutputStreams [out]

Receives the number of output streams.

## -returns

The method returns an <b>HRESULT</b>. Possible values include,  but are  not limited to the values given in the following table.

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
Transitioning the stream state succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer passed.

</td>
</tr>
</table>

## -remarks

This function is used by DTM to get the number of streams supported by the Device MFT. The number of streams include unselected streams., fore example, streams with no media type or a NULL media type.

This method would not be called with NULL parameters.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imfdevicetransform">IMFDeviceTransform</a>