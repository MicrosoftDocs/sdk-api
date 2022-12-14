---
UID: NF:mfapi.MFTRegister
title: MFTRegister function (mfapi.h)
description: Adds information about a Media Foundation transform (MFT) to the registry.
helpviewer_keywords: ["MFTRegister","MFTRegister function [Media Foundation]","MFT_CODEC_MERIT_Attribute","MFT_ENUM_FLAG_ASYNCMFT","MFT_ENUM_FLAG_FIELDOFUSE","MFT_ENUM_FLAG_HARDWARE","MFT_ENUM_FLAG_SYNCMFT","MFT_ENUM_FLAG_TRANSCODE_ONLY","fb3a2b67-d3e4-4d5f-960a-3979f4780904","mf.mftregister","mfapi/MFTRegister"]
old-location: mf\mftregister.htm
tech.root: mf
ms.assetid: fb3a2b67-d3e4-4d5f-960a-3979f4780904
ms.date: 12/05/2018
ms.keywords: MFTRegister, MFTRegister function [Media Foundation], MFT_CODEC_MERIT_Attribute, MFT_ENUM_FLAG_ASYNCMFT, MFT_ENUM_FLAG_FIELDOFUSE, MFT_ENUM_FLAG_HARDWARE, MFT_ENUM_FLAG_SYNCMFT, MFT_ENUM_FLAG_TRANSCODE_ONLY, fb3a2b67-d3e4-4d5f-960a-3979f4780904, mf.mftregister, mfapi/MFTRegister
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - MFTRegister
 - mfapi/MFTRegister
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
 - MFTRegister
---

# MFTRegister function


## -description

Adds information about a Media Foundation transform (MFT) to the registry.
        

Applications can enumerate the MFT by calling the <a href="/windows/desktop/api/mfapi/nf-mfapi-mftenum">MFTEnum</a> or <a href="/windows/desktop/api/mfapi/nf-mfapi-mftenumex">MFTEnumEx</a> function.

## -parameters

### -param clsidMFT [in]

The CLSID of the MFT.
          The MFT must also be registered as a COM object using the same CLSID.

### -param guidCategory [in]

GUID that specifies the category of the MFT. For a list of MFT categories, see <a href="/windows/desktop/medfound/mft-category">MFT_CATEGORY</a>.

### -param pszName [in]

Wide-character string that contains the friendly name of the MFT.

### -param Flags [in]

Bitwise <b>OR</b> of zero or more of the following flags from the <a href="/windows/win32/api/mfapi/ne-mfapi-_mft_enum_flag">_MFT_ENUM_FLAG</a>  enumeration:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MFT_ENUM_FLAG_ASYNCMFT"></a><a id="mft_enum_flag_asyncmft"></a><dl>
<dt><b>MFT_ENUM_FLAG_ASYNCMFT</b></dt>
</dl>
</td>
<td width="60%">
The MFT performs asynchronous processing in software. See <a href="/windows/desktop/medfound/asynchronous-mfts">Asynchronous MFTs</a>. This flag does not apply to hardware transforms.

Requires Windows 7.

</td>
</tr>
<tr>
<td width="40%"><a id="MFT_ENUM_FLAG_FIELDOFUSE"></a><a id="mft_enum_flag_fieldofuse"></a><dl>
<dt><b>MFT_ENUM_FLAG_FIELDOFUSE</b></dt>
</dl>
</td>
<td width="60%">
The application must unlock the MFT in order to use it. See <a href="/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock">IMFFieldOfUseMFTUnlock</a>.

Requires Windows 7.

</td>
</tr>
<tr>
<td width="40%"><a id="MFT_ENUM_FLAG_HARDWARE"></a><a id="mft_enum_flag_hardware"></a><dl>
<dt><b>MFT_ENUM_FLAG_HARDWARE</b></dt>
</dl>
</td>
<td width="60%">
The MFT performs hardware-based data processing, using either the AVStream driver or a GPU-based proxy MFT. MFTs in this category always process data asynchronously. See <a href="/windows/desktop/medfound/hardware-mfts">Hardware MFTs</a>.

<div class="alert"><b>Note</b>  This flag applies to video codecs and video processors that perform their work entirely in hardware. It does not apply to software decoders that use DirectX Video Acceleration to assist decoding.</div>
<div> </div>
Requires Windows 7.

</td>
</tr>
<tr>
<td width="40%"><a id="MFT_ENUM_FLAG_SYNCMFT"></a><a id="mft_enum_flag_syncmft"></a><dl>
<dt><b>MFT_ENUM_FLAG_SYNCMFT</b></dt>
</dl>
</td>
<td width="60%">
The MFT performs synchronous processing in software. This flag does not apply to hardware transforms.

