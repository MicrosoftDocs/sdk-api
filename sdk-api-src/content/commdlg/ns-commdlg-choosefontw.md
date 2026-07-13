---
UID: NS:commdlg.tagCHOOSEFONTW
title: CHOOSEFONTW (commdlg.h)
description: Contains information that the ChooseFont function uses to initialize the Font dialog box. After the user closes the dialog box, the system returns information about the user's selection in this structure. (Unicode)
helpviewer_keywords: ["*LPCHOOSEFONTW","BOLD_FONTTYPE","CF_ANSIONLY","CF_APPLY","CF_BOTH","CF_EFFECTS","CF_ENABLEHOOK","CF_ENABLETEMPLATE","CF_ENABLETEMPLATEHANDLE","CF_FIXEDPITCHONLY","CF_FORCEFONTEXIST","CF_INACTIVEFONTS","CF_INITTOLOGFONTSTRUCT","CF_LIMITSIZE","CF_NOFACESEL","CF_NOOEMFONTS","CF_NOSCRIPTSEL","CF_NOSIMULATIONS","CF_NOSIZESEL","CF_NOSTYLESEL","CF_NOVECTORFONTS","CF_NOVERTFONTS","CF_PRINTERFONTS","CF_SCALABLEONLY","CF_SCREENFONTS","CF_SCRIPTSONLY","CF_SELECTSCRIPT","CF_SHOWHELP","CF_TTONLY","CF_USESTYLE","CF_WYSIWYG","CHOOSEFONT","CHOOSEFONT structure [Dialog Boxes]","CHOOSEFONTA","CHOOSEFONTW","ITALIC_FONTTYPE","LPCHOOSEFONT","LPCHOOSEFONT structure pointer [Dialog Boxes]","PRINTER_FONTTYPE","REGULAR_FONTTYPE","SCREEN_FONTTYPE","SIMULATED_FONTTYPE","_win32_CHOOSEFONT_str","_win32_choosefont_str_cpp","commdlg/CHOOSEFONT","commdlg/CHOOSEFONTA","commdlg/CHOOSEFONTW","commdlg/LPCHOOSEFONT","dlgbox.choosefont_str","tagCHOOSEFONTA","tagCHOOSEFONTW","winui._win32_choosefont_str"]
old-location: dlgbox\choosefont_str.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxstructures\choosefont.htm
ms.date: 12/05/2018
ms.keywords: '*LPCHOOSEFONTW, BOLD_FONTTYPE, CF_ANSIONLY, CF_APPLY, CF_BOTH, CF_EFFECTS, CF_ENABLEHOOK, CF_ENABLETEMPLATE, CF_ENABLETEMPLATEHANDLE, CF_FIXEDPITCHONLY, CF_FORCEFONTEXIST, CF_INACTIVEFONTS, CF_INITTOLOGFONTSTRUCT, CF_LIMITSIZE, CF_NOFACESEL, CF_NOOEMFONTS, CF_NOSCRIPTSEL, CF_NOSIMULATIONS, CF_NOSIZESEL, CF_NOSTYLESEL, CF_NOVECTORFONTS, CF_NOVERTFONTS, CF_PRINTERFONTS, CF_SCALABLEONLY, CF_SCREENFONTS, CF_SCRIPTSONLY, CF_SELECTSCRIPT, CF_SHOWHELP, CF_TTONLY, CF_USESTYLE, CF_WYSIWYG, CHOOSEFONT, CHOOSEFONT structure [Dialog Boxes], CHOOSEFONTA, CHOOSEFONTW, ITALIC_FONTTYPE, LPCHOOSEFONT, LPCHOOSEFONT structure pointer [Dialog Boxes], PRINTER_FONTTYPE, REGULAR_FONTTYPE, SCREEN_FONTTYPE, SIMULATED_FONTTYPE, _win32_CHOOSEFONT_str, _win32_choosefont_str_cpp, commdlg/CHOOSEFONT, commdlg/CHOOSEFONTA, commdlg/CHOOSEFONTW, commdlg/LPCHOOSEFONT, dlgbox.choosefont_str, tagCHOOSEFONTA, tagCHOOSEFONTW, winui._win32_choosefont_str'
req.header: commdlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CHOOSEFONTW (Unicode) and CHOOSEFONTA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CHOOSEFONTW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCHOOSEFONTW
 - commdlg/tagCHOOSEFONTW
 - CHOOSEFONTW
 - commdlg/CHOOSEFONTW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commdlg.h
