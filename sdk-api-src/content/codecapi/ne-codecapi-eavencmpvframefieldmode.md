---
UID: NE:codecapi.eAVEncMPVFrameFieldMode
title: eAVEncMPVFrameFieldMode
author: windows-sdk-content
description: Specifies whether the encoder produces encoded fields or encoded frames. This enumeration is used with the AVEncMPVFrameFieldMode property.
old-location: dshow\eavencmpvframefieldmode.htm
tech.root: DirectShow
ms.assetid: 4e1d683c-cbeb-4e40-a8d2-484d09323cb9
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: codecapi/eAVEncMPVFrameFieldMode, codecapi/eAVEncMPVFrameFieldMode_FieldMode, codecapi/eAVEncMPVFrameFieldMode_FrameMode, dshow.eavencmpvframefieldmode, eAVEncMPVFrameFieldMode, eAVEncMPVFrameFieldMode enumeration [DirectShow], eAVEncMPVFrameFieldModeEnumeration, eAVEncMPVFrameFieldMode_FieldMode, eAVEncMPVFrameFieldMode_FrameMode
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - eAVEncMPVFrameFieldMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# eAVEncMPVFrameFieldMode enumeration


## -description



Specifies whether the encoder produces encoded fields or encoded frames. This enumeration is used with the <a href="https://msdn.microsoft.com/bf21ea55-662f-4a69-8528-67592b8b8645">AVEncMPVFrameFieldMode</a> property.




## -enum-fields




### -field eAVEncMPVFrameFieldMode_FieldMode

The encoder produces an MPEG picture for each field in the source video.


### -field eAVEncMPVFrameFieldMode_FrameMode

The encoder produces an MPEG picture for each frame (or pair of fields) in the source video.


## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI Interface</a>
 

 

