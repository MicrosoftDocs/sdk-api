---
UID: NF:winuser.GetDialogBaseUnits
title: GetDialogBaseUnits function (winuser.h)
description: Retrieves the system's dialog base units, which are the average width and height of characters in the system font.
helpviewer_keywords: ["GetDialogBaseUnits","GetDialogBaseUnits function [Dialog Boxes]","_win32_GetDialogBaseUnits","_win32_getdialogbaseunits_cpp","dlgbox.getdialogbaseunits","winui._win32_getdialogbaseunits","winuser/GetDialogBaseUnits"]
old-location: dlgbox\getdialogbaseunits.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\getdialogbaseunits.htm
ms.date: 12/05/2018
ms.keywords: GetDialogBaseUnits, GetDialogBaseUnits function [Dialog Boxes], _win32_GetDialogBaseUnits, _win32_getdialogbaseunits_cpp, dlgbox.getdialogbaseunits, winui._win32_getdialogbaseunits, winuser/GetDialogBaseUnits
req.header: winuser.h
req.include-header: Windows.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetDialogBaseUnits
 - winuser/GetDialogBaseUnits
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - ext-ms-win-ntuser-dialogbox-l1-1-2.dll
api_name:
 - GetDialogBaseUnits
req.apiset: ext-ms-win-ntuser-dialogbox-l1-1-2 (introduced in Windows 10, version 10.0.10240)
---

# GetDialogBaseUnits function


## -description

Retrieves the system's dialog base units, which are the average width and height of characters in the system font. For dialog boxes that use the system font, you can use these values to convert between dialog template units, as specified in dialog box templates, and pixels. For dialog boxes that do not use the system font, the conversion from dialog template units to pixels depends on the font used by the dialog box.

For either type of dialog box, it is easier to use the <a href="/windows/desktop/api/winuser/nf-winuser-mapdialogrect">MapDialogRect</a> function to perform the conversion. <b>MapDialogRect</b> takes the font into account and correctly converts a rectangle from dialog template units into pixels.



## -returns

Type: <b>LONG</b>

The function returns the dialog base units. The low-order word of the return value contains the horizontal dialog box base unit, and the high-order word contains the vertical dialog box base unit.

## -remarks

The horizontal base unit returned by <b>GetDialogBaseUnits</b> is equal to the average width, in pixels, of the characters in the system font; the vertical base unit is equal to the height, in pixels, of the font.

The system font is used only if the dialog box template fails to specify a font. Most dialog box templates specify a font; as a result, this function is not useful for most dialog boxes.
 

For a dialog box that does not use the system font, the base units are the average width and height, in pixels, of the characters in the dialog's font. You can use the <a href="/windows/desktop/api/wingdi/nf-wingdi-gettextmetrics">GetTextMetrics</a> and <a href="/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a">GetTextExtentPoint32</a> functions to calculate these values for a selected font. However, by using the <a href="/windows/desktop/api/winuser/nf-winuser-mapdialogrect">MapDialogRect</a> function, you can avoid errors that might result if your calculations differ from those performed by the system.

Each horizontal base unit is equal to 4 horizontal dialog template units; each vertical base unit is equal to 8 vertical dialog template units. Therefore, to convert dialog template units to pixels, use the following formulas: 		
				
				


```

pixelX = MulDiv(templateunitX, baseunitX, 4);
pixelY = MulDiv(templateunitY, baseunitY, 8);
```


Similarly, to convert from pixels to dialog template units, use the following formulas:
				
				


```

templateunitX = MulDiv(pixelX, 4, baseunitX);
templateunitY = MulDiv(pixelY, 8, baseunitY);
```



#### Examples

For an example, see "Creating a Combo Box Toolbar" in <a href="/windows/desktop/Controls/using-combo-boxes">Using Combo Boxes</a>.

<div class="code"></div>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/dlgbox/dialog-boxes">Dialog Boxes</a>



<a href="/windows/desktop/api/winuser/nf-winuser-mapdialogrect">MapDialogRect</a>



<b>Reference</b>
