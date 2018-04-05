---
UID: NE:uiribbon.UI_SWATCHCOLORTYPE
title: UI_SWATCHCOLORTYPE
author: windows-driver-content
description: Specifies the values that identify how a color swatch in a DropDownColorPicker or a FontControl color picker (Text color or Text highlight) is filled.Note  These are recommendations only.
old-location: windowsribbon\windowsribbon_ui_swatchcolortype.htm
old-project: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\enums\ui_swatchcolortype.htm
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: UI_SWATCHCOLORTYPE, UI_SWATCHCOLORTYPE enumeration [Windows Ribbon], UI_SWATCHCOLORTYPE_AUTOMATIC, UI_SWATCHCOLORTYPE_NOCOLOR, UI_SWATCHCOLORTYPE_RGB, scenicintent_UI_SWATCHCOLORTYPE, uiribbon/UI_SWATCHCOLORTYPE, uiribbon/UI_SWATCHCOLORTYPE_AUTOMATIC, uiribbon/UI_SWATCHCOLORTYPE_NOCOLOR, uiribbon/UI_SWATCHCOLORTYPE_RGB, windowsribbon.windowsribbon_ui_swatchcolortype
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: UI_SWATCHCOLORTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Uiribbon.h
api_name:
-	UI_SWATCHCOLORTYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# UI_SWATCHCOLORTYPE enumeration


## -description


Specifies the values that identify how a color swatch in a <a href="https://msdn.microsoft.com/fc4df978-9c52-43d5-8a5e-e015aa7058cd">DropDownColorPicker</a> or a <a href="https://msdn.microsoft.com/98eddab5-28cb-4b9d-a788-ee28dd6055b1">FontControl</a> color picker (<b>Text color</b> or <b>Text highlight</b>) is filled.
<div class="alert"><b>Note</b>  These are recommendations only. The application can associate any fill type with these values.</div><div> </div>

## -enum-fields




### -field UI_SWATCHCOLORTYPE_NOCOLOR

The swatch is transparent.


### -field UI_SWATCHCOLORTYPE_AUTOMATIC

The swatch is filled with a solid RGB color bound to <a href="http://go.microsoft.com/fwlink/p/?linkid=143871">GetSysColor(COLOR_WINDOWTEXT)</a>.


### -field UI_SWATCHCOLORTYPE_RGB

The swatch is filled with a solid RGB color.


## -see-also




<a href="https://msdn.microsoft.com/8499a096-aac3-4af3-a4c9-eebf53698744">Constants and Enumerations</a>
 

 

