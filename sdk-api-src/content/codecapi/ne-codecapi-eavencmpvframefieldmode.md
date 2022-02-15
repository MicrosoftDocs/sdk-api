---
UID: NE:codecapi.eAVEncMPVFrameFieldMode
title: eAVEncMPVFrameFieldMode (codecapi.h)
description: Specifies whether the encoder produces encoded fields or encoded frames. This enumeration is used with the AVEncMPVFrameFieldMode property.
helpviewer_keywords: ["codecapi/eAVEncMPVFrameFieldMode","codecapi/eAVEncMPVFrameFieldMode_FieldMode","codecapi/eAVEncMPVFrameFieldMode_FrameMode","dshow.eavencmpvframefieldmode","eAVEncMPVFrameFieldMode","eAVEncMPVFrameFieldMode enumeration [DirectShow]","eAVEncMPVFrameFieldModeEnumeration","eAVEncMPVFrameFieldMode_FieldMode","eAVEncMPVFrameFieldMode_FrameMode"]
old-location: dshow\eavencmpvframefieldmode.htm
tech.root: dshow
ms.assetid: 4e1d683c-cbeb-4e40-a8d2-484d09323cb9
ms.date: 12/05/2018
ms.keywords: codecapi/eAVEncMPVFrameFieldMode, codecapi/eAVEncMPVFrameFieldMode_FieldMode, codecapi/eAVEncMPVFrameFieldMode_FrameMode, dshow.eavencmpvframefieldmode, eAVEncMPVFrameFieldMode, eAVEncMPVFrameFieldMode enumeration [DirectShow], eAVEncMPVFrameFieldModeEnumeration, eAVEncMPVFrameFieldMode_FieldMode, eAVEncMPVFrameFieldMode_FrameMode
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
 - eAVEncMPVFrameFieldMode
 - codecapi/eAVEncMPVFrameFieldMode
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
 - eAVEncMPVFrameFieldMode
---

# eAVEncMPVFrameFieldMode enumeration


## -description

Specifies whether the encoder produces encoded fields or encoded frames. This enumeration is used with the <a href="/windows/desktop/DirectShow/avencmpvframefieldmode-property">AVEncMPVFrameFieldMode</a> property.

## -enum-fields

### -field eAVEncMPVFrameFieldMode_FieldMode:0

The encoder produces an MPEG picture for each field in the source video.

### -field eAVEncMPVFrameFieldMode_FrameMode:1

The encoder produces an MPEG picture for each frame (or pair of fields) in the source video.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
