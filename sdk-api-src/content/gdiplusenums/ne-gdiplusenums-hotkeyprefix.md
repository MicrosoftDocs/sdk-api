---
UID: NE:gdiplusenums.HotkeyPrefix
title: HotkeyPrefix (gdiplusenums.h)
description: The HotkeyPrefix enumeration specifies how to display hot keys. There are three options:\_do nothing, display hot keys underlined, and hide the hot key underlines.
helpviewer_keywords: ["HotkeyPrefix","HotkeyPrefix enumeration [GDI+]","HotkeyPrefixHide","HotkeyPrefixNone","HotkeyPrefixShow","_gdiplus_ENUM_HotkeyPrefix","gdiplus._gdiplus_ENUM_HotkeyPrefix","gdiplusenums/HotkeyPrefix","gdiplusenums/HotkeyPrefixHide","gdiplusenums/HotkeyPrefixNone","gdiplusenums/HotkeyPrefixShow"]
old-location: gdiplus\_gdiplus_ENUM_HotkeyPrefix.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\hotkeyprefix.htm
ms.date: 12/05/2018
ms.keywords: HotkeyPrefix, HotkeyPrefix enumeration [GDI+], HotkeyPrefixHide, HotkeyPrefixNone, HotkeyPrefixShow, _gdiplus_ENUM_HotkeyPrefix, gdiplus._gdiplus_ENUM_HotkeyPrefix, gdiplusenums/HotkeyPrefix, gdiplusenums/HotkeyPrefixHide, gdiplusenums/HotkeyPrefixNone, gdiplusenums/HotkeyPrefixShow
req.header: gdiplusenums.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
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
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - HotkeyPrefix
 - gdiplusenums/HotkeyPrefix
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusenums.h
api_name:
 - HotkeyPrefix
---

# HotkeyPrefix enumeration


## -description

The <b>HotkeyPrefix</b> enumeration specifies how to display hot keys. There are three options: do nothing, display hot keys underlined, and hide the hot key underlines.

## -enum-fields

### -field HotkeyPrefixNone:0

Specifies that no hot key processing occurs.

### -field HotkeyPrefixShow:1

Specifies that Unicode text is scanned for ampersands (&amp;), which are interpreted as hot key markers in the same way as menu and dialog resources are processed in the Windows user interface. All pairs of ampersands are replaced by a single ampersand. All single ampersands are removed and the first character that follows the first single ampersand is displayed underlined.

### -field HotkeyPrefixHide:2

Specifies that Unicode text is scanned for ampersands (&amp;), which are substituted and removed as in HotkeyPrefixShow but no underline is shown. This option can be used when accessibility hot key underlines are not required.

## -remarks

Hot keys are keys that are programmed to provide keyboard shortcuts to functionality and are activated by pressing the ALT key. The keys are application dependent and are identified by an underscored letter, typically in a menu. An example would be the 
				<b>File</b> menu with the letter F underscored. This makes the F key a hot key to launch the 
				<b>File</b> menu.

