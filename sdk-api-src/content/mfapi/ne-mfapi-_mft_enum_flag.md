---
UID: NE:mfapi._MFT_ENUM_FLAG
title: _MFT_ENUM_FLAG (mfapi.h)
description: Contains flags for registering and enumeration Media Foundation transforms (MFTs).
helpviewer_keywords: ["MFT_ENUM_FLAG_ALL","MFT_ENUM_FLAG_ASYNCMFT","MFT_ENUM_FLAG_FIELDOFUSE","MFT_ENUM_FLAG_HARDWARE","MFT_ENUM_FLAG_LOCALMFT","MFT_ENUM_FLAG_SORTANDFILTER","MFT_ENUM_FLAG_SYNCMFT","MFT_ENUM_FLAG_TRANSCODE_ONLY","_MFT_ENUM_FLAG","_MFT_ENUM_FLAG enumeration [Media Foundation]","mf._mft_enum_flag","mfapi/MFT_ENUM_FLAG_ALL","mfapi/MFT_ENUM_FLAG_ASYNCMFT","mfapi/MFT_ENUM_FLAG_FIELDOFUSE","mfapi/MFT_ENUM_FLAG_HARDWARE","mfapi/MFT_ENUM_FLAG_LOCALMFT","mfapi/MFT_ENUM_FLAG_SORTANDFILTER","mfapi/MFT_ENUM_FLAG_SYNCMFT","mfapi/MFT_ENUM_FLAG_TRANSCODE_ONLY","mfapi/_MFT_ENUM_FLAG"]
old-location: mf\_mft_enum_flag.htm
tech.root: mf
ms.assetid: ba39fb66-d8b6-49c1-8312-18ebdcb012c9
ms.date: 12/05/2018
ms.keywords: MFT_ENUM_FLAG_ALL, MFT_ENUM_FLAG_ASYNCMFT, MFT_ENUM_FLAG_FIELDOFUSE, MFT_ENUM_FLAG_HARDWARE, MFT_ENUM_FLAG_LOCALMFT, MFT_ENUM_FLAG_SORTANDFILTER, MFT_ENUM_FLAG_SYNCMFT, MFT_ENUM_FLAG_TRANSCODE_ONLY, _MFT_ENUM_FLAG, _MFT_ENUM_FLAG enumeration [Media Foundation], mf._mft_enum_flag, mfapi/MFT_ENUM_FLAG_ALL, mfapi/MFT_ENUM_FLAG_ASYNCMFT, mfapi/MFT_ENUM_FLAG_FIELDOFUSE, mfapi/MFT_ENUM_FLAG_HARDWARE, mfapi/MFT_ENUM_FLAG_LOCALMFT, mfapi/MFT_ENUM_FLAG_SORTANDFILTER, mfapi/MFT_ENUM_FLAG_SYNCMFT, mfapi/MFT_ENUM_FLAG_TRANSCODE_ONLY, mfapi/_MFT_ENUM_FLAG
req.header: mfapi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFT_ENUM_FLAG
 - mfapi/_MFT_ENUM_FLAG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - _MFT_ENUM_FLAG
---

# _MFT_ENUM_FLAG enumeration


## -description

Contains flags for registering and enumeration Media Foundation transforms (MFTs).

These flags are used in the following functions:
<ul>
<li>
<a href="/windows/desktop/api/mfapi/nf-mfapi-mftenumex">MFTEnumEx</a>: These flags control which Media Foundation transforms (MFTs) are enumerated, as well as the enumeration order.</li>
<li>
<a href="/windows/desktop/api/mfapi/nf-mfapi-mftregister">MFTRegister</a>: A subset of these flags are used when registering an MFT.</li>
</ul>

## -enum-fields

### -field MFT_ENUM_FLAG_SYNCMFT:0x00000001

The MFT performs synchronous data processing in software. 

This flag does not apply to hardware transforms.

### -field MFT_ENUM_FLAG_ASYNCMFT:0x00000002

