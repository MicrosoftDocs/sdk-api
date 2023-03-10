---
UID: NE:codecapi.eAVDecVideoSoftwareDeinterlaceMode
title: eAVDecVideoSoftwareDeinterlaceMode (codecapi.h)
description: Specifies a video decoder's software deinterlace mode. This enumeration is used with the AVDecVideoSoftwareDeinterlaceMode property.
helpviewer_keywords: ["codecapi/eAVDecVideoSoftwareDeinterlaceMode","codecapi/eAVDecVideoSoftwareDeinterlaceMode_BOBDeinterlacing","codecapi/eAVDecVideoSoftwareDeinterlaceMode_NoDeinterlacing","codecapi/eAVDecVideoSoftwareDeinterlaceMode_ProgressiveDeinterlacing","codecapi/eAVDecVideoSoftwareDeinterlaceMode_SmartBOBDeinterlacing","dshow.eavdecvideosoftwaredeinterlacemode","eAVDecVideoSoftwareDeinterlaceMode","eAVDecVideoSoftwareDeinterlaceMode enumeration [DirectShow]","eAVDecVideoSoftwareDeinterlaceMode_BOBDeinterlacing","eAVDecVideoSoftwareDeinterlaceMode_NoDeinterlacing","eAVDecVideoSoftwareDeinterlaceMode_ProgressiveDeinterlacing","eAVDecVideoSoftwareDeinterlaceMode_SmartBOBDeinterlacing"]
old-location: dshow\eavdecvideosoftwaredeinterlacemode.htm
tech.root: dshow
ms.assetid: 3c72e714-1252-4c8b-9371-58f995e5b163
ms.date: 12/05/2018
ms.keywords: codecapi/eAVDecVideoSoftwareDeinterlaceMode, codecapi/eAVDecVideoSoftwareDeinterlaceMode_BOBDeinterlacing, codecapi/eAVDecVideoSoftwareDeinterlaceMode_NoDeinterlacing, codecapi/eAVDecVideoSoftwareDeinterlaceMode_ProgressiveDeinterlacing, codecapi/eAVDecVideoSoftwareDeinterlaceMode_SmartBOBDeinterlacing, dshow.eavdecvideosoftwaredeinterlacemode, eAVDecVideoSoftwareDeinterlaceMode, eAVDecVideoSoftwareDeinterlaceMode enumeration [DirectShow], eAVDecVideoSoftwareDeinterlaceMode_BOBDeinterlacing, eAVDecVideoSoftwareDeinterlaceMode_NoDeinterlacing, eAVDecVideoSoftwareDeinterlaceMode_ProgressiveDeinterlacing, eAVDecVideoSoftwareDeinterlaceMode_SmartBOBDeinterlacing
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - eAVDecVideoSoftwareDeinterlaceMode
 - codecapi/eAVDecVideoSoftwareDeinterlaceMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - codecapi.h
api_name:
 - eAVDecVideoSoftwareDeinterlaceMode
---

# eAVDecVideoSoftwareDeinterlaceMode enumeration


## -description

Specifies a video decoder's software deinterlace mode. This enumeration is used with the <a href="/windows/desktop/DirectShow/avdecvideosoftwaredeinterlacemode-property">AVDecVideoSoftwareDeinterlaceMode</a> property.

## -enum-fields

### -field eAVDecVideoSoftwareDeinterlaceMode_NoDeinterlacing:0

No software deinterlacing.

### -field eAVDecVideoSoftwareDeinterlaceMode_ProgressiveDeinterlacing:1

Progressive deinterlacing.

### -field eAVDecVideoSoftwareDeinterlaceMode_BOBDeinterlacing:2

Bob deinterlacing.

### -field eAVDecVideoSoftwareDeinterlaceMode_SmartBOBDeinterlacing:3  

"Smart" bob deinterlacing.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
