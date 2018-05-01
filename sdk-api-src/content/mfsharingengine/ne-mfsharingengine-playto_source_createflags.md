---
UID: NE:mfsharingengine.PLAYTO_SOURCE_CREATEFLAGS
title: PLAYTO_SOURCE_CREATEFLAGS
author: windows-driver-content
description: Contains flags for the IPlayToSourceClassFactory::CreateInstance method.
old-location: mf\playto_source_createflags.htm
old-project: medfound
ms.assetid: 15B632DD-586B-40E4-9B63-05CCC6AFB93A
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: PLAYTO_CONTROLLER_CREATEFLAGS, PLAYTO_CONTROLLER_CREATEFLAGS enumeration [Media Foundation], PLAYTO_SOURCE_AUDIO, PLAYTO_SOURCE_CREATEFLAGS, PLAYTO_SOURCE_IMAGE, PLAYTO_SOURCE_PROTECTED, PLAYTO_SOURCE_VIDEO, mf.playto_controller_createflags, mf.playto_source_createflags, mfsharingengine/PLAYTO_CONTROLLER_CREATEFLAGS, mfsharingengine/PLAYTO_SOURCE_AUDIO, mfsharingengine/PLAYTO_SOURCE_IMAGE, mfsharingengine/PLAYTO_SOURCE_PROTECTED, mfsharingengine/PLAYTO_SOURCE_VIDEO
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: mfsharingengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
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
req.typenames: PLAYTO_SOURCE_CREATEFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mfsharingengine.h
api_name:
-	PLAYTO_SOURCE_CREATEFLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# PLAYTO_SOURCE_CREATEFLAGS enumeration


## -description


Contains flags for the <a href="https://msdn.microsoft.com/3F7F8441-B0A2-407E-B127-C7DC66CA34DE">IPlayToSourceClassFactory::CreateInstance</a> method.


## -enum-fields




### -field PLAYTO_SOURCE_NONE


### -field PLAYTO_SOURCE_IMAGE

Share images.


### -field PLAYTO_SOURCE_AUDIO

Share audio.


### -field PLAYTO_SOURCE_VIDEO

Share video.


### -field PLAYTO_SOURCE_PROTECTED

Share DRM protected media.

Supported in Windows 8.1 and later.


## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

