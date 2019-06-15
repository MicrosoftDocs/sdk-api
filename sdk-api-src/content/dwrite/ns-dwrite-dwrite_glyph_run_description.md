---
UID: NS:dwrite.DWRITE_GLYPH_RUN_DESCRIPTION
title: DWRITE_GLYPH_RUN_DESCRIPTION (dwrite.h)
author: windows-sdk-content
description: Contains additional properties related to those in DWRITE_GLYPH_RUN.
old-location: directwrite\dwrite_glyph_run_description.htm
tech.root: DirectWrite
ms.assetid: 0fb25253-274a-42b7-8491-525d0550ce39
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DWRITE_GLYPH_RUN_DESCRIPTION, DWRITE_GLYPH_RUN_DESCRIPTION structure [Direct Write], directwrite.dwrite_glyph_run_description, dwrite/DWRITE_GLYPH_RUN_DESCRIPTION
ms.topic: struct
f1_keywords: ["dwrite/DWRITE_GLYPH_RUN_DESCRIPTION"]
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
 - DWRITE_GLYPH_RUN_DESCRIPTION
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DWRITE_GLYPH_RUN_DESCRIPTION structure


## -description


Contains additional properties related to those in <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/ns-dwrite-dwrite_glyph_run">DWRITE_GLYPH_RUN</a>.


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

Corresponding text position in the string this glyph run came from.  This is relative to the beginning of the string represented by the <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a> object.

