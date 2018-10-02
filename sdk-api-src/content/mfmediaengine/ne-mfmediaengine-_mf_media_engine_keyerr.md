---
UID: NE:mfmediaengine._MF_MEDIA_ENGINE_KEYERR
title: "_MF_MEDIA_ENGINE_KEYERR"
author: windows-sdk-content
description: Defines media key error codes for the media engine.
old-location: mf\mf_media_engine_keyerr.htm
tech.root: MedFound
ms.assetid: F6E13260-74A2-40D0-A704-4E1CDB16B8D8
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: MF_MEDIAENGINE_KEYERR_CLIENT, MF_MEDIAENGINE_KEYERR_DOMAIN, MF_MEDIAENGINE_KEYERR_HARDWARECHANGE, MF_MEDIAENGINE_KEYERR_OUTPUT, MF_MEDIAENGINE_KEYERR_SERVICE, MF_MEDIAENGINE_KEYERR_UNKNOWN, MF_MEDIA_ENGINE_KEYERR, MF_MEDIA_ENGINE_KEYERR enumeration [Media Foundation], _MF_MEDIA_ENGINE_KEYERR, mf.mf_media_engine_keyerr, mfmediaengine/MF_MEDIAENGINE_KEYERR_CLIENT, mfmediaengine/MF_MEDIAENGINE_KEYERR_DOMAIN, mfmediaengine/MF_MEDIAENGINE_KEYERR_HARDWARECHANGE, mfmediaengine/MF_MEDIAENGINE_KEYERR_OUTPUT, mfmediaengine/MF_MEDIAENGINE_KEYERR_SERVICE, mfmediaengine/MF_MEDIAENGINE_KEYERR_UNKNOWN, mfmediaengine/MF_MEDIA_ENGINE_KEYERR
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
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
 - mfmediaengine.h
api_name:
 - MF_MEDIA_ENGINE_KEYERR
product: Windows
targetos: Windows
req.typenames: MF_MEDIA_ENGINE_KEYERR
req.redist: 
---

# _MF_MEDIA_ENGINE_KEYERR enumeration


## -description


Defines media key error codes for the media engine.


## -enum-fields




### -field MF_MEDIAENGINE_KEYERR_UNKNOWN

Unknown error occurred.


### -field MF_MEDIAENGINE_KEYERR_CLIENT

An error with the client occurred.


### -field MF_MEDIAENGINE_KEYERR_SERVICE

An error with the service occurred.


### -field MF_MEDIAENGINE_KEYERR_OUTPUT

An error with the output occurred.


### -field MF_MEDIAENGINE_KEYERR_HARDWARECHANGE

An error occurred related to a hardware change.


### -field MF_MEDIAENGINE_KEYERR_DOMAIN

An error with the domain occurred.


## -remarks



<b>MF_MEDIA_ENGINE_KEYERR</b> is used with the <i>code</i> parameter of  <a href="https://msdn.microsoft.com/e437b46a-8b25-42c4-b307-b6962b60b452">IMFMediaKeySessionNotify::KeyError</a> and the <i>code</i> value returned from <a href="https://msdn.microsoft.com/4693b7d5-59ee-472f-83fc-1ecbcc165dac">IMFMediaKeySession::GetError</a>.




## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

