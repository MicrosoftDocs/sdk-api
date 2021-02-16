---
UID: NF:mftransform.IMFTransform.GetInputCurrentType
title: IMFTransform::GetInputCurrentType (mftransform.h)
description: Gets the current media type for an input stream on this Media Foundation transform (MFT).
helpviewer_keywords: ["GetInputCurrentType","GetInputCurrentType method [Media Foundation]","GetInputCurrentType method [Media Foundation]","IMFTransform interface","IMFTransform interface [Media Foundation]","GetInputCurrentType method","IMFTransform.GetInputCurrentType","IMFTransform::GetInputCurrentType","f3603586-41fd-4eed-9942-28925ed29690","mf.imftransform_getinputcurrenttype","mftransform/IMFTransform::GetInputCurrentType"]
old-location: mf\imftransform_getinputcurrenttype.htm
tech.root: mf
ms.assetid: f3603586-41fd-4eed-9942-28925ed29690
ms.date: 12/05/2018
ms.keywords: GetInputCurrentType, GetInputCurrentType method [Media Foundation], GetInputCurrentType method [Media Foundation],IMFTransform interface, IMFTransform interface [Media Foundation],GetInputCurrentType method, IMFTransform.GetInputCurrentType, IMFTransform::GetInputCurrentType, f3603586-41fd-4eed-9942-28925ed29690, mf.imftransform_getinputcurrenttype, mftransform/IMFTransform::GetInputCurrentType
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
 - IMFTransform::GetInputCurrentType
 - mftransform/IMFTransform::GetInputCurrentType
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
 - IMFTransform.GetInputCurrentType
---

# IMFTransform::GetInputCurrentType


## -description

Gets the current media type for an input stream on this Media Foundation transform (MFT).

## -parameters

### -param dwInputStreamID [in]

Input stream identifier. To get the list of stream identifiers, call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids">IMFTransform::GetStreamIDs</a>.

### -param ppType [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface. The caller must release the interface.

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
<dt><b>MF_E_TRANSFORM_TYPE_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
The input media type has not been set.
              

</td>
</tr>
</table>

## -remarks

If the specified input stream does not yet have a media type, the method returns <b>MF_E_TRANSFORM_TYPE_NOT_SET</b>. Most MFTs do not set any default media types when first created. Instead, the client must set the media type by calling <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype">IMFTransform::SetInputType</a>.
      

If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including mftransform.h, this method is renamed <b>MFTGetInputCurrentType</b>. See <a href="/windows/desktop/medfound/comparison-of-mfts-and-dmos">Creating Hybrid DMO/MFT Objects</a>.

<h3><a id="Implementation_Notes"></a><a id="implementation_notes"></a><a id="IMPLEMENTATION_NOTES"></a>Implementation Notes</h3>
The MFT should return a clone of the media  type, not a pointer to the original type. Otherwise, the caller might modify the type and alter the internal state of the MFT.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>