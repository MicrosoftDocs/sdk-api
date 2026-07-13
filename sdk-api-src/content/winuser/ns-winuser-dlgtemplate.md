---
UID: NS:winuser.DLGTEMPLATE
title: DLGTEMPLATE (winuser.h)
description: Defines the dimensions and style of a dialog box.
helpviewer_keywords: ["*LPDLGTEMPLATEA","*LPDLGTEMPLATEW","DLGTEMPLATE","DLGTEMPLATE structure [Dialog Boxes]","LPDLGTEMPLATE","LPDLGTEMPLATE structure pointer [Dialog Boxes]","_win32_DLGTEMPLATE_str","_win32_dlgtemplate_str_cpp","dlgbox.dlgtemplate","winui._win32_dlgtemplate_str","winuser/DLGTEMPLATE","winuser/LPDLGTEMPLATE"]
old-location: dlgbox\dlgtemplate.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxstructures\dlgtemplate.htm
ms.date: 12/05/2018
ms.keywords: '*LPDLGTEMPLATEA, *LPDLGTEMPLATEW, DLGTEMPLATE, DLGTEMPLATE structure [Dialog Boxes], LPDLGTEMPLATE, LPDLGTEMPLATE structure pointer [Dialog Boxes], _win32_DLGTEMPLATE_str, _win32_dlgtemplate_str_cpp, dlgbox.dlgtemplate, winui._win32_dlgtemplate_str, winuser/DLGTEMPLATE, winuser/LPDLGTEMPLATE'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DLGTEMPLATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DLGTEMPLATE
 - winuser/DLGTEMPLATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - DLGTEMPLATE
---

# DLGTEMPLATE structure


## -description

Defines the dimensions and style of a dialog box. This structure, always the first in a standard template for a dialog box, also specifies the number of controls in the dialog box and therefore specifies the number of subsequent <a href="/windows/desktop/api/winuser/ns-winuser-dlgitemtemplate">DLGITEMTEMPLATE</a> structures in the template.

## -struct-fields

### -field style

Type: <b>DWORD</b>

The style of the dialog box. This member can be a combination of <a href="/windows/desktop/winmsg/window-styles">window style values</a> (such as <b>WS_CAPTION</b> and <b>WS_SYSMENU</b>) and <a href="/windows/desktop/dlgbox/dialog-box-styles">dialog box style values</a> (such as <b>DS_CENTER</b>).

If the style member includes the <b>DS_SETFONT</b> style, the header of the dialog box template contains additional data specifying the font to use for text in the client area and controls of the dialog box. The font data begins on the 
						<b>WORD</b> boundary that follows the title array. The font data specifies a 16-bit point size value and a Unicode font name string. If possible, the system creates a font according to the specified values. Then the system sends a <a href="/windows/desktop/winmsg/wm-setfont">WM_SETFONT</a> message to the dialog box and to each control to provide a handle to the font. If <b>DS_SETFONT</b> is not specified, the dialog box template does not include the font data. 

The <b>DS_SHELLFONT</b> style is not supported in the <b>DLGTEMPLATE</b> header.

### -field dwExtendedStyle

Type: <b>DWORD</b>

The extended styles for a window. This member is not used to create dialog boxes, but applications that use dialog box templates can use it to create other types of windows. For a list of values, see <a href="/windows/desktop/winmsg/extended-window-styles">Extended Window Styles</a>.

### -field cdit

Type: <b>WORD</b>

The number of items in the dialog box.

### -field x

Type: <b>short</b>

The x-coordinate, in dialog box units, of the upper-left corner of the dialog box.

### -field y

Type: <b>short</b>

The y-coordinate, in dialog box units, of the upper-left corner of the dialog box.

### -field cx

Type: <b>short</b>

The width, in dialog box units, of the dialog box.

### -field cy

Type: <b>short</b>

The height, in dialog box units, of the dialog box.

