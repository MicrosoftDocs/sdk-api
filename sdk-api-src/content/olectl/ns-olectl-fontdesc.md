---
UID: NS:olectl.tagFONTDESC
title: FONTDESC (olectl.h)
author: windows-sdk-content
description: Contains parameters used to create a font object through the OleCreateFontIndirect function.
old-location: com\fontdesc.htm
tech.root: com
ms.assetid: c677b0ba-fd52-40e8-b7c3-b80a01c9fb26
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPFONTDESC, FONTDESC, FONTDESC structure [COM], LPFONTDESC, LPFONTDESC structure pointer [COM], _ctrl_FONTDESC, com.fontdesc, olectl/FONTDESC, olectl/LPFONTDESC"
ms.topic: struct
f1_keywords: 
 - "olectl/FONTDESC"
dev_langs:
 - c++
req.header: olectl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Olectl.h
api_name:
 - FONTDESC
targetos: Windows
req.typenames: FONTDESC, *LPFONTDESC
req.redist: 
ms.custom: 19H1
---

# FONTDESC structure


## -description


Contains parameters used to create a font object through the <a href="https://docs.microsoft.com/windows/desktop/api/olectl/nf-olectl-olecreatefontindirect">OleCreateFontIndirect</a> function.


## -struct-fields




### -field cbSizeofstruct

The size of the structure, in bytes.


### -field lpstrName

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/wtypesbase/nf-wtypesbase-olestr">OLESTR</a> that specifies the caller-owned string specifying the font name.

cySize


### -field cySize

Initial point size of the font. Use the <b>int64</b> member of the <a href="http://go.microsoft.com/fwlink/p/?linkid=146163">CY</a> structure and scale your font size (in points) by 10000.


### -field sWeight

Initial weight of the font. If the weight is below 550 (the average of FW_NORMAL, 400, and FW_BOLD, 700), then the <b>Bold</b> property is also initialized to <b>FALSE</b>. If the weight is above 550, the <b>Bold</b> property is set to <b>TRUE</b>.


### -field sCharset

Initial character set of the font.


### -field fItalic

Initial italic state of the font.


### -field fUnderline

Initial underline state of the font.


### -field fStrikethrough

Initial strikethrough state of the font.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/olectl/nf-olectl-olecreatefontindirect">OleCreateFontIndirect</a>
 

 

