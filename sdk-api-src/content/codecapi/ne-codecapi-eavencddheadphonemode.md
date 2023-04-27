---
UID: NE:codecapi.eAVEncDDHeadphoneMode
title: eAVEncDDHeadphoneMode (codecapi.h)
description: Specifies headphone mode for a Dolby Digital audio stream. This enumeration is used with the AVEncDDHeadphoneMode property.
helpviewer_keywords: ["codecapi/eAVEncDDHeadphoneMode","codecapi/eAVEncDDHeadphoneMode_Encoded","codecapi/eAVEncDDHeadphoneMode_NotEncoded","codecapi/eAVEncDDHeadphoneMode_NotIndicated","dshow.eavencddheadphonemode","eAVEncDDHeadphoneMode","eAVEncDDHeadphoneMode enumeration [DirectShow]","eAVEncDDHeadphoneMode_Encoded","eAVEncDDHeadphoneMode_NotEncoded","eAVEncDDHeadphoneMode_NotIndicated"]
old-location: dshow\eavencddheadphonemode.htm
tech.root: dshow
ms.assetid: 8739334c-bbaa-482e-9113-d4a885f98913
ms.date: 12/05/2018
ms.keywords: codecapi/eAVEncDDHeadphoneMode, codecapi/eAVEncDDHeadphoneMode_Encoded, codecapi/eAVEncDDHeadphoneMode_NotEncoded, codecapi/eAVEncDDHeadphoneMode_NotIndicated, dshow.eavencddheadphonemode, eAVEncDDHeadphoneMode, eAVEncDDHeadphoneMode enumeration [DirectShow], eAVEncDDHeadphoneMode_Encoded, eAVEncDDHeadphoneMode_NotEncoded, eAVEncDDHeadphoneMode_NotIndicated
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
 - eAVEncDDHeadphoneMode
 - codecapi/eAVEncDDHeadphoneMode
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
 - eAVEncDDHeadphoneMode
---

# eAVEncDDHeadphoneMode enumeration


## -description

Specifies headphone mode for a Dolby Digital audio stream. This enumeration is used with the <a href="/windows/desktop/DirectShow/avencddheadphonemode-property">AVEncDDHeadphoneMode</a> property.

## -enum-fields

### -field eAVEncDDHeadphoneMode_NotIndicated:0

Headphone mode is not indicated.

### -field eAVEncDDHeadphoneMode_NotEncoded:1

Headphone mode is disabled.

### -field eAVEncDDHeadphoneMode_Encoded:2

Headphone mode is enabled.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
