---
UID: NE:wincodec.WICRawRenderMode
title: WICRawRenderMode (wincodec.h)
author: windows-sdk-content
description: Specifies the render intent of the next CopyPixels call.
old-location: wic\_wic_codec_wicrawrendermode.htm
tech.root: wic
ms.assetid: dc020c78-a018-42ee-a500-65a743b96107
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WICRawRenderMode, WICRawRenderMode enumeration [Windows Imaging Component], WICRawRenderModeBestQuality, WICRawRenderModeDraft, WICRawRenderModeNormal, _wic_codec_wicrawrendermode, wic._wic_codec_wicrawrendermode, wincodec/WICRawRenderMode, wincodec/WICRawRenderModeBestQuality, wincodec/WICRawRenderModeDraft, wincodec/WICRawRenderModeNormal
ms.topic: enum
f1_keywords: 
 - "wincodec/WICRawRenderMode"
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
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
 - Wincodec.h
api_name:
 - WICRawRenderMode
product: Windows
targetos: Windows
req.typenames: WICRawRenderMode
req.redist: 
ms.custom: 19H1
---

# WICRawRenderMode enumeration


## -description


Specifies the render intent of the next <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels">CopyPixels</a> call. 


## -enum-fields




### -field WICRawRenderModeDraft

Use speed priority mode.


### -field WICRawRenderModeNormal

Use normal priority mode. Balance of speed and quality.


### -field WICRawRenderModeBestQuality

Use best quality mode.


### -field WICRAWRENDERMODE_FORCE_DWORD



