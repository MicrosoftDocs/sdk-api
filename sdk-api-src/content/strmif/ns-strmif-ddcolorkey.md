---
UID: NS:strmif.DDCOLORKEY
title: DDCOLORKEY (strmif.h)
description: Describes a color key as a range of values.
helpviewer_keywords: ["*LPDDCOLORKEY","DDCOLORKEY","DDCOLORKEY structure [DirectShow]","DDCOLORKEYStructure","dshow.ddcolorkey","strmif/DDCOLORKEY"]
old-location: dshow\ddcolorkey.htm
tech.root: dshow
ms.assetid: bd360860-94e3-4f91-a455-5fdb227368b3
ms.date: 12/05/2018
ms.keywords: '*LPDDCOLORKEY, DDCOLORKEY, DDCOLORKEY structure [DirectShow], DDCOLORKEYStructure, dshow.ddcolorkey, strmif/DDCOLORKEY'
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP or later
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
targetos: Windows
req.typenames: DDCOLORKEY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DDCOLORKEY
 - strmif/DDCOLORKEY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DDCOLORKEY
---

# DDCOLORKEY structure


## -description

Describes a color key as a range of values.

## -struct-fields

### -field dw1

Specifies the lower bound of the color key range.

### -field dw2

Specifies the upper bound of the color key range.

## -remarks

This structure is used by the Video Mixing Renderer (VMR) filter. The VMR uses this structure to support the DirectDraw capability of specifying a range of values for a color key by using two <b>DWORD</b>s. The VMR and the graphics card automatically determine whether the two <b>DWORD</b>s are interpreted as RGB or YUV color space values. Not all hardware may support this capability. To ensure compatibility with all hardware, set <b>dw1</b> and <b>dw2</b> to the same value.

