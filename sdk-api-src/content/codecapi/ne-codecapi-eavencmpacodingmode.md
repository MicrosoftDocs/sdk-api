---
UID: NE:codecapi.eAVEncMPACodingMode
title: eAVEncMPACodingMode (codecapi.h)
description: Specifies the MPEG audio encoding mode. This enumeration is used with the AVEncMPACodingMode property.
old-location: dshow\eavencmpacodingmode.htm
tech.root: DirectShow
ms.assetid: 37c3309b-05ea-4c78-b447-196d16c0f0cd
ms.date: 12/05/2018
ms.keywords: codecapi/eAVEncMPACodingMode, codecapi/eAVEncMPACodingMode_DualChannel, codecapi/eAVEncMPACodingMode_JointStereo, codecapi/eAVEncMPACodingMode_Mono, codecapi/eAVEncMPACodingMode_Stereo, codecapi/eAVEncMPACodingMode_Surround, dshow.eavencmpacodingmode, eAVEncMPACodingMode, eAVEncMPACodingMode enumeration [DirectShow], eAVEncMPACodingModeEnumeration, eAVEncMPACodingMode_DualChannel, eAVEncMPACodingMode_JointStereo, eAVEncMPACodingMode_Mono, eAVEncMPACodingMode_Stereo, eAVEncMPACodingMode_Surround
ms.topic: enum
f1_keywords:
- codecapi/eAVEncMPACodingMode
dev_langs:
- c++
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
- codecapi.h
api_name:
- eAVEncMPACodingMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# eAVEncMPACodingMode enumeration


## -description



Specifies the MPEG audio encoding mode. This enumeration is used with the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/avencmpacodingmode-property">AVEncMPACodingMode</a> property.




## -enum-fields




### -field eAVEncMPACodingMode_Mono

Single channel.
          This mode corresponds to single_channel mode (bit code '11'), defined in ISO/IEC 11172-3.


### -field eAVEncMPACodingMode_Stereo

Stereo channels.
          This mode corresponds to stereo mode ('00'), defined in ISO/IEC 11172-3.


### -field eAVEncMPACodingMode_DualChannel

Two mono channels.
          This mode corresponds to dual_channel mode ('10'), defined in ISO/IEC 11172-3.


### -field eAVEncMPACodingMode_JointStereo

Joint stereo mode. This mode uses similarities between the two channels to achieve greater compression. This mode corresponds to joint_stereo mode ('01'), defined in ISO/IEC 11172-3.


### -field eAVEncMPACodingMode_Surround

Surround audio (5.1 channels).
          This mode applies to MPEG-2 audio (ISO/IEC 13818-3).


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
 

 

