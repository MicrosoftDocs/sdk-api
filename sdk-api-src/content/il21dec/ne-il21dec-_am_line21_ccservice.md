---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _AM_LINE21_CCSERVICE enumeration


## -description



Indicates the closed captioning service.




## -enum-fields




### -field AM_L21_CCSERVICE_None


            No current service.
          


### -field AM_L21_CCSERVICE_Caption1


            CC1 (caption channel).
          


### -field AM_L21_CCSERVICE_Caption2


            CC2 (caption channel).
          


### -field AM_L21_CCSERVICE_Text1


            T1 (text channel).
          


### -field AM_L21_CCSERVICE_Text2


            T2 (text channel)
          


### -field AM_L21_CCSERVICE_XDS


            Extended Data Services (XDS or EDS).
          


### -field AM_L21_CCSERVICE_DefChannel


### -field AM_L21_CCSERVICE_Invalid




## -remarks



The Line 21 decoder supports CC1 and CC2 only.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/bfd1c33d-27e0-4923-9c80-5d1bedb4fd25">IAMLine21Decoder::GetCurrentService</a>



<a href="https://msdn.microsoft.com/2f1945c3-644d-4e72-b2b7-a7e068b59d96">IAMLine21Decoder::SetCurrentService</a>
 

 