The MFT performs asynchronous data processing in software. See <a href="/windows/desktop/medfound/asynchronous-mfts">Asynchronous MFTs</a>.

This flag does not apply to hardware transforms.

### -field MFT_ENUM_FLAG_HARDWARE:0x00000004

The MFT performs hardware-based data processing, using either the AVStream driver or a GPU-based proxy MFT. MFTs in this category always process data asynchronously. See <a href="/windows/desktop/medfound/hardware-mfts">Hardware MFTs</a>.

<div class="alert"><b>Note</b>  This flag applies to video codecs and video processors that perform their work entirely in hardware. It does not apply to software decoders that use DirectX Video Acceleration to assist decoding.</div>
<div> </div>

### -field MFT_ENUM_FLAG_FIELDOFUSE:0x00000008

The MFT that must be unlocked by the application before use. Unlocking is performed using the <a href="/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock">IMFFieldOfUseMFTUnlock</a> interface. For more information, see <a href="/windows/desktop/medfound/field-of-use-restrictions">Field of Use Restrictions</a>.

This flag does not apply to hardware transforms.

### -field MFT_ENUM_FLAG_LOCALMFT:0x00000010

For enumeration, include MFTs that were registered in the caller's process. To register an MFT in the caller's process, call the either the <a href="/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal">MFTRegisterLocal</a> or <a href="/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid">MFTRegisterLocalByCLSID</a> function.

This flag does not apply to hardware transforms.

Do not set this flag in the <a href="/windows/desktop/api/mfapi/nf-mfapi-mftregister">MFTRegister</a> function.

### -field MFT_ENUM_FLAG_TRANSCODE_ONLY:0x00000020

The MFT is optimized for transcoding rather than playback.

### -field MFT_ENUM_FLAG_SORTANDFILTER:0x00000040

For enumeration, sort and filter the results. For more information, see the Remarks section of <a href="/windows/desktop/api/mfapi/nf-mfapi-mftenumex">MFTEnumEx</a>.

Do not set this flag in the <a href="/windows/desktop/api/mfapi/nf-mfapi-mftregister">MFTRegister</a> function.

### -field MFT_ENUM_FLAG_SORTANDFILTER_APPROVED_ONLY:0x000000C0

### -field MFT_ENUM_FLAG_SORTANDFILTER_WEB_ONLY:0x00000140

### -field MFT_ENUM_FLAG_SORTANDFILTER_WEB_ONLY_EDGEMODE:0x00000240

### -field MFT_ENUM_FLAG_UNTRUSTED_STOREMFT:0x00000400

### -field MFT_ENUM_FLAG_ALL:0x0000003F

Bitwise <b>OR</b> of all the flags, excluding <b>MFT_ENUM_FLAG_SORTANDFILTER</b>.

Do not set this flag in the <a href="/windows/desktop/api/mfapi/nf-mfapi-mftregister">MFTRegister</a> function.

## -remarks

For registration, these flags describe the MFT that is being registered. Some flags do not apply in that context. For enumeration, these flags control which MFTs are selected in the enumeration. For more details about the precise meaning of these flags, see the reference topics for <a href="/windows/desktop/api/mfapi/nf-mfapi-mftregister">MFTRegister</a> and <a href="/windows/desktop/api/mfapi/nf-mfapi-mftenumex">MFTEnumEx</a>


For registration, the <b>MFT_ENUM_FLAG_SYNCMFT</b>,  <b>MFT_ENUM_FLAG_ASYNCMFT</b>, and <b>MFT_ENUM_FLAG_HARDWARE</b> flags are mutually exclusive. For enumeration, these three flags can be combined.

## -see-also

<a href="/windows/desktop/medfound/field-of-use-restrictions">Field of Use Restrictions</a>



<a href="/windows/desktop/api/mfapi/nf-mfapi-mftenumex">MFTEnumEx</a>



<a href="/windows/desktop/api/mfapi/nf-mfapi-mftregister">MFTRegister</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
