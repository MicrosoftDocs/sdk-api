---
UID: NS:usp10.tag_SCRIPT_ITEM
title: SCRIPT_ITEM (usp10.h)
description: Contains a script item, including a SCRIPT_ANALYSIS structure with the string offset of the first character of the item.
helpviewer_keywords: ["SCRIPT_ITEM","SCRIPT_ITEM structure [Internationalization for Windows Applications]","_win32_SCRIPT_ITEM_str","intl.script_item","usp10/SCRIPT_ITEM"]
old-location: intl\script_item.htm
tech.root: Intl
ms.assetid: d309f3a7-fec3-4999-bbbe-bb85ceecb4c4
ms.date: 12/05/2018
ms.keywords: SCRIPT_ITEM, SCRIPT_ITEM structure [Internationalization for Windows Applications], _win32_SCRIPT_ITEM_str, intl.script_item, usp10/SCRIPT_ITEM
req.header: usp10.h
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
targetos: Windows
req.typenames: SCRIPT_ITEM
req.redist: Internet Explorer 5 or later onWindows Me/98/95
ms.custom: 19H1
f1_keywords:
 - tag_SCRIPT_ITEM
 - usp10/tag_SCRIPT_ITEM
 - SCRIPT_ITEM
 - usp10/SCRIPT_ITEM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Usp10.h
api_name:
 - SCRIPT_ITEM
---

# SCRIPT_ITEM structure


## -description

Contains a script item, including a <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a> structure with the string offset of the first character of the item.

## -struct-fields

### -field iCharPos

Offset from the beginning of the itemized string to the first character of the item, counted in Unicode code points (WCHAR values).

### -field a

A <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a> structure containing the analysis of the item.

## -see-also

<a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype">ScriptItemizeOpenType</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-structures">Uniscribe Structures</a>