---
UID: NS:ddraw._DDCOLORKEY
title: DDCOLORKEY (ddraw.h)
description: The DDCOLORKEY structure describes a source color key, destination color key, or color space.
old-location: directdraw\ddcolorkey.htm
tech.root: directdraw
ms.assetid: c520e649-86f9-4c4a-bb67-22d75aa3c8b0
ms.date: 12/05/2018
ms.keywords: '*LPDDCOLORKEY, DDCOLORKEY, DDCOLORKEY structure [DirectDraw], LPDDCOLORKEY, LPDDCOLORKEY structure pointer [DirectDraw], ddraw/DDCOLORKEY, ddraw/LPDDCOLORKEY, directdraw.ddcolorkey'
f1_keywords:
- ddraw/DDCOLORKEY
dev_langs:
- c++
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
targetos: Windows
req.typenames: DDCOLORKEY
req.redist: 
ms.custom: 19H1
---

# DDCOLORKEY structure


## -description


The <b>DDCOLORKEY</b> structure describes a source color key, destination color key, or color space. A color key is specified if the low and high range values are the same. This structure is used with the <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getcolorkey">IDirectDrawSurface7::GetColorKey</a> and <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-setcolorkey">IDirectDrawSurface7::SetColorKey</a> methods.




## -struct-fields




### -field dwColorSpaceLowValue

Low value of the color range that is to be used as the color key.


### -field dwColorSpaceHighValue

High value of the color range that is to be used as the color key.

