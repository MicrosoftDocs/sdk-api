---
UID: NF:d2d1helper.ColorF.ColorF(UINT32,FLOAT)
title: ColorF::ColorF(UINT32,FLOAT) (d2d1helper.h)
description: Instantiates a new instance of the ColorF class that contains the specified RGB and alpha values.
helpviewer_keywords: ["ColorF","ColorF interface [Direct2D]","ColorF(UINT32","FLOAT) constructor","ColorF(UINT32","FLOAT) constructor [Direct2D]","ColorF(UINT32","FLOAT) constructor [Direct2D]","ColorF interface","ColorF.ColorF","ColorF.ColorF(UINT32","FLOAT)","ColorF::ColorF","ColorF::ColorF(UINT32","FLOAT)","ColorF::ColorF(UINT32","FLOAT)(UINT32","FLOAT)","D2D1.ColorF.ColorF(UINT32","FLOAT)","D2D1::ColorF::ColorF(UINT32","FLOAT)","d2d1helper/ColorF::ColorF(UINT32","FLOAT)","direct2d.colorf_colorf_uint32_rgb__float_a_"]
old-location: direct2d\colorf_colorf_uint32_rgb__float_a_.htm
tech.root: Direct2D
ms.assetid: 1edb46b1-9700-4c0d-b987-660034e8fb55
ms.date: 12/05/2018
ms.keywords: ColorF, ColorF interface [Direct2D],ColorF(UINT32,FLOAT) constructor, ColorF(UINT32,FLOAT) constructor [Direct2D], ColorF(UINT32,FLOAT) constructor [Direct2D],ColorF interface, ColorF.ColorF, ColorF.ColorF(UINT32,FLOAT), ColorF::ColorF, ColorF::ColorF(UINT32,FLOAT), ColorF::ColorF(UINT32,FLOAT)(UINT32,FLOAT), D2D1.ColorF.ColorF(UINT32,FLOAT), D2D1::ColorF::ColorF(UINT32,FLOAT), d2d1helper/ColorF::ColorF(UINT32,FLOAT), direct2d.colorf_colorf_uint32_rgb__float_a_
req.header: d2d1helper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: D2D1
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ColorF::ColorF
 - d2d1helper/ColorF::ColorF
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ColorF.ColorF(UINT32, FLOAT)
---

# ColorF::ColorF(UINT32,FLOAT)


## -description

Instantiates a new instance of the <a href="/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf">ColorF</a> class that contains the specified RGB and alpha values.

## -parameters

### -param rgb

Type: <b>UINT32</b>

The RGB value for the color to be constructed.

### -param a

Type: <b>FLOAT</b>

The alpha value for the color to be constructed. An alpha channel value ranges from 0.0 to 1.0, where 0.0 represents a fully transparent color and 1.0  represents a fully opaque color. The default value is 1.0.

## -see-also

<a href="/windows/desktop/Direct2D/direct2d-brushes-overview">Brushes Overview</a>



<a href="/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf">ColorF</a>