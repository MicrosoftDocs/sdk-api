---
UID: NE:codecapi.eAVEncVideoSourceScanType
title: eAVEncVideoSourceScanType (codecapi.h)
description: Specifies whether the input frames for an encoder are progressive or interlaced. This enumeration is used with the AVEncVideoForceSourceScanType property.
helpviewer_keywords: ["codecapi/eAVEncVideoSourceScanType","codecapi/eAVEncVideoSourceScan_Automatic","codecapi/eAVEncVideoSourceScan_Interlaced","codecapi/eAVEncVideoSourceScan_Progressive","dshow.eavencvideosourcescantype","eAVEncVideoSourceScanType","eAVEncVideoSourceScanType enumeration [DirectShow]","eAVEncVideoSourceScanTypeEnumeration","eAVEncVideoSourceScan_Automatic","eAVEncVideoSourceScan_Interlaced","eAVEncVideoSourceScan_Progressive"]
old-location: dshow\eavencvideosourcescantype.htm
tech.root: dshow
ms.assetid: f191f4de-2549-4223-b40d-828df467b691
ms.date: 12/05/2018
ms.keywords: codecapi/eAVEncVideoSourceScanType, codecapi/eAVEncVideoSourceScan_Automatic, codecapi/eAVEncVideoSourceScan_Interlaced, codecapi/eAVEncVideoSourceScan_Progressive, dshow.eavencvideosourcescantype, eAVEncVideoSourceScanType, eAVEncVideoSourceScanType enumeration [DirectShow], eAVEncVideoSourceScanTypeEnumeration, eAVEncVideoSourceScan_Automatic, eAVEncVideoSourceScan_Interlaced, eAVEncVideoSourceScan_Progressive
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
 - eAVEncVideoSourceScanType
 - codecapi/eAVEncVideoSourceScanType
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
 - eAVEncVideoSourceScanType
---

# eAVEncVideoSourceScanType enumeration


## -description

Specifies whether the input frames for an encoder are progressive or interlaced. This enumeration is used with the <a href="/windows/desktop/DirectShow/avencvideoforcesourcescantype-property">AVEncVideoForceSourceScanType</a> property.

## -enum-fields

### -field eAVEncVideoSourceScan_Automatic:0

Use the media type on the encoder's input pin to determine whether the frames are progressive or interlaced.

### -field eAVEncVideoSourceScan_Interlaced:1

Input frames are interlaced.

### -field eAVEncVideoSourceScan_Progressive:2

Input frames are progressive.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
