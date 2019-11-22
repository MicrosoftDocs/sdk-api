---
UID: NE:codecapi.eAVEncVideoSourceScanType
title: eAVEncVideoSourceScanType (codecapi.h)

description: Specifies whether the input frames for an encoder are progressive or interlaced. This enumeration is used with the AVEncVideoForceSourceScanType property.
old-location: dshow\eavencvideosourcescantype.htm
tech.root: DirectShow
ms.assetid: f191f4de-2549-4223-b40d-828df467b691

ms.date: 12/05/2018
ms.keywords: codecapi/eAVEncVideoSourceScanType, codecapi/eAVEncVideoSourceScan_Automatic, codecapi/eAVEncVideoSourceScan_Interlaced, codecapi/eAVEncVideoSourceScan_Progressive, dshow.eavencvideosourcescantype, eAVEncVideoSourceScanType, eAVEncVideoSourceScanType enumeration [DirectShow], eAVEncVideoSourceScanTypeEnumeration, eAVEncVideoSourceScan_Automatic, eAVEncVideoSourceScan_Interlaced, eAVEncVideoSourceScan_Progressive
ms.topic: enum
f1_keywords: 
 - "codecapi/eAVEncVideoSourceScanType"
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
 - eAVEncVideoSourceScanType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# eAVEncVideoSourceScanType enumeration


## -description



Specifies whether the input frames for an encoder are progressive or interlaced. This enumeration is used with the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/avencvideoforcesourcescantype-property">AVEncVideoForceSourceScanType</a> property.




## -enum-fields




### -field eAVEncVideoSourceScan_Automatic

Use the media type on the encoder's input pin to determine whether the frames are progressive or interlaced.


### -field eAVEncVideoSourceScan_Interlaced

Input frames are interlaced.


### -field eAVEncVideoSourceScan_Progressive

Input frames are progressive.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
 

 