api_name:
 - CHOOSEFONT
 - CHOOSEFONTA
 - CHOOSEFONTW
---

# CHOOSEFONTW structure

## -description

Contains information that the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)">ChooseFont</a> function uses to initialize the <b>Font</b> dialog box. After the user closes the dialog box, the system returns information about the user's selection in this structure.

## -struct-fields

### -field lStructSize

Type: <b>DWORD</b>

The length of the structure, in bytes.

### -field hwndOwner

Type: <b>HWND</b>

A handle to the window that owns the dialog box. This member can be any valid window handle, or it can be <b>NULL</b> if the dialog box has no owner.

### -field hDC

Type: <b>HDC</b>

This member is ignored by the <a href="/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)">ChooseFont</a> function.

<b>Windows Vista and Windows XP/2000:  </b>A handle to the device context or information context of the printer whose fonts will be listed in the dialog box. This member is used only if the <b>Flags</b> member specifies the <b>CF_PRINTERFONTS</b> or <b>CF_BOTH</b> flag; otherwise, this member is ignored.

### -field lpLogFont

Type: <b>LPLOGFONT</b>

A pointer to a  <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure. If you set the <b>CF_INITTOLOGFONTSTRUCT</b> flag in the <b>Flags</b> member and initialize the other members, the <a href="/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)">ChooseFont</a> function initializes the dialog box with a font that matches the <b>LOGFONT</b> members. If the user clicks the <b>OK</b> button, <b>ChooseFont</b> sets the members of the <b>LOGFONT</b> structure based on the user's selections.

### -field iPointSize

Type: <b>INT</b>

The size of the selected font, in units of 1/10 of a point. The <a href="/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)">ChooseFont</a> function sets this value after the user closes the dialog box.

### -field Flags

Type: <b>DWORD</b>

A set of bit flags that you can use to initialize the <b>Font</b> dialog box. When the dialog box returns, it sets these flags to indicate the user input. This member can be one or more of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CF_APPLY"></a><a id="cf_apply"></a><dl>
<dt><b>CF_APPLY</b></dt>
<dt>0x00000200L</dt>
</dl>
</td>
<td width="60%">
Causes the dialog box to display the <b>Apply</b> button. You should provide a hook procedure to process <a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a> messages for the <b>Apply</b> button. The hook procedure can send the <a href="/windows/desktop/dlgbox/wm-choosefont-getlogfont">WM_CHOOSEFONT_GETLOGFONT</a> message to the dialog box to retrieve the address of the  structure that contains the current selections for the font. 

</td>
</tr>
<tr>
<td width="40%"><a id="CF_ANSIONLY"></a><a id="cf_ansionly"></a><dl>
<dt><b>CF_ANSIONLY</b></dt>
<dt>0x00000400L</dt>
</dl>
</td>
<td width="60%">
This flag is obsolete. To limit font selections to all scripts except those that use the OEM or Symbol character sets, use <b>CF_SCRIPTSONLY</b>. To get the original <b>CF_ANSIONLY</b> behavior, use <b>CF_SELECTSCRIPT</b> and specify <b>ANSI_CHARSET</b> in the <b>lfCharSet</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure pointed to by <b>lpLogFont</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CF_BOTH"></a><a id="cf_both"></a><dl>
<dt><b>CF_BOTH</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
This flag is ignored for font enumeration.

<b>Windows Vista and Windows XP/2000:  </b>Causes the dialog box to list the available printer and screen fonts. The <b>hDC</b> member is a handle to the device context or information context associated with the printer. This flag is a combination of the <b>CF_SCREENFONTS</b> and <b>CF_PRINTERFONTS</b> flags.

</td>
</tr>
<tr>
<td width="40%"><a id="CF_EFFECTS"></a><a id="cf_effects"></a><dl>
<dt><b>CF_EFFECTS</b></dt>
<dt>0x00000100L</dt>
</dl>
</td>
<td width="60%">
Causes the dialog box to display the controls that allow the user to specify strikeout, underline, and text color options. If this flag is set, you can use the <b>rgbColors</b> member to specify the initial text color. You can use the <b>lfStrikeOut</b> and <b>lfUnderline</b> members of the  structure pointed to by <b>lpLogFont</b> to specify the initial settings of the strikeout and underline check boxes. <a href="/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)">ChooseFont</a> can use these members to return the user's selections.

