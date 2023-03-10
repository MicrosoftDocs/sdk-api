---
UID: NF:mftransform.IMFTransform.SetInputType
title: IMFTransform::SetInputType (mftransform.h)
description: Sets, tests, or clears the media type for an input stream on this Media Foundation transform (MFT).
helpviewer_keywords: ["822a83d1-177a-4a8d-842e-eb76f8253283","IMFTransform interface [Media Foundation]","SetInputType method","IMFTransform.SetInputType","IMFTransform::SetInputType","SetInputType","SetInputType method [Media Foundation]","SetInputType method [Media Foundation]","IMFTransform interface","mf.imftransform_setinputtype","mftransform/IMFTransform::SetInputType"]
old-location: mf\imftransform_setinputtype.htm
tech.root: mf
ms.assetid: 822a83d1-177a-4a8d-842e-eb76f8253283
ms.date: 12/05/2018
ms.keywords: 822a83d1-177a-4a8d-842e-eb76f8253283, IMFTransform interface [Media Foundation],SetInputType method, IMFTransform.SetInputType, IMFTransform::SetInputType, SetInputType, SetInputType method [Media Foundation], SetInputType method [Media Foundation],IMFTransform interface, mf.imftransform_setinputtype, mftransform/IMFTransform::SetInputType
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
 - IMFTransform::SetInputType
 - mftransform/IMFTransform::SetInputType
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
 - IMFTransform.SetInputType
---

# IMFTransform::SetInputType


## -description

Sets, tests, or clears the media type for an input stream on this Media Foundation transform (MFT).

## -parameters

### -param dwInputStreamID [in]

Input stream identifier. To get the list of stream identifiers, call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids">IMFTransform::GetStreamIDs</a>.

### -param pType [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface, or <b>NULL</b>.

### -param dwFlags [in]

Zero or more flags from the <a href="/windows/win32/api/mftransform/ne-mftransform-_mft_set_type_flags">_MFT_SET_TYPE_FLAGS</a> enumeration.

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
<dt><b>MF_E_INVALIDMEDIATYPE</b></dt>
</dl>
</td>
<td width="60%">
The MFT cannot use the proposed media type.
              

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
<dt><b>MF_E_INVALIDTYPE</b></dt>
</dl>
</td>
<td width="60%">
The proposed type is not valid. This error code indicates that the media type itself is not configured correctly; for example, it might contain mutually contradictory attributes.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_TRANSFORM_CANNOT_CHANGE_MEDIATYPE_WHILE_PROCESSING</b></dt>
</dl>
</td>
<td width="60%">
The MFT cannot switch types while processing data. Try draining or flushing the MFT.
              

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_UNSUPPORTED_D3D_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The MFT could not find a suitable DirectX Video Acceleration (DXVA) configuration.
              

</td>
</tr>
</table>

## -remarks

This method can be used to set, test without setting, or clear the media type:

<ul>
<li>To set the media type, set <i>dwFlags</i> to zero and set <i>pType</i> to a non-<b>NULL</b> pointer that specifies the media type.
          </li>
<li>To test the media type without setting it, set <i>dwFlags</i> to <b>MFT_SET_TYPE_TEST_ONLY</b> and set <i>pType</i> to a non-<b>NULL</b> pointer that specifies the media type. If the media type is acceptable, the method return <b>S_OK</b>. Otherwise, it returns <b>MF_E_INVALIDMEDIATYPE</b>. Regardless of the return value, the current media type does not change.
          </li>
<li>To clear the media type, set <i>pType</i> to <b>NULL</b>.
          </li>
</ul>
Setting the media type on one stream may change the acceptable types on another stream.
      

An MFT may require the caller to set one or more output types before setting the input type. If so, the method returns <b>MF_E_TRANSFORM_TYPE_NOT_SET</b>.
      

If the MFT supports DirectX Video Acceleration (DXVA) but is unable to find a suitable DXVA configuration (for example, if the graphics driver does not have the right capabilities), the method should return <b>MF_E_UNSUPPORTED_D3D_TYPE</b>. For more information, see <a href="/windows/desktop/medfound/supporting-dxva-2-0-in-media-foundation">Supporting DXVA 2.0 in Media Foundation</a>.
      

If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including mftransform.h, this method is renamed <b>MFTSetInputType</b>. See <a href="/windows/desktop/medfound/comparison-of-mfts-and-dmos">Creating Hybrid DMO/MFT Objects</a>.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>