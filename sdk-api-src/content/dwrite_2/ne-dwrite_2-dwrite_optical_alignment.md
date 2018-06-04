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

# DWRITE_OPTICAL_ALIGNMENT enumeration


## -description


The optical margin alignment mode.


        By default, glyphs are aligned to the margin by the default origin and side-bearings of the glyph. 
        If you specify <b>DWRITE_OPTICAL_ALIGNMENT_NO_SIDE_BEARINGS</b>, then the alignment uses the side bearings to offset the glyph 
        from the aligned edge to ensure the ink of the glyphs are aligned.
      


## -enum-fields




### -field DWRITE_OPTICAL_ALIGNMENT_NONE

Align to the default origin and side-bearings of the glyph.


### -field DWRITE_OPTICAL_ALIGNMENT_NO_SIDE_BEARINGS

Align to the ink of the glyphs, such that the black box abuts the margins.