</td>
</tr>
<tr>
<td width="40%"><a id="CF_ENABLEHOOK"></a><a id="cf_enablehook"></a><dl>
<dt><b>CF_ENABLEHOOK</b></dt>
<dt>0x00000008L</dt>
</dl>
</td>
<td width="60%">
Enables the hook procedure specified in the <b>lpfnHook</b> member of this structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CF_ENABLETEMPLATE"></a><a id="cf_enabletemplate"></a><dl>
<dt><b>CF_ENABLETEMPLATE</b></dt>
<dt>0x00000010L</dt>
</dl>
</td>
<td width="60%">
Indicates that the <b>hInstance</b> and <b>lpTemplateName</b> members specify a dialog box template to use in place of the default template.

</td>
</tr>
<tr>
<td width="40%"><a id="CF_ENABLETEMPLATEHANDLE"></a><a id="cf_enabletemplatehandle"></a><dl>
<dt><b>CF_ENABLETEMPLATEHANDLE</b></dt>
<dt>0x00000020L</dt>
</dl>
</td>
<td width="60%">
Indicates that the <b>hInstance</b> member identifies a data block that contains a preloaded dialog box template. The system ignores the <b>lpTemplateName</b> member if this flag is specified.

</td>
</tr>
<tr>
<td width="40%"><a id="CF_FIXEDPITCHONLY"></a><a id="cf_fixedpitchonly"></a><dl>
<dt><b>CF_FIXEDPITCHONLY</b></dt>
<dt>0x00004000L</dt>
</dl>
</td>
<td width="60%">

<a href="/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)">ChooseFont</a> should enumerate and allow selection of only fixed-pitch fonts.

</td>
</tr>
<tr>
<td width="40%"><a id="CF_FORCEFONTEXIST"></a><a id="cf_forcefontexist"></a><dl>
<dt><b>CF_FORCEFONTEXIST</b></dt>
<dt>0x00010000L</dt>
</dl>
</td>
<td width="60%">

<a href="/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)">ChooseFont</a> should indicate an error condition if the user attempts to select a font or style that is not listed in the dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="CF_INACTIVEFONTS"></a><a id="cf_inactivefonts"></a><dl>
<dt><b>CF_INACTIVEFONTS</b></dt>
<dt>0x02000000L</dt>
</dl>
</td>
<td width="60%">

<a href="/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)">ChooseFont</a> should additionally display fonts that are set to Hide in Fonts Control Panel.

<b>Windows Vista and Windows XP/2000:  </b>This flag is not supported until Windows 7.

</td>
</tr>
<tr>
<td width="40%"><a id="CF_INITTOLOGFONTSTRUCT"></a><a id="cf_inittologfontstruct"></a><dl>
<dt><b>CF_INITTOLOGFONTSTRUCT</b></dt>
<dt>0x00000040L</dt>
</dl>
</td>
<td width="60%">

<a href="/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)">ChooseFont</a> should use the  structure pointed to by the <b>lpLogFont</b> member to initialize the dialog box controls.

</td>
</tr>
<tr>
<td width="40%"><a id="CF_LIMITSIZE"></a><a id="cf_limitsize"></a><dl>
<dt><b>CF_LIMITSIZE</b></dt>
<dt>0x00002000L</dt>
</dl>
</td>
<td width="60%">

<a href="/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)">ChooseFont</a> should select only font sizes within the range specified by the <b>nSizeMin</b> and <b>nSizeMax</b> members.

</td>
</tr>
<tr>
<td width="40%"><a id="CF_NOOEMFONTS"></a><a id="cf_nooemfonts"></a><dl>
<dt><b>CF_NOOEMFONTS</b></dt>
<dt>0x00000800L</dt>
</dl>
</td>
<td width="60%">
Same as the <b>CF_NOVECTORFONTS</b> flag.

