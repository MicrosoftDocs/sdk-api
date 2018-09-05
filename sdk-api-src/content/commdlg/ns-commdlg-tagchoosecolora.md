---
UID: NS:commdlg.tagCHOOSECOLORA
title: tagCHOOSECOLORA
author: windows-sdk-content
description: Contains information the ChooseColor function uses to initialize the Color dialog box. After the user closes the dialog box, the system returns information about the user's selection in this structure.
old-location: dlgbox\choosecolor_str.htm
old-project: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxstructures\choosecolor.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: "*LPCHOOSECOLORA, CC_ANYCOLOR, CC_ENABLEHOOK, CC_ENABLETEMPLATE, CC_ENABLETEMPLATEHANDLE, CC_FULLOPEN, CC_PREVENTFULLOPEN, CC_RGBINIT, CC_SHOWHELP, CC_SOLIDCOLOR, CHOOSECOLOR, CHOOSECOLOR structure [Dialog Boxes], CHOOSECOLORA, CHOOSECOLORW, LPCHOOSECOLOR, LPCHOOSECOLOR structure pointer [Dialog Boxes], _win32_CHOOSECOLOR_str, _win32_choosecolor_str_cpp, commdlg/CHOOSECOLOR, commdlg/CHOOSECOLORA, commdlg/CHOOSECOLORW, commdlg/LPCHOOSECOLOR, dlgbox.choosecolor_str, tagCHOOSECOLORA, tagCHOOSECOLORW, winui._win32_choosecolor_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: commdlg.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CHOOSECOLORW (Unicode) and CHOOSECOLORA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CHOOSECOLORA, *LPCHOOSECOLORA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commdlg.h
api_name:
 - CHOOSECOLOR
 - CHOOSECOLORA
 - CHOOSECOLORW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagCHOOSECOLORA structure


## -description


Contains information the <a href="https://msdn.microsoft.com/cb4f59e8-bbf0-406e-9103-1a08c3731da6">ChooseColor</a> function uses to initialize the <b>Color</b> dialog box. After the user closes the dialog box, the system returns information about the user's selection in this structure. 


## -struct-fields




### -field lStructSize

Type: <b>DWORD</b>

The length, in bytes, of the structure. 


### -field hwndOwner

Type: <b>HWND</b>

A handle to the window that owns the dialog box. This member can be any valid window handle, or it can be <b>NULL</b> if the dialog box has no owner. 


### -field hInstance

Type: <b>HWND</b>

If the <b>CC_ENABLETEMPLATEHANDLE</b> flag is set in the <b>Flags</b> member, <b>hInstance</b> is a handle to a memory object containing a dialog box template. If the <b>CC_ENABLETEMPLATE</b> flag is set, <b>hInstance</b> is a handle to a module that contains a dialog box template named by the <b>lpTemplateName</b> member. If neither <b>CC_ENABLETEMPLATEHANDLE</b> nor <b>CC_ENABLETEMPLATE</b> is set, this member is ignored. 


### -field rgbResult

Type: <b><a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a></b>

If the <b>CC_RGBINIT</b> flag is set, <b>rgbResult</b> specifies the color initially selected when the dialog box is created. If the specified color value is not among the available colors, the system selects the nearest solid color available. If <b>rgbResult</b> is zero or <b>CC_RGBINIT</b> is not set, the initially selected color is black. If the user clicks the <b>OK</b> button, <b>rgbResult</b> specifies the user's color selection. To create a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> color value, use the <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a> macro. 


### -field lpCustColors

Type: <b><a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>*</b>

A pointer to an array of 16  values that contain red, green, blue (RGB) values for the custom color boxes in the dialog box. If the user modifies these colors, the system updates the array with the new RGB values. To preserve new custom colors between calls to the <a href="https://msdn.microsoft.com/cb4f59e8-bbf0-406e-9103-1a08c3731da6">ChooseColor</a> function, you should allocate static memory for the array. To create a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> color value, use the <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a> macro. 


### -field Flags

Type: <b>DWORD</b>

A set of bit flags that you can use to initialize the <b>Color</b> dialog box. When the dialog box returns, it sets these flags to indicate the user's input. This member can be a combination of the following flags. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CC_ANYCOLOR"></a><a id="cc_anycolor"></a><dl>
<dt><b>CC_ANYCOLOR</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Causes the dialog box to display all available colors in the set of basic colors. 

