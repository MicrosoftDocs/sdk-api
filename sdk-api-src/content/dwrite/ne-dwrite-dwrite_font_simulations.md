---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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