</td>
</tr>
<tr>
<td width="40%"><a id="CF_NOFACESEL"></a><a id="cf_nofacesel"></a><dl>
<dt><b>CF_NOFACESEL</b></dt>
<dt>0x00080000L</dt>
</dl>
</td>
<td width="60%">
When using a <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure to initialize the dialog box controls, use this flag to prevent the dialog box from displaying an initial selection for the font name combo box. This is useful when there is no single font name that applies to the text selection. 

</td>
</tr>
<tr>
<td width="40%"><a id="CF_NOSCRIPTSEL"></a><a id="cf_noscriptsel"></a><dl>
<dt><b>CF_NOSCRIPTSEL</b></dt>
<dt>0x00800000L</dt>
</dl>
</td>
<td width="60%">
Disables the <b>Script</b> combo box. When this flag is set, the <b>lfCharSet</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure is set to <b>DEFAULT_CHARSET</b> when <a href="/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)">ChooseFont</a> returns. This flag is used only to initialize the dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="CF_NOSIMULATIONS"></a><a id="cf_nosimulations"></a><dl>
<dt><b>CF_NOSIMULATIONS</b></dt>
<dt>0x00001000L</dt>
</dl>
</td>
<td width="60%">

<a href="/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)">ChooseFont</a> should not display or allow selection of font simulations.

</td>
</tr>
<tr>
<td width="40%"><a id="CF_NOSIZESEL"></a><a id="cf_nosizesel"></a><dl>
<dt><b>CF_NOSIZESEL</b></dt>
<dt>0x00200000L</dt>
</dl>
</td>
<td width="60%">
When using a  structure to initialize the dialog box controls, use this flag to prevent the dialog box from displaying an initial selection for the <b>Font Size</b> combo box. This is useful when there is no single font size that applies to the text selection. 

</td>
</tr>
<tr>
<td width="40%"><a id="CF_NOSTYLESEL"></a><a id="cf_nostylesel"></a><dl>
<dt><b>CF_NOSTYLESEL</b></dt>
<dt>0x00100000L</dt>
</dl>
</td>
<td width="60%">
When using a <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure to initialize the dialog box controls, use this flag to prevent the dialog box from displaying an initial selection for the <b>Font Style</b> combo box. This is useful when there is no single font style that applies to the text selection. 

</td>
</tr>
<tr>
<td width="40%"><a id="CF_NOVECTORFONTS"></a><a id="cf_novectorfonts"></a><dl>
<dt><b>CF_NOVECTORFONTS</b></dt>
<dt>0x00000800L</dt>
</dl>
</td>
<td width="60%">

<a href="/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)">ChooseFont</a> should not allow vector font selections.

</td>
</tr>
<tr>
<td width="40%"><a id="CF_NOVERTFONTS"></a><a id="cf_novertfonts"></a><dl>
<dt><b>CF_NOVERTFONTS</b></dt>
<dt>0x01000000L</dt>
</dl>
</td>
<td width="60%">
Causes the <b>Font</b> dialog box to list only horizontally oriented fonts.

</td>
</tr>
<tr>
<td width="40%"><a id="CF_PRINTERFONTS"></a><a id="cf_printerfonts"></a><dl>
<dt><b>CF_PRINTERFONTS</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
This flag is ignored for font enumeration.

<b>Windows Vista and Windows XP/2000:  </b>Causes the dialog box to list only the fonts supported by the printer associated with the device context or information context identified by the <b>hDC</b> member. It also causes the font type description label to appear at the bottom of the <b>Font</b> dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="CF_SCALABLEONLY"></a><a id="cf_scalableonly"></a><dl>
<dt><b>CF_SCALABLEONLY</b></dt>
<dt>0x00020000L</dt>
</dl>
</td>
<td width="60%">
Specifies that <a href="/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)">ChooseFont</a> should allow only the selection of scalable fonts. Scalable fonts include vector fonts, scalable printer fonts, TrueType fonts, and fonts scaled by other technologies.

</td>
</tr>
<tr>
<td width="40%"><a id="CF_SCREENFONTS"></a><a id="cf_screenfonts"></a><dl>
<dt><b>CF_SCREENFONTS</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
This flag is ignored for font enumeration.

<b>Windows Vista and Windows XP/2000:  </b>Causes the dialog box to list only the screen fonts supported by the system.

