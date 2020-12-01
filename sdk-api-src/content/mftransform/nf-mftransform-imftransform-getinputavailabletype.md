---
UID: NF:mftransform.IMFTransform.GetInputAvailableType
title: IMFTransform::GetInputAvailableType (mftransform.h)
description: Gets an available media type for an input stream on this Media Foundation transform (MFT).
helpviewer_keywords: ["GetInputAvailableType","GetInputAvailableType method [Media Foundation]","GetInputAvailableType method [Media Foundation]","IMFTransform interface","IMFTransform interface [Media Foundation]","GetInputAvailableType method","IMFTransform.GetInputAvailableType","IMFTransform::GetInputAvailableType","ed4cfdd0-28d5-4775-aa32-c17c6b13e5bf","mf.imftransform_getinputavailabletype","mftransform/IMFTransform::GetInputAvailableType"]
old-location: mf\imftransform_getinputavailabletype.htm
tech.root: mf
ms.assetid: ed4cfdd0-28d5-4775-aa32-c17c6b13e5bf
ms.date: 12/05/2018
ms.keywords: GetInputAvailableType, GetInputAvailableType method [Media Foundation], GetInputAvailableType method [Media Foundation],IMFTransform interface, IMFTransform interface [Media Foundation],GetInputAvailableType method, IMFTransform.GetInputAvailableType, IMFTransform::GetInputAvailableType, ed4cfdd0-28d5-4775-aa32-c17c6b13e5bf, mf.imftransform_getinputavailabletype, mftransform/IMFTransform::GetInputAvailableType
req.header: mftransform.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFTransform::GetInputAvailableType
 - mftransform/IMFTransform::GetInputAvailableType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFTransform.GetInputAvailableType
---

# IMFTransform::GetInputAvailableType


## -description

Gets an available media type for an input stream on this Media Foundation transform (MFT).

## -parameters

### -param dwInputStreamID [in]

Input stream identifier. To get the list of stream identifiers, call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids">IMFTransform::GetStreamIDs</a>.

### -param dwTypeIndex [in]

Index of the media type to retrieve. Media types are indexed from zero and returned in approximate order of preference.

### -param ppType [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The MFT does not have a list of available input types.
              

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NO_MORE_TYPES</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwTypeIndex</i> parameter is out of range.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_TRANSFORM_TYPE_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
You must set the output types before setting the input types.
              

</td>
</tr>
</table>

## -remarks

The MFT defines a list of available media types for each input stream and orders them by preference. This method enumerates the available media types for an input stream. To enumerate the available types, increment <i>dwTypeIndex</i> until the method returns <b>MF_E_NO_MORE_TYPES</b>.
      

Setting the media type on one stream might change the available types for another stream, or change the preference order. However, an MFT is not required to update the list of available types dynamically. The only guaranteed way to test whether you can set a particular input type is to call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype">IMFTransform::SetInputType</a>.
      

In some cases, an MFT cannot return a list of input types until one or more output types are set. If so, the method returns <b>MF_E_TRANSFORM_TYPE_NOT_SET</b>.
      

An MFT is not required to implement this method. However, most MFTs should implement this method, unless the supported types are simple and can be discovered through the <a href="/windows/desktop/api/mfapi/nf-mfapi-mftgetinfo">MFTGetInfo</a> function.

If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including mftransform.h, this method is renamed <b>MFTGetInputAvailableType</b>. See <a href="/windows/desktop/medfound/comparison-of-mfts-and-dmos">Creating Hybrid DMO/MFT Objects</a>.

For encoders, after the output type is set, <b>GetInputAvailableType</b> must return a list of input types that are compatible with the current output type. This means that all types returned by <b>GetInputAvailableType</b> after the output type is set must be valid types for <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype">SetInputType</a>.

Encoders should reject input types if the attributes of the input media type and output media type do not match, such as resolution setting with <a href="/windows/desktop/medfound/mf-mt-frame-size-attribute">MF_MT_FRAME_SIZE</a>, nominal range setting with <a href="/windows/desktop/medfound/mf-mt-video-nominal-range-attribute">MF_MT_VIDEO_NOMINAL_RANGE</a>, or frame rate setting with MF_MT_FRAME_SIZE

<h3><a id="Implementation_Notes"></a><a id="implementation_notes"></a><a id="IMPLEMENTATION_NOTES"></a>Implementation Notes</h3>
If the MFT stores a media type internally, the MFT should return a clone of the media  type, not a pointer to the original type. Otherwise, the caller might modify the type and alter the internal state of the MFT.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>