</td>
</tr>
<tr>
<td width="40%"><a id="MFT_ENUM_FLAG_TRANSCODE_ONLY"></a><a id="mft_enum_flag_transcode_only"></a><dl>
<dt><b>MFT_ENUM_FLAG_TRANSCODE_ONLY</b></dt>
</dl>
</td>
<td width="60%">
The MFT is optimized for transcoding and should not be used for playback.

Requires Windows 7.

</td>
</tr>
</table>
 

Setting <i>Flags</i> to zero is  equivalent to setting the <b>MFT_ENUM_FLAG_SYNCMFT</b> flag. The default processing model for MFTs is synchronous processing.

Prior to Windows 7, the <i>Flags</i> parameter was reserved.

### -param cInputTypes [in]

Number of elements in the <i>pInputTypes</i> array.

### -param pInputTypes [in]

Pointer to an array of <a href="/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info">MFT_REGISTER_TYPE_INFO</a> structures. Each member of the array specifies an input format that the MFT supports.  This parameter can be <b>NULL</b>.

This parameter can be <b>NULL</b>. However, if the parameter is <b>NULL</b>, the MFT will be enumerated only when an application specifies <b>NULL</b> for the desired input type.

### -param cOutputTypes [in]

Number of elements in the <i>pOutputTypes</i> array.

### -param pOutputTypes [in]

Pointer to an array of <a href="/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info">MFT_REGISTER_TYPE_INFO</a> structures. Each member of the array defines an output format that the MFT supports. 

This parameter can be <b>NULL</b>. However, if the parameter is <b>NULL</b>, the MFT will be enumerated only when an application specifies <b>NULL</b> for the desired output type.

### -param pAttributes [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of an attribute store that contains additional registry information. This parameter can be <b>NULL</b>. If the parameter is non-<b>NULL</b>, the attributes are written to the registry as a byte array.
      You can use the <a href="/windows/desktop/api/mfapi/nf-mfapi-mftgetinfo">MFTGetInfo</a> function to retrieve the attributes.

The following attribute is defined for this parameter:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MFT_CODEC_MERIT_Attribute"></a><a id="mft_codec_merit_attribute"></a><a id="MFT_CODEC_MERIT_ATTRIBUTE"></a><dl>
<dt><b><a href="/windows/desktop/medfound/mft-codec-merit-attribute">MFT_CODEC_MERIT_Attribute</a></b></dt>
</dl>
</td>
<td width="60%">
Contains the merit value of a hardware codec. See <a href="/windows/desktop/medfound/codec-merit">Codec Merit</a>.

</td>
</tr>
</table>

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The registry entries created by this function are read by the following functions: 

<table>
<tr>
<th>Function</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/mfapi/nf-mfapi-mftenum">MFTEnum</a>
</td>
<td>Enumerates MFTs by media type and category.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/mfapi/nf-mfapi-mftenumex">MFTEnumEx</a>
</td>
<td>Extended version of <a href="/windows/desktop/api/mfapi/nf-mfapi-mftenum">MFTEnum</a>.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/mfapi/nf-mfapi-mftgetinfo">MFTGetInfo</a>
</td>
<td>Looks up an MFT by CLSID and retrieves the registry information.</td>
</tr>
</table>
 

This function does not register the CLSID of the MFT for the <b>CoCreateInstance</b> or <b>CoGetClassObject</b> functions.
      

To remove the entries from the registry, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mftunregister">MFTUnregister</a>.
      If you remove an MFT from the system, you should always call <b>MFTUnregister</b>.

The formats given in the <i>pInputTypes</i> and <i>pOutputTypes</i> parameters are intended to help applications search for MFTs by format. Applications can use the <a href="/windows/desktop/api/mfapi/nf-mfapi-mftenum">MFTEnum</a> or <a href="/windows/desktop/api/mfapi/nf-mfapi-mftenumex">MFTEnumEx</a> functions to enumerate MFTs that match a particular set of formats.

It is recommended 
        to specify at least one input type in <i>pInputTypes</i> and one output type in the <i>pOutputTypes</i> parameter. Otherwise, the MFT might be skipped in the enumeration.

On 64-bit Windows, the 32-bit version of this function registers the MFT in the 32-bit node of the registry. For more information, see <a href="/windows/desktop/SysInfo/32-bit-and-64-bit-application-data-in-the-registry">32-bit and 64-bit Application Data in the Registry</a>.

## -see-also

<a href="/windows/desktop/api/mfapi/nf-mfapi-mftenumex">MFTEnumEx</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>



<a href="/windows/win32/api/mfapi/ne-mfapi-_mft_enum_flag">_MFT_ENUM_FLAG</a>