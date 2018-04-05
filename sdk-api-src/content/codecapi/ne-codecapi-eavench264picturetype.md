---
UID: NE:codecapi.eAVEncH264PictureType
title: eAVEncH264PictureType
author: windows-driver-content
description: Specifies the type of picture that is output by a video encoder.
old-location: mf\eavench264picturetype.htm
old-project: medfound
ms.assetid: D73E2F87-EED3-4655-BB39-EB4C8E0B0058
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: codecapi/eAVEncH264PictureType, codecapi/eAVEncH264PictureType_B, codecapi/eAVEncH264PictureType_IDR, codecapi/eAVEncH264PictureType_P, eAVEncH264PictureType, eAVEncH264PictureType enumeration [Media Foundation], eAVEncH264PictureType_B, eAVEncH264PictureType_IDR, eAVEncH264PictureType_P, mf.eavench264picturetype
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	codecapi.h
api_name:
-	eAVEncH264PictureType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# eAVEncH264PictureType enumeration


## -description


Specifies the type of picture that is output by a video encoder.


## -enum-fields




### -field eAVEncH264PictureType_IDR

Instantaneous decoding refresh (IDR) picture.


### -field eAVEncH264PictureType_P

Predictive (B) picture.


### -field eAVEncH264PictureType_B

Bi-predictive (B) picture.


## -remarks



This enumeration is used with the <a href="https://msdn.microsoft.com/18A47033-3EAC-46C3-94AB-6ED20732F63C">MFSampleExtension_VideoEncodePictureType</a> sample attribute.




## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

