---
UID: NE:codecapi.eAVEncVideoSourceScanType
title: eAVEncVideoSourceScanType
author: windows-sdk-content
description: Specifies whether the input frames for an encoder are progressive or interlaced. This enumeration is used with the AVEncVideoForceSourceScanType property.
old-location: dshow\eavencvideosourcescantype.htm
tech.root: DirectShow
ms.assetid: f191f4de-2549-4223-b40d-828df467b691
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: codecapi/eAVEncVideoSourceScanType, codecapi/eAVEncVideoSourceScan_Automatic, codecapi/eAVEncVideoSourceScan_Interlaced, codecapi/eAVEncVideoSourceScan_Progressive, dshow.eavencvideosourcescantype, eAVEncVideoSourceScanType, eAVEncVideoSourceScanType enumeration [DirectShow], eAVEncVideoSourceScanTypeEnumeration, eAVEncVideoSourceScan_Automatic, eAVEncVideoSourceScan_Interlaced, eAVEncVideoSourceScan_Progressive
ms.topic: enum
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# eAVEncVideoSourceScanType enumeration


## -description



Specifies whether the input frames for an encoder are progressive or interlaced. This enumeration is used with the <a href="https://msdn.microsoft.com/59aeb20a-5e8b-4e27-8e69-9f373ff45b27">AVEncVideoForceSourceScanType</a> property.




## -enum-fields




### -field eAVEncVideoSourceScan_Automatic

Use the media type on the encoder's input pin to determine whether the frames are progressive or interlaced.


### -field eAVEncVideoSourceScan_Interlaced

Input frames are interlaced.


### -field eAVEncVideoSourceScan_Progressive

Input frames are progressive.


## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd311953(v=VS.85).aspx">ICodecAPI Interface</a>
 

 

