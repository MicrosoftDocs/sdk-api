---
UID: NE:codecapi.eAVEncDDService
title: eAVEncDDService
author: windows-sdk-content
description: Specifies the audio service contained in a Dolby Digital audio stream. This enumeration is used with the AVEncDDService property.
old-location: dshow\eavencddservice.htm
old-project: DirectShow
ms.assetid: 25673019-6c26-4b2c-a394-81177a6c00c0
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: codecapi/eAVEncDDService, codecapi/eAVEncDDService_C, codecapi/eAVEncDDService_CM, codecapi/eAVEncDDService_D, codecapi/eAVEncDDService_E, codecapi/eAVEncDDService_HI, codecapi/eAVEncDDService_ME, codecapi/eAVEncDDService_VI, codecapi/eAVEncDDService_VO, dshow.eavencddservice, eAVEncDDService, eAVEncDDService enumeration [DirectShow], eAVEncDDServiceEnumeration, eAVEncDDService_C, eAVEncDDService_CM, eAVEncDDService_D, eAVEncDDService_E, eAVEncDDService_HI, eAVEncDDService_ME, eAVEncDDService_VI, eAVEncDDService_VO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - codecapi.h
api_name:
 - eAVEncDDService
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# eAVEncDDService enumeration


## -description



Specifies the audio service contained in a Dolby Digital audio stream. This enumeration is used with the <a href="https://msdn.microsoft.com/454021c7-f574-443c-bd23-411be44162b5">AVEncDDService</a> property.




## -enum-fields




### -field eAVEncDDService_CM

Complete main audio service.


### -field eAVEncDDService_ME

Main service: music and effects. (The main audio service minus the dialog channel.)


### -field eAVEncDDService_VI

Associated service: visually impaired.


### -field eAVEncDDService_HI

Associated service: hard of hearing.


### -field eAVEncDDService_D

Associated service: dialog.


### -field eAVEncDDService_C

Associated service: commentary.


### -field eAVEncDDService_E

Associated service: emergency.


### -field eAVEncDDService_VO

Associated service: voice over.


## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI Interface</a>
 

 