## -remarks

In a standard template for a dialog box, the <b>DLGTEMPLATE</b> structure is always immediately followed by three variable-length arrays that specify the menu, class, and title for the dialog box. When the DS_SETFONT style is specified, these arrays are also followed by a 16-bit value specifying point size and another variable-length array specifying a typeface name. Each array consists of one or more 16-bit elements. The menu, class, title, and font arrays must be aligned on 
				<b>WORD</b> boundaries. 

Immediately following the <b>DLGTEMPLATE</b> structure is a menu array that identifies a menu resource for the dialog box. If the first element of this array is 0x0000, the dialog box has no menu and the array has no other elements. If the first element is 0xFFFF, the array has one additional element that specifies the ordinal value of a menu resource in an executable file. If the first element has any other value, the system treats the array as a null-terminated Unicode string that specifies the name of a menu resource in an executable file. 

Following the menu array is a class array that identifies the window class of the dialog box. If the first element of the array is 0x0000, the system uses the predefined dialog box class for the dialog box and the array has no other elements. If the first element is 0xFFFF, the array has one additional element that specifies the ordinal value of a predefined system window class. If the first element has any other value, the system treats the array as a null-terminated Unicode string that specifies the name of a registered window class. 

Following the class array is a title array that specifies a null-terminated Unicode string that contains the title of the dialog box. If the first element of this array is 0x0000, the dialog box has no title and the array has no other elements. 

The 16-bit point size value and the typeface array follow the title array, but only if the 
				<b>style</b> member specifies the DS_SETFONT style. The point size value
specifies the point size of the font to use for the text in the dialog box and its controls. The typeface array is a null-terminated Unicode string specifying the name of the typeface for the font. When these values are specified, the system creates a font having the specified size and typeface (if possible) and sends a <a href="/windows/desktop/winmsg/wm-setfont">WM_SETFONT</a> message to the dialog box procedure and the control window procedures as it creates the dialog box and controls. 

Following the <b>DLGTEMPLATE</b> header in a standard dialog box template are one or more <a href="/windows/desktop/api/winuser/ns-winuser-dlgitemtemplate">DLGITEMTEMPLATE</a> structures that define the dimensions and style of the controls in the dialog box. The 
				<b>cdit</b> member specifies the number of <b>DLGITEMTEMPLATE</b> structures in the template. These <b>DLGITEMTEMPLATE</b> structures must be aligned on 
				<b>DWORD</b> boundaries.

If you specify character strings in the menu, class, title, or typeface arrays, you must use Unicode strings. 

The 
				<b>x</b>, 
				<b>y</b>, 
				<b>cx</b>, and 
				<b>cy</b> members specify values in dialog box units. You can convert these values to screen units (pixels) by using the <a href="/windows/desktop/api/winuser/nf-winuser-mapdialogrect">MapDialogRect</a> function.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createdialogindirecta">CreateDialogIndirect</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createdialogindirectparama">CreateDialogIndirectParam</a>



<a href="/windows/desktop/api/winuser/ns-winuser-dlgitemtemplate">DLGITEMTEMPLATE</a>



<a href="/windows/desktop/dlgbox/dlgitemtemplateex">DLGITEMTEMPLATEEX</a>



<a href="/windows/desktop/dlgbox/dlgtemplateex">DLGTEMPLATEEX</a>



<a href="/windows/desktop/dlgbox/dialog-boxes">Dialog Boxes</a>



<a href="/windows/desktop/api/winuser/nf-winuser-dialogboxindirecta">DialogBoxIndirect</a>



<a href="/windows/desktop/api/winuser/nf-winuser-dialogboxindirectparama">DialogBoxIndirectParam</a>



<a href="/windows/desktop/api/winuser/nf-winuser-mapdialogrect">MapDialogRect</a>



<a href="/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar">MultiByteToWideChar</a>



<b>Other Resources</b>



<b>Reference</b>

