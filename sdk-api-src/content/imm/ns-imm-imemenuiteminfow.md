---
UID: NS:imm.tagIMEMENUITEMINFOW
title: IMEMENUITEMINFOW (imm.h)
description: The IMEMENUITEMINFOW (Unicode) structure (imm.h) contains information about IME menu items.
helpviewer_keywords: ["*LPIMEMENUITEMINFOW","*NPIMEMENUITEMINFOW","*PIMEMENUITEMINFOW","IMEMENUITEMINFO","IMEMENUITEMINFO structure [Internationalization for Windows Applications]","IMEMENUITEMINFOA","IMEMENUITEMINFOW","PIMEMENUITEMINFO","PIMEMENUITEMINFO structure pointer [Internationalization for Windows Applications]","_win32_IMEMENUITEMINFO_str","imm/IMEMENUITEMINFO","imm/IMEMENUITEMINFOA","imm/IMEMENUITEMINFOW","imm/PIMEMENUITEMINFO","intl.imemenuiteminfo","tagIMEMENUITEMINFOA","tagIMEMENUITEMINFOW"]
old-location: intl\imemenuiteminfo.htm
tech.root: Intl
ms.assetid: 2e00993f-6720-4139-8097-a3d830e661ca
ms.date: 08/04/2022
ms.keywords: '*LPIMEMENUITEMINFOW, *NPIMEMENUITEMINFOW, *PIMEMENUITEMINFOW, IMEMENUITEMINFO, IMEMENUITEMINFO structure [Internationalization for Windows Applications], IMEMENUITEMINFOA, IMEMENUITEMINFOW, PIMEMENUITEMINFO, PIMEMENUITEMINFO structure pointer [Internationalization for Windows Applications], _win32_IMEMENUITEMINFO_str, imm/IMEMENUITEMINFO, imm/IMEMENUITEMINFOA, imm/IMEMENUITEMINFOW, imm/PIMEMENUITEMINFO, intl.imemenuiteminfo, tagIMEMENUITEMINFOA, tagIMEMENUITEMINFOW'
req.header: imm.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: IMEMENUITEMINFOW (Unicode) and IMEMENUITEMINFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IMEMENUITEMINFOW, *PIMEMENUITEMINFOW, *NPIMEMENUITEMINFOW, *LPIMEMENUITEMINFOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagIMEMENUITEMINFOW
 - imm/tagIMEMENUITEMINFOW
 - PIMEMENUITEMINFOW
 - imm/PIMEMENUITEMINFOW
 - IMEMENUITEMINFOW
 - imm/IMEMENUITEMINFOW
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
 - IMEMENUITEMINFO
 - IMEMENUITEMINFOA
 - IMEMENUITEMINFOW
---

# IMEMENUITEMINFOW structure


## -description

Contains information about IME menu items.

## -struct-fields

### -field cbSize

Size, in bytes, of the structure.

### -field fType

Menu item type. This member can have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>IMFT_RADIOCCHECK</td>
<td>Display checked menu items using a radio-button mark instead of a check mark if the <b>hbmpChecked</b> member is <b>NULL</b>.</td>
</tr>
<tr>
<td>IMFT_SEPARATOR</td>
<td>Menu item is a separator. A menu item separator appears as a horizontal dividing line. The <b>hbmpItem</b> and <b>szString</b> members are ignored in this case.</td>
</tr>
<tr>
<td>IMFT_SUBMENU</td>
<td>Menu item is a submenu.</td>
</tr>
</table>

### -field fState

Menu item state. This member can have one or more of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>IMFS_CHECKED</td>
<td>The menu item is checked. For more information, see the description of the <b>hbmpChecked</b> member.</td>
</tr>
<tr>
<td>IMFS_DEFAULT</td>
<td>The menu item is the default. A menu can contain only one default menu item, which is displayed in bold.</td>
</tr>
<tr>
<td>IMFS_DISABLED</td>
<td>The menu item is disabled and appears dimmed so it cannot be selected. This is equivalent to IMFS_GRAYED.</td>
</tr>
<tr>
<td>IMFS_ENABLED</td>
<td>The menu item is enabled. This is the default state.</td>
</tr>
<tr>
<td>IMFS_GRAYED</td>
<td>The menu item is disabled and appears dimmed so it cannot be selected. This is equivalent to IMFS_DISABLED.</td>
</tr>
<tr>
<td>IMFS_HILITE</td>
<td>The menu item is highlighted.</td>
</tr>
<tr>
<td>IMFS_UNCHECKED</td>
<td>The menu item is unchecked. For more information about unchecked menu items, see the description of the <b>hbmpUnchecked</b> member.</td>
</tr>
<tr>
<td>IMFS_UNHILITE</td>
<td>The menu item is not highlighted. This is the default state.</td>
</tr>
</table>

### -field wID

Application-defined 16-bit value that identifies the menu item.

### -field hbmpChecked

Handle to the bitmap to display next to the item if it is checked. If this member is <b>NULL</b>, a default bitmap is used. If the IMFT_RADIOCHECK type value is specified, the default bitmap is a bullet. Otherwise, it is a check mark.

### -field hbmpUnchecked

Handle to the bitmap to display next to the item if it is not checked. If this member is <b>NULL</b>, no bitmap is used.

### -field dwItemData

Application-defined value associated with the menu item.

### -field szString

Content of the menu item. This is a null-terminated string.

### -field hbmpItem

Handle to a bitmap to display.

## -see-also

<a href="/windows/desktop/api/imm/nf-imm-immgetimemenuitemsa">ImmGetImeMenuItems</a>



<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-structures">Input Method Manager Structures</a>

## -remarks

> [!NOTE]
> The imm.h header defines IMEMENUITEMINFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
