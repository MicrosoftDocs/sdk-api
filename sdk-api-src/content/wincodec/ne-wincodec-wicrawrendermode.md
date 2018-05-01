---
UID: NE:wincodec.WICRawRenderMode
title: WICRawRenderMode
author: windows-driver-content
description: Specifies the render intent of the next CopyPixels call.
old-location: wic\_wic_codec_wicrawrendermode.htm
old-project: wic
ms.assetid: dc020c78-a018-42ee-a500-65a743b96107
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: WICRawRenderMode, WICRawRenderMode enumeration [Windows Imaging Component], WICRawRenderModeBestQuality, WICRawRenderModeDraft, WICRawRenderModeNormal, _wic_codec_wicrawrendermode, wic._wic_codec_wicrawrendermode, wincodec/WICRawRenderMode, wincodec/WICRawRenderModeBestQuality, wincodec/WICRawRenderModeDraft, wincodec/WICRawRenderModeNormal
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICRawRenderMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincodec.h
api_name:
-	WICRawRenderMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WICRawRenderMode enumeration


## -description


Specifies the render intent of the next <a href="https://msdn.microsoft.com/d4908a75-e7de-4b8f-bdc8-d86cf6b49f8c">CopyPixels</a> call. 


## -enum-fields




### -field WICRawRenderModeDraft

Use speed priority mode.


### -field WICRawRenderModeNormal

Use normal priority mode. Balance of speed and quality.


### -field WICRawRenderModeBestQuality

Use best quality mode.


### -field WICRAWRENDERMODE_FORCE_DWORD