</td>
</tr>
<tr>
<td width="40%"><a id="CC_ENABLEHOOK"></a><a id="cc_enablehook"></a><dl>
<dt><b>CC_ENABLEHOOK</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Enables the hook procedure specified in the <b>lpfnHook</b> member of this structure. This flag is used only to initialize the dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="CC_ENABLETEMPLATE"></a><a id="cc_enabletemplate"></a><dl>
<dt><b>CC_ENABLETEMPLATE</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
The <b>hInstance</b> and <b>lpTemplateName</b> members specify a dialog box template to use in place of the default template. This flag is used only to initialize the dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="CC_ENABLETEMPLATEHANDLE"></a><a id="cc_enabletemplatehandle"></a><dl>
<dt><b>CC_ENABLETEMPLATEHANDLE</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
The <b>hInstance</b> member identifies a data block that contains a preloaded dialog box template. The system ignores the <b>lpTemplateName</b> member if this flag is specified. This flag is used only to initialize the dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="CC_FULLOPEN"></a><a id="cc_fullopen"></a><dl>
<dt><b>CC_FULLOPEN</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Causes the dialog box to display the additional controls that allow the user to create custom colors. If this flag is not set, the user must click the <b>Define Custom Color</b> button to display the custom color controls.

</td>
</tr>
<tr>
<td width="40%"><a id="CC_PREVENTFULLOPEN"></a><a id="cc_preventfullopen"></a><dl>
<dt><b>CC_PREVENTFULLOPEN</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Disables the <b>Define Custom Color</b> button.

</td>
</tr>
<tr>
<td width="40%"><a id="CC_RGBINIT"></a><a id="cc_rgbinit"></a><dl>
<dt><b>CC_RGBINIT</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Causes the dialog box to use the color specified in the <b>rgbResult</b> member as the initial color selection.

</td>
</tr>
<tr>
<td width="40%"><a id="CC_SHOWHELP"></a><a id="cc_showhelp"></a><dl>
<dt><b>CC_SHOWHELP</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Causes the dialog box to display the Help button. The <b>hwndOwner</b> member must specify the window to receive the <a href="https://msdn.microsoft.com/21c0fcf5-785b-4005-8133-e48347f991a8">HELPMSGSTRING</a> registered messages that the dialog box sends when the user clicks the <b>Help</b> button.

</td>
</tr>
<tr>
<td width="40%"><a id="CC_SOLIDCOLOR"></a><a id="cc_solidcolor"></a><dl>
<dt><b>CC_SOLIDCOLOR</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Causes the dialog box to display only solid colors in the set of basic colors. 

</td>
</tr>
</table>
 


### -field lCustData

Type: <b>LPARAM</b>

Application-defined data that the system passes to the hook procedure identified by the <b>lpfnHook</b> member. When the system sends the <a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a> message to the hook procedure, the message's <i>lParam</i> parameter is a pointer to the <b>CHOOSECOLOR</b> structure specified when the dialog was created. The hook procedure can use this pointer to get the <b>lCustData</b> value. 


### -field lpfnHook

Type: <b>LPCCHOOKPROC</b>

A pointer to a <a href="https://msdn.microsoft.com/4486ad29-fe1e-4e7f-951f-d137c6497591">CCHookProc</a> hook procedure that can process messages intended for the dialog box. This member is ignored unless the <b>CC_ENABLEHOOK</b> flag is set in the <b>Flags</b> member. 


### -field lpTemplateName

Type: <b>LPCTSTR</b>

The name of the dialog box template resource in the module identified by the <b>hInstance</b> member. This template is substituted for the standard dialog box template. For numbered dialog box resources, <b>lpTemplateName</b> can be a value returned by the <a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a> macro. This member is ignored unless the <b>CC_ENABLETEMPLATE</b> flag is set in the <b>Flags</b> member. 


## -see-also




<a href="https://msdn.microsoft.com/4486ad29-fe1e-4e7f-951f-d137c6497591">CCHookProc</a>



<a href="https://msdn.microsoft.com/cb4f59e8-bbf0-406e-9103-1a08c3731da6">ChooseColor</a>



<a href="https://msdn.microsoft.com/28573019-f0bd-4a8e-a1a1-48559f658a81">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a>



<b>Reference</b>
 

 

