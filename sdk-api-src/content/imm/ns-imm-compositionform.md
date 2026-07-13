---
UID: NS:imm.tagCOMPOSITIONFORM
title: COMPOSITIONFORM (imm.h)
description: The COMPOSITIONFORM (imm.h) structure contains style and position information for a composition window.
helpviewer_keywords: ["*LPCOMPOSITIONFORM","*NPCOMPOSITIONFORM","*PCOMPOSITIONFORM","COMPOSITIONFORM","COMPOSITIONFORM structure [Internationalization for Windows Applications]","PCOMPOSITIONFORM","PCOMPOSITIONFORM structure pointer [Internationalization for Windows Applications]","_win32_COMPOSITIONFORM_str","imm/COMPOSITIONFORM","imm/PCOMPOSITIONFORM","intl.compositionform","tagCOMPOSITIONFORM"]
old-location: intl\compositionform.htm
tech.root: Intl
ms.assetid: 9b76474a-1ea9-4fcf-9fa8-deee5009a7ba
ms.date: 08/04/2022
ms.keywords: '*LPCOMPOSITIONFORM, *NPCOMPOSITIONFORM, *PCOMPOSITIONFORM, COMPOSITIONFORM, COMPOSITIONFORM structure [Internationalization for Windows Applications], PCOMPOSITIONFORM, PCOMPOSITIONFORM structure pointer [Internationalization for Windows Applications], _win32_COMPOSITIONFORM_str, imm/COMPOSITIONFORM, imm/PCOMPOSITIONFORM, intl.compositionform, tagCOMPOSITIONFORM'
req.header: imm.h
req.include-header: Immdev.h, Windows.h
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
req.typenames: COMPOSITIONFORM, *PCOMPOSITIONFORM, *NPCOMPOSITIONFORM, *LPCOMPOSITIONFORM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCOMPOSITIONFORM
 - imm/tagCOMPOSITIONFORM
 - PCOMPOSITIONFORM
 - imm/PCOMPOSITIONFORM
 - COMPOSITIONFORM
 - imm/COMPOSITIONFORM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Imm.h
api_name:
 - COMPOSITIONFORM
---

# COMPOSITIONFORM structure


## -description

Contains style and position information for a composition window.

## -struct-fields

### -field dwStyle

Position style. This member can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>CFS_DEFAULT</td>
<td>Move the composition window to the default position. The IME window can display the composition window outside the client area, such as in a floating window.</td>
</tr>
<tr>
<td>CFS_FORCE_POSITION</td>
<td>Display the upper left corner of the composition window at exactly the position specified by <b>ptCurrentPos</b>. The coordinates are relative to the upper left corner of the window containing the composition window and are not subject to adjustment by the IME.</td>
</tr>
<tr>
<td>CFS_POINT</td>
<td>Display the upper left corner of the composition window at the position specified by <b>ptCurrentPos</b>. The coordinates are relative to the upper left corner of the window containing the composition window and are subject to adjustment by the IME.</td>
</tr>
<tr>
<td>CFS_RECT</td>
<td>Display the composition window at the position specified by <b>rcArea</b>. The coordinates are relative to the upper left of the window containing the composition window.</td>
</tr>
</table>

### -field ptCurrentPos

A <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure containing the coordinates of the upper left corner of the composition window.

### -field rcArea

A <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure containing the coordinates of the upper left and lower right corners of the composition window.

## -remarks

Some IME windows adjust the composition window position specified by the system or the application. The CFS_FORCE_POSITION directs the IME window to skip this adjustment.

## -see-also

<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-structures">Input Method Manager Structures</a>
