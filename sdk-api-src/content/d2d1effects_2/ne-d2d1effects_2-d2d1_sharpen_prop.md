---
UID: NE:d2d1effects_2.D2D1_SHARPEN_PROP
title: D2D1_SHARPEN_PROP
author: windows-sdk-content
description: Identifiers for properties of the Sharpen effect.
old-location: direct2d\d2d1_sharpen_prop.htm
old-project: Direct2D
ms.assetid: 73ED06C4-A8FB-4312-8BB8-3B9C885E9FEC
ms.author: windowssdkdev
ms.date: 04/20/2018
ms.keywords: D2D1_SHARPEN_PROP, D2D1_SHARPEN_PROP enumeration [Direct2D], D2D1_SHARPEN_PROP_SHARPNESS, D2D1_SHARPEN_PROP_THRESHOLD, d2d1effects_2/D2D1_SHARPEN_PROP, d2d1effects_2/D2D1_SHARPEN_PROP_SHARPNESS, d2d1effects_2/D2D1_SHARPEN_PROP_THRESHOLD, direct2d.d2d1_sharpen_prop
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1effects_2.h
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
req.typenames: D2D1_SHARPEN_PROP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d2d1effects_2.h
api_name:
-	D2D1_SHARPEN_PROP
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# D2D1_SHARPEN_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/1eb12d1e-83c1-ba13-33be-df2078f3ccb8">Sharpen effect</a>.


## -enum-fields




### -field D2D1_SHARPEN_PROP_SHARPNESS

The D2D1_SHARPEN_PROP_SHARPNESS property is a float value indicating how much to sharpen the input image.  The allowed range is 0.0 to 10.0. The default value is 0.0.


### -field D2D1_SHARPEN_PROP_THRESHOLD

The D2D1_SHARPEN_PROP_THRESHOLD property is a float value.  The allowed range is 0.0 to 1.0. The default value is 0.0.


### -field D2D1_SHARPEN_PROP_FORCE_DWORD



