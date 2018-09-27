---
UID: NF:mftransform.MFCreateTransformActivate
title: MFCreateTransformActivate function
author: windows-sdk-content
description: Creates a generic activation object for Media Foundation transforms (MFTs).
old-location: mf\mfcreatetransformactivate.htm
tech.root: medfound
ms.assetid: 845c7114-756b-4d0f-a92e-9c6e2eba7c94
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: MFCreateTransformActivate, MFCreateTransformActivate function [Media Foundation], mf.mfcreatetransformactivate, mftransform/MFCreateTransformActivate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateTransformActivate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateTransformActivate function


## -description


Creates a generic activation object for Media Foundation transforms (MFTs).


## -parameters




### -param ppActivate [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> interface.
          The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Most applications will not use this function; it is used internally by the <a href="https://msdn.microsoft.com/e065ae51-85dd-48ef-9322-de4ade62c0fe">MFTEnumEx</a> function. 

An <i>activation object</i> is a helper object that creates another object, somewhat similar to a class factory. The <b>MFCreateTransformActivate</b> function creates an activation object for MFTs. Before this activation object can create an MFT, the caller must initialize the activation object by setting one or more attributes on it.

<table>
<tr>
<th>Attribute</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/99ee6f50-1de7-41ea-be5b-135730138d5d">MFT_TRANSFORM_CLSID_Attribute</a>
</td>
<td>Required. Contains the CLSID of the MFT. The activation object creates the MFT by passing this CLSID to the <b>CoCreateInstance</b> function.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/cebd64ea-b20f-4ccc-805f-0deab3096bc3">MF_TRANSFORM_CATEGORY_Attribute</a>
</td>
<td>Optional. Specifies the category of the MFT.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/de377132-19b0-4c8c-882e-193c31420739">MF_TRANSFORM_FLAGS_Attribute</a>
</td>
<td>Contains various flags that describe the MFT. For hardware-based MFTs, set the <b>MFT_ENUM_FLAG_HARDWARE</b> flag. Otherwise, this attribute is optional.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/1df40a42-4c02-473f-a87f-2ae2d42e4f4e">MFT_CODEC_MERIT_Attribute</a>
</td>
<td>
Optional. Contains the merit value of a hardware codec.

If this attribute is set and its value is greater than zero, the activation object calls <a href="https://msdn.microsoft.com/69029cf3-7f34-4bb1-8dfd-fa9a8d1a63c9">MFGetMFTMerit</a> to get the trusted merit value for the MFT. If the trusted merit is less than the value of this attribute, the activation object's <a href="https://msdn.microsoft.com/120b8070-6732-450d-8334-b3910f7bb4d2">IMFActivate::ActivateObject</a> method fails and returns <b>MF_E_INVALID_CODEC_MERIT</b>.

</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/7e153051-a167-4ff7-8178-b290d8a1345e">MFT_ENUM_HARDWARE_URL_Attribute</a>
</td>
<td>Required for hardware-based MFTs. Specifies the symbolic link for the hardware device. The device proxy uses this value to configure the MFT.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/7f48967e-375a-4019-b14f-2f457b616cc0">MFT_FIELDOFUSE_UNLOCK_Attribute</a>
</td>
<td>
Optional. Contains an <a href="https://msdn.microsoft.com/b144589b-d559-4686-b617-0e3c393380e9">IMFFieldOfUseMFTUnlock</a> pointer, which can be used to unlock the MFT. The <b>IMFFieldOfUseMFTUnlock</b> interface is used with MFTs that have usage restrictions.

If this attribute is set and the <a href="https://msdn.microsoft.com/de377132-19b0-4c8c-882e-193c31420739">MF_TRANSFORM_FLAGS_Attribute</a>  attribute contains the <b>MFT_ENUM_FLAG_FIELDOFUSE</b> flag, the activation object calls <a href="https://msdn.microsoft.com/54b15e72-6551-4162-90ca-a9bed68ca62f">IMFFieldOfUseMFTUnlock::Unlock</a> when it creates the MFT. An application can also set the <a href="https://msdn.microsoft.com/7f48967e-375a-4019-b14f-2f457b616cc0">MFT_FIELDOFUSE_UNLOCK_Attribute</a> attribute without setting the <b>MFT_ENUM_FLAG_FIELDOFUSE</b> flag. In that case, the application must call <b>Unlock</b>.

</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/f9bd8a50-e43e-4668-86a0-c9d5f517f4cf">MFT_PREFERRED_ENCODER_PROFILE</a>
</td>
<td>
Optional. Contains the encoding profile for an encoder. The value of this attribute is an <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> pointer.

If this attribute is set and the value of the <a href="https://msdn.microsoft.com/cebd64ea-b20f-4ccc-805f-0deab3096bc3">MF_TRANSFORM_CATEGORY_Attribute</a> attribute is <b>MFT_CATEGORY_AUDIO_ENCODER</b> or <b>MFT_CATEGORY_VIDEO_ENCODER</b>, the activation object uses the encoding profile to configure the MFT. The MFT must expose either <b>ICodecAPI</b>  or <b>IPropertyStore</b> for this purpose.

</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/36a09696-3fe7-41a0-93f1-712220f88b04">MFT_PREFERRED_OUTPUTTYPE_Attribute</a>
</td>
<td>
Optional. Specifies the preferred output format for an encoder.

If this attribute set and the value of the <a href="https://msdn.microsoft.com/cebd64ea-b20f-4ccc-805f-0deab3096bc3">MF_TRANSFORM_CATEGORY_Attribute</a> attribute is <b>MFT_CATEGORY_AUDIO_ENCODER</b> or <b>MFT_CATEGORY_VIDEO_ENCODER</b>, the activation object sets this media type on the MFT.

</td>
</tr>
</table>
 

For more information about activation objects, see <a href="https://msdn.microsoft.com/767d5f1c-2b8d-43b6-916b-035129e93204">Activation Objects</a>.  




## -see-also




<a href="https://msdn.microsoft.com/767d5f1c-2b8d-43b6-916b-035129e93204">Activation Objects</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>
 

 

