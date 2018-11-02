---
UID: NS:ddraw._DDCOLORKEY
title: "_DDCOLORKEY"
author: windows-sdk-content
description: The DDCOLORKEY structure describes a source color key, destination color key, or color space.
old-location: directdraw\ddcolorkey.htm
tech.root: directdraw
ms.assetid: c520e649-86f9-4c4a-bb67-22d75aa3c8b0
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*LPDDCOLORKEY, DDCOLORKEY, DDCOLORKEY structure [DirectDraw], LPDDCOLORKEY, LPDDCOLORKEY structure pointer [DirectDraw], _DDCOLORKEY, ddraw/DDCOLORKEY, ddraw/LPDDCOLORKEY, directdraw.ddcolorkey"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ddraw.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ddraw.h
api_name:
 - DDCOLORKEY
product: Windows
targetos: Windows
req.typenames: DDCOLORKEY
req.redist: 
---

# _DDCOLORKEY structure


## -description


The <b>DDCOLORKEY</b> structure describes a source color key, destination color key, or color space. A color key is specified if the low and high range values are the same. This structure is used with the <a href="https://msdn.microsoft.com/0df14c63-f962-4823-873a-3fe1d626f4cb">IDirectDrawSurface7::GetColorKey</a> and <a href="https://msdn.microsoft.com/36f2510e-d12a-40af-b65c-aa36ce46a942">IDirectDrawSurface7::SetColorKey</a> methods.




## -struct-fields




### -field dwColorSpaceLowValue

Low value of the color range that is to be used as the color key.


### -field dwColorSpaceHighValue

High value of the color range that is to be used as the color key.