</td>
</tr>
<tr>
<td width="40%"><a id="CF_SCRIPTSONLY"></a><a id="cf_scriptsonly"></a><dl>
<dt><b>CF_SCRIPTSONLY</b></dt>
<dt>0x00000400L</dt>
</dl>
</td>
<td width="60%">

<a href="/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)">ChooseFont</a> should allow selection of fonts for all non-OEM and Symbol character sets, as well as the ANSI character set. This supersedes the <b>CF_ANSIONLY</b> value.

</td>
</tr>
<tr>
<td width="40%"><a id="CF_SELECTSCRIPT"></a><a id="cf_selectscript"></a><dl>
<dt><b>CF_SELECTSCRIPT</b></dt>
<dt>0x00400000L</dt>
</dl>
</td>
<td width="60%">
When specified on input, only fonts with the character set identified in the <b>lfCharSet</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure are displayed. The user will not be allowed to change the character set specified in the <b>Scripts</b> combo box.

</td>
</tr>
<tr>
<td width="40%"><a id="CF_SHOWHELP"></a><a id="cf_showhelp"></a><dl>
<dt><b>CF_SHOWHELP</b></dt>
<dt>0x00000004L</dt>
</dl>
</td>
<td width="60%">
Causes the dialog box to display the <b>Help</b> button. The <b>hwndOwner</b> member must specify the window to receive the <a href="/windows/desktop/dlgbox/helpmsgstring">HELPMSGSTRING</a> registered messages that the dialog box sends when the user clicks the <b>Help</b> button.

</td>
</tr>
<tr>
<td width="40%"><a id="CF_TTONLY"></a><a id="cf_ttonly"></a><dl>
<dt><b>CF_TTONLY</b></dt>
<dt>0x00040000L</dt>
</dl>
</td>
<td width="60%">

<a href="/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)">ChooseFont</a> should only enumerate and allow the selection of TrueType fonts.

</td>
</tr>
<tr>
<td width="40%"><a id="CF_USESTYLE"></a><a id="cf_usestyle"></a><dl>
<dt><b>CF_USESTYLE</b></dt>
<dt>0x00000080L</dt>
</dl>
</td>
<td width="60%">
The <b>lpszStyle</b> member is a pointer to a buffer that contains style data that <a href="/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)">ChooseFont</a> should use to initialize the <b>Font Style</b> combo box. When the user closes the dialog box, <b>ChooseFont</b> copies style data for the user's selection to this buffer.

<div class="alert"><b>Note</b>  To globalize your application, you should specify the style by using the <b>lfWeight</b> and <b>lfItalic</b> members of the <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure pointed to by <b>lpLogFont</b>. The style name may change depending on the system user interface language.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="CF_WYSIWYG"></a><a id="cf_wysiwyg"></a><dl>
<dt><b>CF_WYSIWYG</b></dt>
<dt>0x00008000L</dt>
</dl>
</td>
<td width="60%">
 Obsolete. <a href="/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)">ChooseFont</a> ignores this flag.

<b>Windows Vista and Windows XP/2000:  </b><a href="/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)">ChooseFont</a> should allow only the selection of fonts available on both the printer and the display. If this flag is specified, the <b>CF_SCREENSHOTS</b> and <b>CF_PRINTERFONTS</b>, or <b>CF_BOTH</b> flags should also be specified.

</td>
</tr>
</table>

### -field rgbColors

Type: <b><a href="/windows/desktop/gdi/colorref">COLORREF</a></b>

If the <b>CF_EFFECTS</b> flag is set, <b>rgbColors</b> specifies the initial text color. When <a href="/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)">ChooseFont</a> returns successfully, this member contains the RGB value of the text color that the user selected. To create a <a href="/windows/desktop/gdi/colorref">COLORREF</a> color value, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a> macro.

### -field lCustData

Type: <b>LPARAM</b>

Application-defined data that the system passes to the hook procedure identified by the <b>lpfnHook</b> member. When the system sends the <a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a> message to the hook procedure, the message's <i>lParam</i> parameter is a pointer to the <a href="/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)">CHOOSEFONT</a> structure specified when the dialog was created. The hook procedure can use this pointer to get the <b>lCustData</b> value.

### -field lpfnHook

Type: <b>LPCFHOOKPROC</b>

