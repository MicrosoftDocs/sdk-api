---
UID: NS:winuser.__unnamed_struct_5
title: DLGITEMTEMPLATE
author: windows-sdk-content
description: Defines the dimensions and style of a control in a dialog box. One or more of these structures are combined with a DLGTEMPLATE structure to form a standard template for a dialog box.
old-location: dlgbox\dlgitemtemplate.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxstructures\dlgitemtemplate.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPDLGITEMTEMPLATEA, *LPDLGITEMTEMPLATEW, *PDLGITEMTEMPLATEA, *PDLGITEMTEMPLATEW, DLGITEMTEMPLATE, DLGITEMTEMPLATE structure [Dialog Boxes], PDLGITEMTEMPLATE, PDLGITEMTEMPLATE structure pointer [Dialog Boxes], _win32_DLGITEMTEMPLATE_str, _win32_dlgitemtemplate_str_cpp, dlgbox.dlgitemtemplate, winui._win32_dlgitemtemplate_str, winuser/DLGITEMTEMPLATE, winuser/PDLGITEMTEMPLATE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - DLGITEMTEMPLATE
product: Windows
targetos: Windows
req.typenames: DLGITEMTEMPLATE
req.redist: 
---

# DLGITEMTEMPLATE structure


## -description


Defines the dimensions and style of a control in a dialog box. One or more of these structures are combined with a <a href="https://msdn.microsoft.com/e6164c92-51ec-48ea-9a61-80e55de7a6d8">DLGTEMPLATE</a> structure to form a standard template for a dialog box. 


## -struct-fields




### -field style

Type: <b>DWORD</b>

The style of the control. This member can be a combination of <a href="winui._win32_Window_Styles">window style values</a> (such as <b>WS_BORDER</b>) and one or more of the <a href="https://msdn.microsoft.com/aab0cd68-ede7-474b-8695-c75805669716">control style values</a> (such as <b>BS_PUSHBUTTON</b> and <b>ES_LEFT</b>). 


### -field dwExtendedStyle

Type: <b>DWORD</b>

The extended styles for a window. This member is not used to create controls in dialog boxes, but applications that use dialog box templates can use it to create other types of windows. For a list of values, see <a href="https://msdn.microsoft.com/5830B16E-CD52-4a1a-A1BD-3AFE66BA5FDD">Extended Window Styles</a>.


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
				<i>lParam</i> parameter of the <a href="https://msdn.microsoft.com/d484d0fc-bad0-4fcb-bf4b-37cbc50846ee">WM_CREATE</a> message that it sends to the control. 

If you specify character strings in the class and title arrays, you must use Unicode strings. Use the 
				<a href="https://msdn.microsoft.com/a117fdfe-b52b-466f-9300-6455e91ea2a8">MultiByteToWideChar</a> function to generate Unicode strings from ANSI strings.

The 
				<b>x</b>, 
				<b>y</b>, 
				<b>cx</b>, and 
				<b>cy</b> members specify values in dialog box units. You can convert these values to screen units (pixels) by using the <a href="https://msdn.microsoft.com/20f6477e-d0a3-4781-9f57-0ff05e68c5e6">MapDialogRect</a> function. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/b3bddf88-be6d-4aa3-9e23-257126bdfc15">CreateDialogIndirect</a>



<a href="https://msdn.microsoft.com/f8ed581b-992e-41b8-a2f5-906b9bafa578">CreateDialogIndirectParam</a>



<a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a>



<a href="https://msdn.microsoft.com/c60fd8db-ee4b-433b-a2fb-68b9a677bac8">DLGITEMTEMPLATEEX</a>



<a href="https://msdn.microsoft.com/e6164c92-51ec-48ea-9a61-80e55de7a6d8">DLGTEMPLATE</a>



<a href="https://msdn.microsoft.com/9f016cc6-56e2-45d3-8773-1b405fc10d29">DLGTEMPLATEEX</a>



<a href="https://msdn.microsoft.com/07ebee3c-5aa7-4b0d-b6cb-e642e01e1a88">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/0af783b3-804d-4075-8046-5109f37e275d">DialogBoxIndirect</a>



<a href="https://msdn.microsoft.com/ce241d7b-8775-4c0d-bb4b-87df5f58f8a8">DialogBoxIndirectParam</a>



<a href="https://msdn.microsoft.com/20f6477e-d0a3-4781-9f57-0ff05e68c5e6">MapDialogRect</a>



<a href="https://msdn.microsoft.com/a117fdfe-b52b-466f-9300-6455e91ea2a8">MultiByteToWideChar</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/d484d0fc-bad0-4fcb-bf4b-37cbc50846ee">WM_CREATE</a>
 

 

