---
UID: NS:dxvahd._DXVAHD_COLOR
title: "_DXVAHD_COLOR"
author: windows-sdk-content
description: Defines a color value for Microsoft DirectX Video Acceleration High Definition (DXVA-HD).
old-location: mf\dxvahd_color.htm
old-project: medfound
ms.assetid: 833bb91b-d891-4c3f-be20-367b0a23e97e
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: DXVAHD_COLOR, DXVAHD_COLOR union [Media Foundation], _DXVAHD_COLOR, dxvahd/DXVAHD_COLOR, mf.dxvahd_color
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dxvahd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DXVAHD_COLOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dxvahd.h
api_name:
-	DXVAHD_COLOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _DXVAHD_COLOR structure


## -description


Defines a color value for Microsoft DirectX Video Acceleration High Definition (DXVA-HD).


## -struct-fields




### -field RGB

A <a href="https://msdn.microsoft.com/60a167cb-f95e-4eb5-995f-be4cceaee47d">DXVAHD_COLOR_RGBA</a> structure that contains an RGB color value.


### -field YCbCr

A <a href="https://msdn.microsoft.com/3e37daf1-5529-4042-ab6e-89a7f77d5e15">DXVAHD_COLOR_YCbCrA</a> structure that contains a YCbCr color value.


## -remarks



This union can represent both RGB and YCbCr colors. The interpretation of the union depends on the context.




## -see-also




<a href="https://msdn.microsoft.com/03d97d26-714d-4aec-bb92-0772f09b7cca">Media Foundation Unions</a>
 

 

