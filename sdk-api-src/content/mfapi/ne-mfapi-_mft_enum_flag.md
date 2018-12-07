---
UID: NE:mfapi._MFT_ENUM_FLAG
title: "_MFT_ENUM_FLAG"
author: windows-sdk-content
description: Contains flags for registering and enumeration Media Foundation transforms (MFTs).
old-location: mf\_mft_enum_flag.htm
tech.root: medfound
ms.assetid: ba39fb66-d8b6-49c1-8312-18ebdcb012c9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MFT_ENUM_FLAG_ALL, MFT_ENUM_FLAG_ASYNCMFT, MFT_ENUM_FLAG_FIELDOFUSE, MFT_ENUM_FLAG_HARDWARE, MFT_ENUM_FLAG_LOCALMFT, MFT_ENUM_FLAG_SORTANDFILTER, MFT_ENUM_FLAG_SYNCMFT, MFT_ENUM_FLAG_TRANSCODE_ONLY, _MFT_ENUM_FLAG, _MFT_ENUM_FLAG enumeration [Media Foundation], mf._mft_enum_flag, mfapi/MFT_ENUM_FLAG_ALL, mfapi/MFT_ENUM_FLAG_ASYNCMFT, mfapi/MFT_ENUM_FLAG_FIELDOFUSE, mfapi/MFT_ENUM_FLAG_HARDWARE, mfapi/MFT_ENUM_FLAG_LOCALMFT, mfapi/MFT_ENUM_FLAG_SORTANDFILTER, mfapi/MFT_ENUM_FLAG_SYNCMFT, mfapi/MFT_ENUM_FLAG_TRANSCODE_ONLY, mfapi/_MFT_ENUM_FLAG
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - _MFT_ENUM_FLAG
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# _MFT_ENUM_FLAG enumeration


## -description


Contains flags for registering and enumeration Media Foundation transforms (MFTs).

These flags are used in the following functions:
<ul>
<li>
<a href="https://msdn.microsoft.com/e065ae51-85dd-48ef-9322-de4ade62c0fe">MFTEnumEx</a>: These flags control which Media Foundation transforms (MFTs) are enumerated, as well as the enumeration order.</li>
<li>
<a href="https://msdn.microsoft.com/fb3a2b67-d3e4-4d5f-960a-3979f4780904">MFTRegister</a>: A subset of these flags are used when registering an MFT.</li>
</ul>

## -enum-fields




### -field MFT_ENUM_FLAG_SYNCMFT

The MFT performs synchronous data processing in software. 

This flag does not apply to hardware transforms.


### -field MFT_ENUM_FLAG_ASYNCMFT

The MFT performs asynchronous data processing in software. See <a href="https://msdn.microsoft.com/d438ffae-fc50-454f-8ce4-2d6676500fff">Asynchronous MFTs</a>.

This flag does not apply to hardware transforms.


### -field MFT_ENUM_FLAG_HARDWARE

The MFT performs hardware-based data processing, using either the AVStream driver or a GPU-based proxy MFT. MFTs in this category always process data asynchronously. See <a href="https://msdn.microsoft.com/9922d403-5d0d-433f-ad9f-c86142ac0f46">Hardware MFTs</a>.

<div class="alert"><b>Note</b>  This flag applies to video codecs and video processors that perform their work entirely in hardware. It does not apply to software decoders that use DirectX Video Acceleration to assist decoding.</div>
<div> </div>

### -field MFT_ENUM_FLAG_FIELDOFUSE

The MFT that must be unlocked by the application before use. Unlocking is performed using the <a href="https://msdn.microsoft.com/b144589b-d559-4686-b617-0e3c393380e9">IMFFieldOfUseMFTUnlock</a> interface. For more information, see <a href="https://msdn.microsoft.com/36f28e4c-2baf-4618-9935-5d4615f6bc77">Field of Use Restrictions</a>.

This flag does not apply to hardware transforms.


### -field MFT_ENUM_FLAG_LOCALMFT

For enumeration, include MFTs that were registered in the caller's process. To register an MFT in the caller's process, call the either the <a href="https://msdn.microsoft.com/802f7083-e224-4e5c-8a35-3e93da0cbd91">MFTRegisterLocal</a> or <a href="https://msdn.microsoft.com/80c45ac3-4487-41bf-a5f5-f459db3cd700">MFTRegisterLocalByCLSID</a> function.

This flag does not apply to hardware transforms.

Do not set this flag in the <a href="https://msdn.microsoft.com/fb3a2b67-d3e4-4d5f-960a-3979f4780904">MFTRegister</a> function.


### -field MFT_ENUM_FLAG_TRANSCODE_ONLY

The MFT is optimized for transcoding rather than playback.


### -field MFT_ENUM_FLAG_SORTANDFILTER

For enumeration, sort and filter the results. For more information, see the Remarks section of <a href="https://msdn.microsoft.com/e065ae51-85dd-48ef-9322-de4ade62c0fe">MFTEnumEx</a>.

Do not set this flag in the <a href="https://msdn.microsoft.com/fb3a2b67-d3e4-4d5f-960a-3979f4780904">MFTRegister</a> function.


### -field MFT_ENUM_FLAG_SORTANDFILTER_APPROVED_ONLY


### -field MFT_ENUM_FLAG_SORTANDFILTER_WEB_ONLY


### -field MFT_ENUM_FLAG_SORTANDFILTER_WEB_ONLY_EDGEMODE


### -field MFT_ENUM_FLAG_UNTRUSTED_STOREMFT


### -field MFT_ENUM_FLAG_ALL

Bitwise <b>OR</b> of all the flags, excluding <b>MFT_ENUM_FLAG_SORTANDFILTER</b>.

Do not set this flag in the <a href="https://msdn.microsoft.com/fb3a2b67-d3e4-4d5f-960a-3979f4780904">MFTRegister</a> function.


## -remarks



For registration, these flags describe the MFT that is being registered. Some flags do not apply in that context. For enumeration, these flags control which MFTs are selected in the enumeration. For more details about the precise meaning of these flags, see the reference topics for <a href="https://msdn.microsoft.com/fb3a2b67-d3e4-4d5f-960a-3979f4780904">MFTRegister</a> and <a href="https://msdn.microsoft.com/e065ae51-85dd-48ef-9322-de4ade62c0fe">MFTEnumEx</a>


For registration, the <b>MFT_ENUM_FLAG_SYNCMFT</b>,  <b>MFT_ENUM_FLAG_ASYNCMFT</b>, and <b>MFT_ENUM_FLAG_HARDWARE</b> flags are mutually exclusive. For enumeration, these three flags can be combined.




## -see-also




<a href="https://msdn.microsoft.com/36f28e4c-2baf-4618-9935-5d4615f6bc77">Field of Use Restrictions</a>



<a href="https://msdn.microsoft.com/e065ae51-85dd-48ef-9322-de4ade62c0fe">MFTEnumEx</a>



<a href="https://msdn.microsoft.com/fb3a2b67-d3e4-4d5f-960a-3979f4780904">MFTRegister</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

