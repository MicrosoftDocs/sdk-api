---
UID: NF:mftransform.IMFDeviceTransform.GetStreamIDs
title: IMFDeviceTransform::GetStreamIDs (mftransform.h)
description: The GetStreamIDs method gets the stream identifiers for the input and output streams on this Media Foundation transform (MFT).
helpviewer_keywords: ["GetStreamIDs","GetStreamIDs method [Streaming Media Devices]","GetStreamIDs method [Streaming Media Devices]","IMFDeviceTransform interface","IMFDeviceTransform interface [Streaming Media Devices]","GetStreamIDs method","IMFDeviceTransform.GetStreamIDs","IMFDeviceTransform::GetStreamIDs","mftransform/IMFDeviceTransform::GetStreamIDs","stream.imfdevicetransform_getstreamids"]
old-location: stream\imfdevicetransform_getstreamids.htm
tech.root: stream
ms.assetid: 378A8E3F-8B1E-4C0B-9C30-FE78E1939422
ms.date: 12/05/2018
ms.keywords: GetStreamIDs, GetStreamIDs method [Streaming Media Devices], GetStreamIDs method [Streaming Media Devices],IMFDeviceTransform interface, IMFDeviceTransform interface [Streaming Media Devices],GetStreamIDs method, IMFDeviceTransform.GetStreamIDs, IMFDeviceTransform::GetStreamIDs, mftransform/IMFDeviceTransform::GetStreamIDs, stream.imfdevicetransform_getstreamids
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
 - IMFDeviceTransform::GetStreamIDs
 - mftransform/IMFDeviceTransform::GetStreamIDs
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
 - IMFDeviceTransform.GetStreamIDs
---

# IMFDeviceTransform::GetStreamIDs


## -description

The  <b>GetStreamIDs</b> method gets the stream identifiers for the input and output streams on this Media Foundation transform (MFT).

## -parameters

### -param dwInputIDArraySize [in]

The number of elements in <i>pdwInputStreamIDs</i>

### -param pdwInputStreamIds [out]

 A pointer to an array allocated by the caller. The method fills the array with the input stream identifiers. The array size must be at least equal to the number of input streams. To get the number of input streams, call <a href="/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-getstreamcount">IMFDeviceTransform::GetStreamCount</a>. 

If the caller passes an array that is larger than the number of input streams, the MFT must not write values into the extra array entries.

### -param dwOutputIDArraySize [out]

The number of elements in <i>pdwOutputStreamIDs</i>.

### -param pdwOutputStreamIds

A pointer to an array allocated by the caller. The method fills the array with the output stream identifiers. The array size must be at least equal to the number of output streams. To get the number of output streams, call <a href="/windows/desktop/api/mftransform/nf-mftransform-imfdevicetransform-getstreamcount">IMFDeviceTransform::GetStreamCount</a>.

## -returns

The method returns an <b>HRESULT</b>. Possible values include but not limited to values given in the following table.

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer coming in does not  have enough space to fill in the stream IDs.

</td>
</tr>
</table>

## -remarks

Stream identifiers are necessary because some MFTs can add or remove streams, so the index of a stream may not be unique. Therefore, <a href="/windows/desktop/api/mftransform/nn-mftransform-imfdevicetransform">IMFDeviceTransform</a> methods that operate on streams take stream identifiers.

All input stream identifiers must be unique within an MFT, and all output stream identifiers must be unique. However, an input stream and an output stream can share the same identifier. 
I

If the client adds an input stream, the client assigns the identifier, so the MFT must allow arbitrary identifiers, as long as they are unique. If the MFT creates an output stream, the MFT assigns the identifier. 


By convention, if an MFT has exactly one fixed input stream and one fixed output stream, it should assign the identifier 0 to both streams.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imfdevicetransform">IMFDeviceTransform</a>