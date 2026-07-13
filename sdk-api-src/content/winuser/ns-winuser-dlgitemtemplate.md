---
UID: NS:winuser.DLGITEMTEMPLATE
title: DLGITEMTEMPLATE (winuser.h)
description: Defines the dimensions and style of a control in a dialog box. One or more of these structures are combined with a DLGTEMPLATE structure to form a standard template for a dialog box.
helpviewer_keywords: ["*LPDLGITEMTEMPLATEA","*LPDLGITEMTEMPLATEW","*PDLGITEMTEMPLATEA","*PDLGITEMTEMPLATEW","DLGITEMTEMPLATE","DLGITEMTEMPLATE structure [Dialog Boxes]","PDLGITEMTEMPLATE","PDLGITEMTEMPLATE structure pointer [Dialog Boxes]","_win32_DLGITEMTEMPLATE_str","_win32_dlgitemtemplate_str_cpp","dlgbox.dlgitemtemplate","winui._win32_dlgitemtemplate_str","winuser/DLGITEMTEMPLATE","winuser/PDLGITEMTEMPLATE"]
old-location: dlgbox\dlgitemtemplate.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxstructures\dlgitemtemplate.htm
ms.date: 12/05/2018
ms.keywords: '*LPDLGITEMTEMPLATEA, *LPDLGITEMTEMPLATEW, *PDLGITEMTEMPLATEA, *PDLGITEMTEMPLATEW, DLGITEMTEMPLATE, DLGITEMTEMPLATE structure [Dialog Boxes], PDLGITEMTEMPLATE, PDLGITEMTEMPLATE structure pointer [Dialog Boxes], _win32_DLGITEMTEMPLATE_str, _win32_dlgitemtemplate_str_cpp, dlgbox.dlgitemtemplate, winui._win32_dlgitemtemplate_str, winuser/DLGITEMTEMPLATE, winuser/PDLGITEMTEMPLATE'
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
req.typenames: DLGITEMTEMPLATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DLGITEMTEMPLATE
 - winuser/DLGITEMTEMPLATE
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
 - DLGITEMTEMPLATE
---

# DLGITEMTEMPLATE structure


## -description

Defines the dimensions and style of a control in a dialog box. One or more of these structures are combined with a <a href="/windows/desktop/api/winuser/ns-winuser-dlgtemplate">DLGTEMPLATE</a> structure to form a standard template for a dialog box.

## -struct-fields

### -field style

Type: <b>DWORD</b>

The style of the control. This member can be a combination of <a href="/windows/desktop/winmsg/window-styles">window style values</a> (such as <b>WS_BORDER</b>) and one or more of the <a href="/windows/desktop/Controls/common-control-styles">control style values</a> (such as <b>BS_PUSHBUTTON</b> and <b>ES_LEFT</b>).

### -field dwExtendedStyle

Type: <b>DWORD</b>

The extended styles for a window. This member is not used to create controls in dialog boxes, but applications that use dialog box templates can use it to create other types of windows. For a list of values, see <a href="/windows/desktop/winmsg/extended-window-styles">Extended Window Styles</a>.

### -field x

Type: <b>short</b>

The 
					<i>x</i>-coordinate, in dialog box units, of the upper-left corner of the control. This coordinate is always relative to the upper-left corner of the dialog box's client area.

### -field y

Type: <b>short</b>

The 
					<i>y</i>-coordinate, in dialog box units, of the upper-left corner of the control. This coordinate is always relative to the upper-left corner of the dialog box's client area.

### -field cx

Type: <b>short</b>

The width, in dialog box units, of the control.

### -field cy

Type: <b>short</b>

The height, in dialog box units, of the control.

### -field id

Type: <b>WORD</b>

The control identifier.

## -remarks

In a standard template for a dialog box, the <b>DLGITEMTEMPLATE</b> structure is always immediately followed by three variable-length arrays specifying the class, title, and creation data for the control. Each array consists of one or more 16-bit elements. 

Each <b>DLGITEMTEMPLATE</b> structure in the template must be aligned on a 
				<b>DWORD</b> boundary. The class and title arrays must be aligned on 
				<b>WORD</b> boundaries. The creation data array must be aligned on a 
				<b>WORD</b> boundary. 

Immediately following each <b>DLGITEMTEMPLATE</b> structure is a class array that specifies the window class of the control. If the first element of this array is any value other than 0xFFFF, the system treats the array as a null-terminated Unicode string that specifies the name of a registered window class. If the first element is 0xFFFF, the array has one additional element that specifies the ordinal value of a predefined system class. The ordinal can be one of the following atom values.

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>0x0080</td>
<td>Button</td>
</tr>
<tr>
<td>0x0081</td>
<td>Edit</td>
</tr>
<tr>
<td>0x0082</td>
<td>Static</td>
</tr>
<tr>
<td>0x0083</td>
<td>List box</td>
</tr>
<tr>
<td>0x0084</td>
<td>Scroll bar</td>
</tr>
<tr>
<td>0x0085</td>
<td>Combo box</td>
</tr>
</table>
 

Following the class array is a title array that contains the initial text or resource identifier of the control. If the first element of this array is 0xFFFF, the array has one additional element that specifies an ordinal value of a resource, such as an icon, in an executable file. You can use a resource identifier for controls, such as static icon controls, that load and display an icon or other resource rather than text. If the first element is any value other than 0xFFFF, the system treats the array as a null-terminated Unicode string that specifies the initial text. 

The creation data array begins at the next 
				<b>WORD</b> boundary after the title array. This creation data can be of any size and format. If the first word of the creation data array is nonzero, it indicates the size, in bytes, of the creation data (including the size word). The control's window procedure must be able to interpret the data. When the system creates the control, it passes a pointer to this data in the 
				<i>lParam</i> parameter of the <a href="/windows/desktop/winmsg/wm-create">WM_CREATE</a> message that it sends to the control. 

If you specify character strings in the class and title arrays, you must use Unicode strings. Use the 
				<a href="/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar">MultiByteToWideChar</a> function to generate Unicode strings from ANSI strings.

The 
				<b>x</b>, 
				<b>y</b>, 
				<b>cx</b>, and 
				<b>cy</b> members specify values in dialog box units. You can convert these values to screen units (pixels) by using the <a href="/windows/desktop/api/winuser/nf-winuser-mapdialogrect">MapDialogRect</a> function.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createdialogindirecta">CreateDialogIndirect</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createdialogindirectparama">CreateDialogIndirectParam</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a>



<a href="/windows/desktop/dlgbox/dlgitemtemplateex">DLGITEMTEMPLATEEX</a>



<a href="/windows/desktop/api/winuser/ns-winuser-dlgtemplate">DLGTEMPLATE</a>



<a href="/windows/desktop/dlgbox/dlgtemplateex">DLGTEMPLATEEX</a>



<a href="/windows/desktop/dlgbox/dialog-boxes">Dialog Boxes</a>



<a href="/windows/desktop/api/winuser/nf-winuser-dialogboxindirecta">DialogBoxIndirect</a>



<a href="/windows/desktop/api/winuser/nf-winuser-dialogboxindirectparama">DialogBoxIndirectParam</a>



<a href="/windows/desktop/api/winuser/nf-winuser-mapdialogrect">MapDialogRect</a>



<a href="/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar">MultiByteToWideChar</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/winmsg/wm-create">WM_CREATE</a>

