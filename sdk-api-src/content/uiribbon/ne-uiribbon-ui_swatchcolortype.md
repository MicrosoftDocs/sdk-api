---
UID: NE:uiribbon.UI_SWATCHCOLORTYPE
title: UI_SWATCHCOLORTYPE (uiribbon.h)
description: Specifies the values that identify how a color swatch in a DropDownColorPicker or a FontControl color picker (Text color or Text highlight) is filled.Note  These are recommendations only.
helpviewer_keywords: ["UI_SWATCHCOLORTYPE","UI_SWATCHCOLORTYPE enumeration [Windows Ribbon]","UI_SWATCHCOLORTYPE_AUTOMATIC","UI_SWATCHCOLORTYPE_NOCOLOR","UI_SWATCHCOLORTYPE_RGB","scenicintent_UI_SWATCHCOLORTYPE","uiribbon/UI_SWATCHCOLORTYPE","uiribbon/UI_SWATCHCOLORTYPE_AUTOMATIC","uiribbon/UI_SWATCHCOLORTYPE_NOCOLOR","uiribbon/UI_SWATCHCOLORTYPE_RGB","windowsribbon.windowsribbon_ui_swatchcolortype"]
old-location: windowsribbon\windowsribbon_ui_swatchcolortype.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\enums\ui_swatchcolortype.htm
ms.date: 12/05/2018
ms.keywords: UI_SWATCHCOLORTYPE, UI_SWATCHCOLORTYPE enumeration [Windows Ribbon], UI_SWATCHCOLORTYPE_AUTOMATIC, UI_SWATCHCOLORTYPE_NOCOLOR, UI_SWATCHCOLORTYPE_RGB, scenicintent_UI_SWATCHCOLORTYPE, uiribbon/UI_SWATCHCOLORTYPE, uiribbon/UI_SWATCHCOLORTYPE_AUTOMATIC, uiribbon/UI_SWATCHCOLORTYPE_NOCOLOR, uiribbon/UI_SWATCHCOLORTYPE_RGB, windowsribbon.windowsribbon_ui_swatchcolortype
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: UI_SWATCHCOLORTYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UI_SWATCHCOLORTYPE
 - uiribbon/UI_SWATCHCOLORTYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Uiribbon.h
api_name:
 - UI_SWATCHCOLORTYPE
---

# UI_SWATCHCOLORTYPE enumeration


## -description

Specifies the values that identify how a color swatch in a <a href="/windows/desktop/windowsribbon/windowsribbon-element-dropdowncolorpicker">DropDownColorPicker</a> or a <a href="/windows/desktop/windowsribbon/windowsribbon-element-fontcontrol">FontControl</a> color picker (<b>Text color</b> or <b>Text highlight</b>) is filled.
<div class="alert"><b>Note</b>  These are recommendations only. The application can associate any fill type with these values.</div><div> </div>

## -enum-fields

### -field UI_SWATCHCOLORTYPE_NOCOLOR:0

The swatch is transparent.

### -field UI_SWATCHCOLORTYPE_AUTOMATIC:1

The swatch is filled with a solid RGB color bound to <a href="/windows/win32/api/winuser/nf-winuser-getsyscolor">GetSysColor(COLOR_WINDOWTEXT)</a>.

### -field UI_SWATCHCOLORTYPE_RGB:2

The swatch is filled with a solid RGB color.

## -see-also

<a href="/windows/desktop/windowsribbon/windowsribbon-reference-enumerations">Constants and Enumerations</a>
