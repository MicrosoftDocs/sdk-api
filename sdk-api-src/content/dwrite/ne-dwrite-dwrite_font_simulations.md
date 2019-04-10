---
UID: NE:dwrite.DWRITE_FONT_SIMULATIONS
title: DWRITE_FONT_SIMULATIONS (dwrite.h)
author: windows-sdk-content
description: Specifies algorithmic style simulations to be applied to the font face. Bold and oblique simulations can be combined via bitwise OR operation.
old-location: directwrite\dwrite_font_simulations.htm
tech.root: DirectWrite
ms.assetid: 0881afec-2fa5-4f17-96a2-68a5293e0bba
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DWRITE_FONT_SIMULATIONS, DWRITE_FONT_SIMULATIONS enumeration [Direct Write], DWRITE_FONT_SIMULATIONS_BOLD, DWRITE_FONT_SIMULATIONS_NONE, DWRITE_FONT_SIMULATIONS_OBLIQUE, directwrite.dwrite_font_simulations, dwrite/DWRITE_FONT_SIMULATIONS, dwrite/DWRITE_FONT_SIMULATIONS_BOLD, dwrite/DWRITE_FONT_SIMULATIONS_NONE, dwrite/DWRITE_FONT_SIMULATIONS_OBLIQUE
ms.topic: enum
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - dwrite.h
api_name:
 - DWRITE_FONT_SIMULATIONS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DWRITE_FONT_SIMULATIONS enumeration


## -description


Specifies algorithmic style simulations to be applied to the font face. Bold and oblique simulations can be combined via bitwise OR operation.


## -enum-fields




### -field DWRITE_FONT_SIMULATIONS_NONE

Indicates that no simulations are applied to the font face.


### -field DWRITE_FONT_SIMULATIONS_BOLD

Indicates that algorithmic emboldening is applied to the font face.  <a href="https://msdn.microsoft.com/0881afec-2fa5-4f17-96a2-68a5293e0bba">DWRITE_FONT_SIMULATIONS_BOLD</a> increases weight by applying a widening algorithm to the glyph outline. This may  be used to simulate a bold weight where no designed bold weight is available.


### -field DWRITE_FONT_SIMULATIONS_OBLIQUE

Indicates that algorithmic italicization is applied to the font face. <a href="https://msdn.microsoft.com/0881afec-2fa5-4f17-96a2-68a5293e0bba">DWRITE_FONT_SIMULATIONS_OBLIQUE</a> applies obliquing (shear) to the glyph outline. This may be used to simulate an oblique/italic style where no designed oblique/italic style is available.


## -remarks



Style simulations are not recommended for good typographic quality.



