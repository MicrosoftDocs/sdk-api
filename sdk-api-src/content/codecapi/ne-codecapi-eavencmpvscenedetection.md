---
UID: NE:codecapi.eAVEncMPVSceneDetection
title: eAVEncMPVSceneDetection (codecapi.h)
author: windows-sdk-content
description: Specifies how the encoder behaves when it detects a new scene. This enumeration is used with the AVEncMPVSceneDetection property.
old-location: dshow\eavencmpvscenedetection.htm
tech.root: DirectShow
ms.assetid: 81d273bd-06bc-4418-98af-8e7756aac91c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: codecapi/eAVEncMPVSceneDetection, codecapi/eAVEncMPVSceneDetection_InsertIPicture, codecapi/eAVEncMPVSceneDetection_None, codecapi/eAVEncMPVSceneDetection_StartNewGOP, codecapi/eAVEncMPVSceneDetection_StartNewLocatableGOP, dshow.eavencmpvscenedetection, eAVEncMPVSceneDetection, eAVEncMPVSceneDetection enumeration [DirectShow], eAVEncMPVSceneDetectionEnumeration, eAVEncMPVSceneDetection_InsertIPicture, eAVEncMPVSceneDetection_None, eAVEncMPVSceneDetection_StartNewGOP, eAVEncMPVSceneDetection_StartNewLocatableGOP
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
 - eAVEncMPVSceneDetection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# eAVEncMPVSceneDetection enumeration


## -description



Specifies how the encoder behaves when it detects a new scene. This enumeration is used with the <a href="https://msdn.microsoft.com/9950a55c-75c5-4b49-bd8a-1ce40ac71ee5">AVEncMPVSceneDetection</a> property.




## -enum-fields




### -field eAVEncMPVSceneDetection_None

No special behavior.


### -field eAVEncMPVSceneDetection_InsertIPicture

Insert an I frame.


### -field eAVEncMPVSceneDetection_StartNewGOP

Start a new group of pictures (GOP).


### -field eAVEncMPVSceneDetection_StartNewLocatableGOP

Start a new GOP in which the first consecutive B frames do not reference the previous GOP.


## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd311953(v=VS.85).aspx">ICodecAPI Interface</a>
 

 

