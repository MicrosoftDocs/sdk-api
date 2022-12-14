---
UID: NF:winuser.MapDialogRect
title: MapDialogRect function (winuser.h)
description: Converts the specified dialog box units to screen units (pixels).
helpviewer_keywords: ["MapDialogRect","MapDialogRect function [Dialog Boxes]","_win32_MapDialogRect","_win32_mapdialogrect_cpp","dlgbox.mapdialogrect","winui._win32_mapdialogrect","winuser/MapDialogRect"]
old-location: dlgbox\mapdialogrect.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\mapdialogrect.htm
ms.date: 12/05/2018
ms.keywords: MapDialogRect, MapDialogRect function [Dialog Boxes], _win32_MapDialogRect, _win32_mapdialogrect_cpp, dlgbox.mapdialogrect, winui._win32_mapdialogrect, winuser/MapDialogRect
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
 - MapDialogRect
 - winuser/MapDialogRect
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
 - MapDialogRect
req.apiset: ext-ms-win-ntuser-dialogbox-l1-1-2 (introduced in Windows 10, version 10.0.10240)
---

# MapDialogRect function


## -description

Converts the specified dialog box units to screen units (pixels). The function replaces the coordinates in the specified <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure with the converted coordinates, which allows the structure to be used to create a dialog box or position a control within a dialog box.

## -parameters

### -param hDlg [in]

Type: <b>HWND</b>

A handle to a dialog box. This function accepts only handles returned by one of the dialog box creation functions; handles for other windows are not valid.

### -param lpRect [in, out]

Type: <b>LPRECT</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the dialog box coordinates to be converted.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>MapDialogRect</b> function assumes that the initial coordinates in the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure represent dialog box units. To convert these coordinates from dialog box units to pixels, the function retrieves the current horizontal and vertical base units for the dialog box, then applies the following formulas:
				
				


``` syntax

left   = MulDiv(left,   baseunitX, 4);
right  = MulDiv(right,  baseunitX, 4);
top    = MulDiv(top,    baseunitY, 8);
bottom = MulDiv(bottom, baseunitY, 8);
```

If the dialog box template has the <a href="/windows/desktop/dlgbox/about-dialog-boxes">DS_SETFONT</a> or <b>DS_SHELLFONT</b> style, the base units are the average width and height, in pixels, of the characters in the font specified by the template.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/dlgbox/dialog-boxes">Dialog Boxes</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getdialogbaseunits">GetDialogBaseUnits</a>



<b>Other Resources</b>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<b>Reference</b>
