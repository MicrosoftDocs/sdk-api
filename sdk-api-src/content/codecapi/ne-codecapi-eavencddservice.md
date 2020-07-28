---
UID: NE:codecapi.eAVEncDDService
title: eAVEncDDService (codecapi.h)
description: Specifies the audio service contained in a Dolby Digital audio stream. This enumeration is used with the AVEncDDService property.
helpviewer_keywords: ["codecapi/eAVEncDDService","codecapi/eAVEncDDService_C","codecapi/eAVEncDDService_CM","codecapi/eAVEncDDService_D","codecapi/eAVEncDDService_E","codecapi/eAVEncDDService_HI","codecapi/eAVEncDDService_ME","codecapi/eAVEncDDService_VI","codecapi/eAVEncDDService_VO","dshow.eavencddservice","eAVEncDDService","eAVEncDDService enumeration [DirectShow]","eAVEncDDServiceEnumeration","eAVEncDDService_C","eAVEncDDService_CM","eAVEncDDService_D","eAVEncDDService_E","eAVEncDDService_HI","eAVEncDDService_ME","eAVEncDDService_VI","eAVEncDDService_VO"]
old-location: dshow\eavencddservice.htm
tech.root: dshow
ms.assetid: 25673019-6c26-4b2c-a394-81177a6c00c0
ms.date: 12/05/2018
ms.keywords: codecapi/eAVEncDDService, codecapi/eAVEncDDService_C, codecapi/eAVEncDDService_CM, codecapi/eAVEncDDService_D, codecapi/eAVEncDDService_E, codecapi/eAVEncDDService_HI, codecapi/eAVEncDDService_ME, codecapi/eAVEncDDService_VI, codecapi/eAVEncDDService_VO, dshow.eavencddservice, eAVEncDDService, eAVEncDDService enumeration [DirectShow], eAVEncDDServiceEnumeration, eAVEncDDService_C, eAVEncDDService_CM, eAVEncDDService_D, eAVEncDDService_E, eAVEncDDService_HI, eAVEncDDService_ME, eAVEncDDService_VI, eAVEncDDService_VO
f1_keywords:
- codecapi/eAVEncDDService
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
- eAVEncDDService
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# eAVEncDDService enumeration


## -description



Specifies the audio service contained in a Dolby Digital audio stream. This enumeration is used with the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/avencddservice-property">AVEncDDService</a> property.




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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
 

 

