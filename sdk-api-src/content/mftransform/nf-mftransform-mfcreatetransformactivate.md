---
UID: NF:mftransform.MFCreateTransformActivate
title: MFCreateTransformActivate function (mftransform.h)
description: Creates a generic activation object for Media Foundation transforms (MFTs).
helpviewer_keywords: ["MFCreateTransformActivate","MFCreateTransformActivate function [Media Foundation]","mf.mfcreatetransformactivate","mftransform/MFCreateTransformActivate"]
old-location: mf\mfcreatetransformactivate.htm
tech.root: mf
ms.assetid: 845c7114-756b-4d0f-a92e-9c6e2eba7c94
ms.date: 12/05/2018
ms.keywords: MFCreateTransformActivate, MFCreateTransformActivate function [Media Foundation], mf.mfcreatetransformactivate, mftransform/MFCreateTransformActivate
req.header: mftransform.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateTransformActivate
 - mftransform/MFCreateTransformActivate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateTransformActivate
---

# MFCreateTransformActivate function


## -description

Creates a generic activation object for Media Foundation transforms (MFTs).

## -parameters

### -param ppActivate [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> interface.
          The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Most applications will not use this function; it is used internally by the <a href="/windows/desktop/api/mfapi/nf-mfapi-mftenumex">MFTEnumEx</a> function. 

An <i>activation object</i> is a helper object that creates another object, somewhat similar to a class factory. The <b>MFCreateTransformActivate</b> function creates an activation object for MFTs. Before this activation object can create an MFT, the caller must initialize the activation object by setting one or more attributes on it.

<table>
<tr>
<th>Attribute</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mft-transform-clsid-attribute">MFT_TRANSFORM_CLSID_Attribute</a>
</td>
<td>Required. Contains the CLSID of the MFT. The activation object creates the MFT by passing this CLSID to the <b>CoCreateInstance</b> function.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mf-transform-category-attribute">MF_TRANSFORM_CATEGORY_Attribute</a>
</td>
<td>Optional. Specifies the category of the MFT.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mf-transform-flags-attribute">MF_TRANSFORM_FLAGS_Attribute</a>
</td>
<td>Contains various flags that describe the MFT. For hardware-based MFTs, set the <b>MFT_ENUM_FLAG_HARDWARE</b> flag. Otherwise, this attribute is optional.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mft-codec-merit-attribute">MFT_CODEC_MERIT_Attribute</a>
</td>
<td>
Optional. Contains the merit value of a hardware codec.

If this attribute is set and its value is greater than zero, the activation object calls <a href="/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit">MFGetMFTMerit</a> to get the trusted merit value for the MFT. If the trusted merit is less than the value of this attribute, the activation object's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject">IMFActivate::ActivateObject</a> method fails and returns <b>MF_E_INVALID_CODEC_MERIT</b>.

</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mft-enum-hardware-url-attribute">MFT_ENUM_HARDWARE_URL_Attribute</a>
</td>
<td>Required for hardware-based MFTs. Specifies the symbolic link for the hardware device. The device proxy uses this value to configure the MFT.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mft-fieldofuse-unlock-attribute">MFT_FIELDOFUSE_UNLOCK_Attribute</a>
</td>
<td>
Optional. Contains an <a href="/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock">IMFFieldOfUseMFTUnlock</a> pointer, which can be used to unlock the MFT. The <b>IMFFieldOfUseMFTUnlock</b> interface is used with MFTs that have usage restrictions.

If this attribute is set and the <a href="/windows/desktop/medfound/mf-transform-flags-attribute">MF_TRANSFORM_FLAGS_Attribute</a>  attribute contains the <b>MFT_ENUM_FLAG_FIELDOFUSE</b> flag, the activation object calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock">IMFFieldOfUseMFTUnlock::Unlock</a> when it creates the MFT. An application can also set the <a href="/windows/desktop/medfound/mft-fieldofuse-unlock-attribute">MFT_FIELDOFUSE_UNLOCK_Attribute</a> attribute without setting the <b>MFT_ENUM_FLAG_FIELDOFUSE</b> flag. In that case, the application must call <b>Unlock</b>.

</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mft-preferred-encoder-profile">MFT_PREFERRED_ENCODER_PROFILE</a>
</td>
<td>
Optional. Contains the encoding profile for an encoder. The value of this attribute is an <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> pointer.

If this attribute is set and the value of the <a href="/windows/desktop/medfound/mf-transform-category-attribute">MF_TRANSFORM_CATEGORY_Attribute</a> attribute is <b>MFT_CATEGORY_AUDIO_ENCODER</b> or <b>MFT_CATEGORY_VIDEO_ENCODER</b>, the activation object uses the encoding profile to configure the MFT. The MFT must expose either <b>ICodecAPI</b>  or <b>IPropertyStore</b> for this purpose.

</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mft-preferred-outputtype-attribute">MFT_PREFERRED_OUTPUTTYPE_Attribute</a>
</td>
<td>
Optional. Specifies the preferred output format for an encoder.

If this attribute set and the value of the <a href="/windows/desktop/medfound/mf-transform-category-attribute">MF_TRANSFORM_CATEGORY_Attribute</a> attribute is <b>MFT_CATEGORY_AUDIO_ENCODER</b> or <b>MFT_CATEGORY_VIDEO_ENCODER</b>, the activation object sets this media type on the MFT.

</td>
</tr>
</table>
 

For more information about activation objects, see <a href="/windows/desktop/medfound/activation-objects">Activation Objects</a>.

## -see-also

<a href="/windows/desktop/medfound/activation-objects">Activation Objects</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>