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

# DWRITE_GLYPH_RUN_DESCRIPTION structure


## -description


Contains additional properties related to those in <a href="https://msdn.microsoft.com/2997d63f-8d33-44c3-9617-cfffe5f61f7d">DWRITE_GLYPH_RUN</a>.


## -struct-fields




### -field localeName

Type: <b>const WCHAR*</b>

An array of characters containing the locale name associated with this run.


### -field string

Type: <b>const WCHAR*</b>

An array of characters containing the text associated with the glyphs.


### -field stringLength

Type: <b>UINT32</b>

The number of characters in UTF16 code-units. Note that this may be different than the number of glyphs.


### -field clusterMap

Type: <b>const UINT16*</b>

An array of indices to the glyph indices array, of the first glyphs of all the glyph clusters of the glyphs to render.


### -field textPosition

Type: <b>UINT32 </b>

Corresponding text position in the string this glyph run came from.  This is relative to the beginning of the string represented by the <a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a> object.

