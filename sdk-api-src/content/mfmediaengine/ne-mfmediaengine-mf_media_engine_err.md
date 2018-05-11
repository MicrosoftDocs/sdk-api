---
UID: NE:mfmediaengine.MF_MEDIA_ENGINE_ERR
title: MF_MEDIA_ENGINE_ERR
author: windows-driver-content
description: Defines error status codes for the Media Engine.
old-location: mf\mf_media_engine_err.htm
old-project: medfound
ms.assetid: CFA5C2AF-C804-47B4-B76A-907F26CF3DFC
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: MF_MEDIA_ENGINE_ERR, MF_MEDIA_ENGINE_ERR enumeration [Media Foundation], MF_MEDIA_ENGINE_ERR_ABORTED, MF_MEDIA_ENGINE_ERR_DECODE, MF_MEDIA_ENGINE_ERR_ENCRYPTED, MF_MEDIA_ENGINE_ERR_NETWORK, MF_MEDIA_ENGINE_ERR_NOERROR, MF_MEDIA_ENGINE_ERR_SRC_NOT_SUPPORTED, mf.mf_media_engine_err, mfmediaengine/MF_MEDIA_ENGINE_ERR, mfmediaengine/MF_MEDIA_ENGINE_ERR_ABORTED, mfmediaengine/MF_MEDIA_ENGINE_ERR_DECODE, mfmediaengine/MF_MEDIA_ENGINE_ERR_ENCRYPTED, mfmediaengine/MF_MEDIA_ENGINE_ERR_NETWORK, mfmediaengine/MF_MEDIA_ENGINE_ERR_NOERROR, mfmediaengine/MF_MEDIA_ENGINE_ERR_SRC_NOT_SUPPORTED
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_MEDIA_ENGINE_ERR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mfmediaengine.h
api_name:
-	MF_MEDIA_ENGINE_ERR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MF_MEDIA_ENGINE_ERR enumeration


## -description


Defines error status codes for the Media Engine.


## -enum-fields




### -field MF_MEDIA_ENGINE_ERR_NOERROR

No error.


### -field MF_MEDIA_ENGINE_ERR_ABORTED

The process of fetching the media resource was stopped at the user's request. 


### -field MF_MEDIA_ENGINE_ERR_NETWORK

A network error occurred while fetching the media resource. 


### -field MF_MEDIA_ENGINE_ERR_DECODE

An error occurred while decoding the media resource. 


### -field MF_MEDIA_ENGINE_ERR_SRC_NOT_SUPPORTED

The media resource is not supported. 


### -field MF_MEDIA_ENGINE_ERR_ENCRYPTED

An error occurred while encrypting the media resource.

Supported in Windows 8.1 and later.


## -remarks



The values greater than zero correspond to error codes defined for the <b>MediaError</b> object  in HTML5.




## -see-also




<a href="https://msdn.microsoft.com/6E4C4559-F59C-488C-A790-D95831BC9D29">IMFMediaError::GetErrorCode</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

