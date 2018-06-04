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

# DWRITE_SHAPING_GLYPH_PROPERTIES structure


## -description


Contains shaping output properties for an output glyph.


## -struct-fields




### -field justification

Type: <b>UINT16</b>

Indicates that the glyph has justification applied.


### -field isClusterStart

Type: <b>UINT16</b>

Indicates that the glyph is the start of a cluster.


### -field isDiacritic

Type: <b>UINT16</b>

Indicates that the glyph is a diacritic mark.


### -field isZeroWidthSpace

Type: <b>UINT16</b>

Indicates that the glyph is a word boundary with no visible space.


### -field reserved

Type: <b>UINT16</b>

Reserved for future use.

