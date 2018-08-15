---
UID: NE:d2d1effects_2.D2D1_EMBOSS_PROP
title: D2D1_EMBOSS_PROP
author: windows-sdk-content
description: Identifiers for properties of the Emboss effect.
old-location: direct2d\d2d1_emboss_prop.htm
old-project: direct2d
ms.assetid: 1AC8F0FE-8D51-4DDD-94FB-DC7AC890C95F
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D2D1_EMBOSS_PROP, D2D1_EMBOSS_PROP enumeration [Direct2D], D2D1_EMBOSS_PROP_DIRECTION, D2D1_EMBOSS_PROP_HEIGHT, d2d1effects_2/D2D1_EMBOSS_PROP, d2d1effects_2/D2D1_EMBOSS_PROP_DIRECTION, d2d1effects_2/D2D1_EMBOSS_PROP_HEIGHT, direct2d.d2d1_emboss_prop
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1effects_2.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D2D1_EMBOSS_PROP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects_2.h
api_name:
 - D2D1_EMBOSS_PROP
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# D2D1_EMBOSS_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/74f63875-35cd-f335-62cd-410a953e53ea">Emboss effect</a>.


## -enum-fields




### -field D2D1_EMBOSS_PROP_HEIGHT

The D2D1_EMBOSS_PROP_HEIGHT property is a float value controlling the strength of the embossing effect.  The allowed range is 0.0 to 10.0.  The default value is 1.0.


### -field D2D1_EMBOSS_PROP_DIRECTION

The D2D1_EMBOSS_PROP_DIRECTION property is a float value specifying the light direction used to create the effect. The allowed range is 0.0 to 360.0.  The default value is 0.0. 


### -field D2D1_EMBOSS_PROP_FORCE_DWORD