A pointer to a <a href="/windows/desktop/api/commdlg/nc-commdlg-lpcfhookproc">CFHookProc</a> hook procedure that can process messages intended for the dialog box. This member is ignored unless the <b>CF_ENABLEHOOK</b> flag is set in the <b>Flags</b> member.

### -field lpTemplateName

Type: <b>LPCTSTR</b>

The name of the dialog box template resource in the module identified by the <b>hInstance</b> member. This template is substituted for the standard dialog box template. For numbered dialog box resources, <b>lpTemplateName</b> can be a value returned by the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro. This member is ignored unless the <b>CF_ENABLETEMPLATE</b> flag is set in the <b>Flags</b> member.

### -field hInstance

Type: <b>HINSTANCE</b>

If the <b>CF_ENABLETEMPLATEHANDLE</b> flag is set in the <b>Flags</b> member, <b>hInstance</b> is a handle to a memory object containing a dialog box template. If the <b>CF_ENABLETEMPLATE</b> flag is set, <b>hInstance</b> is a handle to a module that contains a dialog box template named by the <b>lpTemplateName</b> member. If neither <b>CF_ENABLETEMPLATEHANDLE</b> nor <b>CF_ENABLETEMPLATE</b> is set, this member is ignored.

### -field lpszStyle

Type: <b>LPTSTR</b>

The style data. If the <b>CF_USESTYLE</b> flag is specified, <a href="/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)">ChooseFont</a> uses the data in this buffer to initialize the <b>Font Style</b> combo box. When the user closes the dialog box, <b>ChooseFont</b> copies the string in the <b>Font Style</b> combo box into this buffer.

### -field nFontType

Type: <b>WORD</b>

The type of the selected font when <a href="/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)">ChooseFont</a> returns. This member can be one or more of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BOLD_FONTTYPE"></a><a id="bold_fonttype"></a><dl>
<dt><b>BOLD_FONTTYPE</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
The font weight is bold. This information is duplicated in the <b>lfWeight</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure and is equivalent to <b>FW_BOLD</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="ITALIC_FONTTYPE"></a><a id="italic_fonttype"></a><dl>
<dt><b>ITALIC_FONTTYPE</b></dt>
<dt>0x0200</dt>
</dl>
</td>
<td width="60%">
The italic font attribute is set. This information is duplicated in the <b>lfItalic</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_FONTTYPE"></a><a id="printer_fonttype"></a><dl>
<dt><b>PRINTER_FONTTYPE</b></dt>
<dt>0x4000</dt>
</dl>
</td>
<td width="60%">
The font is a printer font.

</td>
</tr>
<tr>
<td width="40%"><a id="REGULAR_FONTTYPE"></a><a id="regular_fonttype"></a><dl>
<dt><b>REGULAR_FONTTYPE</b></dt>
<dt>0x0400</dt>
</dl>
</td>
<td width="60%">
The font weight is normal. This information is duplicated in the <b>lfWeight</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure and is equivalent to <b>FW_REGULAR</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="SCREEN_FONTTYPE"></a><a id="screen_fonttype"></a><dl>
<dt><b>SCREEN_FONTTYPE</b></dt>
<dt>0x2000</dt>
</dl>
</td>
<td width="60%">
The font is a screen font.

</td>
</tr>
<tr>
<td width="40%"><a id="SIMULATED_FONTTYPE"></a><a id="simulated_fonttype"></a><dl>
<dt><b>SIMULATED_FONTTYPE</b></dt>
<dt>0x8000</dt>
</dl>
</td>
<td width="60%">
The font is simulated by the graphics device interface (GDI).

</td>
</tr>
</table>

### -field nSizeMin

Type: <b>INT</b>

The minimum point size a user can select. <a href="/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)">ChooseFont</a> recognizes this member only if the <b>CF_LIMITSIZE</b> flag is specified.

### -field nSizeMax

Type: <b>INT</b>

The maximum point size a user can select. <a href="/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)">ChooseFont</a> recognizes this member only if the <b>CF_LIMITSIZE</b> flag is specified.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)">ChooseFont</a>



<a href="/windows/desktop/dlgbox/common-dialog-box-library">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a>



<b>Reference</b>

## -remarks

> [!NOTE]
> The commdlg.h header defines CHOOSEFONT as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
