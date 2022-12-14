---
UID: NE:xpsobjectmodel.__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0004
title: XPS_STYLE_SIMULATION (xpsobjectmodel.h)
description: Describes the simulation style of a font or glyph.
helpviewer_keywords: ["XPS_STYLE_SIMULATION","XPS_STYLE_SIMULATION enumeration [XPS Documents and Packaging]","XPS_STYLE_SIMULATION_BOLD","XPS_STYLE_SIMULATION_BOLDITALIC","XPS_STYLE_SIMULATION_ITALIC","XPS_STYLE_SIMULATION_NONE","xps.xps_style_simulation","xpsobjectmodel/XPS_STYLE_SIMULATION","xpsobjectmodel/XPS_STYLE_SIMULATION_BOLD","xpsobjectmodel/XPS_STYLE_SIMULATION_BOLDITALIC","xpsobjectmodel/XPS_STYLE_SIMULATION_ITALIC","xpsobjectmodel/XPS_STYLE_SIMULATION_NONE"]
old-location: xps\xps_style_simulation.htm
tech.root: xps
ms.assetid: 3f77c349-ba78-44e9-866a-9f654ed0e9dd
ms.date: 12/05/2018
ms.keywords: XPS_STYLE_SIMULATION, XPS_STYLE_SIMULATION enumeration [XPS Documents and Packaging], XPS_STYLE_SIMULATION_BOLD, XPS_STYLE_SIMULATION_BOLDITALIC, XPS_STYLE_SIMULATION_ITALIC, XPS_STYLE_SIMULATION_NONE, xps.xps_style_simulation, xpsobjectmodel/XPS_STYLE_SIMULATION, xpsobjectmodel/XPS_STYLE_SIMULATION_BOLD, xpsobjectmodel/XPS_STYLE_SIMULATION_BOLDITALIC, xpsobjectmodel/XPS_STYLE_SIMULATION_ITALIC, xpsobjectmodel/XPS_STYLE_SIMULATION_NONE
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: XPS_STYLE_SIMULATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0004
 - xpsobjectmodel/__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0004
 - XPS_STYLE_SIMULATION
 - xpsobjectmodel/XPS_STYLE_SIMULATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xpsobjectmodel.h
api_name:
 - XPS_STYLE_SIMULATION
---

# XPS_STYLE_SIMULATION enumeration


## -description

Describes the simulation style of a font or glyph.

To simulate the appearance of a style that is not provided by the font or glyph, style simulation modifies an existing font or a glyph image.
<div class="code"></div>

## -enum-fields

### -field XPS_STYLE_SIMULATION_NONE:1

No font style simulation.

### -field XPS_STYLE_SIMULATION_ITALIC

Italic style simulation.

### -field XPS_STYLE_SIMULATION_BOLD

Bold style simulation.

### -field XPS_STYLE_SIMULATION_BOLDITALIC

Both bold and italic style simulation: first bold, then italic.

## -see-also

<a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>

