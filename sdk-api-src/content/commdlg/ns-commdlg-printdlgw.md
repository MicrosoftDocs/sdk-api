---
UID: NS:commdlg.tagPDW
title: PRINTDLGW (commdlg.h)
description: Contains information that the PrintDlg function uses to initialize the Print Dialog Box. After the user closes the dialog box, the system uses this structure to return information about the user's selections. (Unicode)
helpviewer_keywords: ["*LPPRINTDLGW","LPPRINTDLG","LPPRINTDLG structure pointer [Dialog Boxes]","PD_ALLPAGES","PD_COLLATE","PD_DISABLEPRINTTOFILE","PD_ENABLEPRINTHOOK","PD_ENABLEPRINTTEMPLATE","PD_ENABLEPRINTTEMPLATEHANDLE","PD_ENABLESETUPHOOK","PD_ENABLESETUPTEMPLATE","PD_ENABLESETUPTEMPLATEHANDLE","PD_HIDEPRINTTOFILE","PD_NONETWORKBUTTON","PD_NOPAGENUMS","PD_NOSELECTION","PD_NOWARNING","PD_PAGENUMS","PD_PRINTSETUP","PD_PRINTTOFILE","PD_RETURNDC","PD_RETURNDEFAULT","PD_RETURNIC","PD_SELECTION","PD_SHOWHELP","PD_USEDEVMODECOPIES","PD_USEDEVMODECOPIESANDCOLLATE","PRINTDLG","PRINTDLG structure [Dialog Boxes]","PRINTDLGA","PRINTDLGW","_win32_PRINTDLG_str","_win32_printdlg_str_cpp","commdlg/LPPRINTDLG","commdlg/PRINTDLG","commdlg/PRINTDLGA","commdlg/PRINTDLGW","dlgbox.printdlg_str","tagPDA","tagPDW","winui._win32_printdlg_str"]
old-location: dlgbox\printdlg_str.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxstructures\printdlg.htm
ms.date: 12/05/2018
ms.keywords: '*LPPRINTDLGW, LPPRINTDLG, LPPRINTDLG structure pointer [Dialog Boxes], PD_ALLPAGES, PD_COLLATE, PD_DISABLEPRINTTOFILE, PD_ENABLEPRINTHOOK, PD_ENABLEPRINTTEMPLATE, PD_ENABLEPRINTTEMPLATEHANDLE, PD_ENABLESETUPHOOK, PD_ENABLESETUPTEMPLATE, PD_ENABLESETUPTEMPLATEHANDLE, PD_HIDEPRINTTOFILE, PD_NONETWORKBUTTON, PD_NOPAGENUMS, PD_NOSELECTION, PD_NOWARNING, PD_PAGENUMS, PD_PRINTSETUP, PD_PRINTTOFILE, PD_RETURNDC, PD_RETURNDEFAULT, PD_RETURNIC, PD_SELECTION, PD_SHOWHELP, PD_USEDEVMODECOPIES, PD_USEDEVMODECOPIESANDCOLLATE, PRINTDLG, PRINTDLG structure [Dialog Boxes], PRINTDLGA, PRINTDLGW, _win32_PRINTDLG_str, _win32_printdlg_str_cpp, commdlg/LPPRINTDLG, commdlg/PRINTDLG, commdlg/PRINTDLGA, commdlg/PRINTDLGW, dlgbox.printdlg_str, tagPDA, tagPDW, winui._win32_printdlg_str'
req.header: commdlg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PRINTDLGW (Unicode) and PRINTDLGA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PRINTDLGW, *LPPRINTDLGW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPDW
 - commdlg/tagPDW
 - LPPRINTDLGW
 - commdlg/LPPRINTDLGW
 - PRINTDLGW
 - commdlg/PRINTDLGW
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
 - PRINTDLG
 - PRINTDLGA
 - PRINTDLGW
---

# PRINTDLGW structure


## -description

Contains information that the <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> function uses to initialize the <a href="/windows/desktop/dlgbox/print-dialog-box">Print Dialog Box</a>. After the user closes the dialog box, the system uses this structure to return information about the user's selections.

## -struct-fields

### -field lStructSize

Type: <b>DWORD</b>

The structure size, in bytes.

### -field hwndOwner

Type: <b>HWND</b>

A handle to the window that owns the dialog box. This member can be any valid window handle, or it can be <b>NULL</b> if the dialog box has no owner.

### -field hDevMode

Type: <b>HGLOBAL</b>

A handle to a movable global memory object that contains a <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure. If <b>hDevMode</b> is not <b>NULL</b> on input, you must allocate a movable block of memory for the <b>DEVMODE</b> structure and initialize its members. The <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> function uses the input data to initialize the controls in the dialog box. When <b>PrintDlg</b> returns, the <b>DEVMODE</b> members indicate the user's input. 

If <b>hDevMode</b> is <b>NULL</b> on input, <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> allocates memory for the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure, initializes its members to indicate the user's input, and returns a handle that identifies it.

If the device driver for the specified printer does not support extended device modes, <b>hDevMode</b> is <b>NULL</b> when <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> returns.

If the device name (specified by the <b>dmDeviceName</b> member of the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure) does not appear in the [devices] section of WIN.INI, <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> returns an error. 

For more information about the <b>hDevMode</b> and <b>hDevNames</b> members, see the Remarks section at the end of this topic.

### -field hDevNames

Type: <b>HGLOBAL</b>

A handle to a movable global memory object that contains a <a href="/windows/desktop/api/commdlg/ns-commdlg-devnames">DEVNAMES</a> structure. If <b>hDevNames</b> is not <b>NULL</b> on input, you must allocate a movable block of memory for the <b>DEVNAMES</b> structure and initialize its members. The <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> function uses the input data to initialize the controls in the dialog box. When <b>PrintDlg</b> returns, the <b>DEVNAMES</b> members contain information for the printer chosen by the user. You can use this information to create a device context or an information context. 

The <b>hDevNames</b> member can be <b>NULL</b>, in which case, <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> allocates memory for the <a href="/windows/desktop/api/commdlg/ns-commdlg-devnames">DEVNAMES</a> structure, initializes its members to indicate the user's input, and returns a handle that identifies it. 

For more information about the <b>hDevMode</b> and <b>hDevNames</b> members, see the Remarks section at the end of this topic.

### -field hDC

Type: <b>HDC</b>

A handle to a device context or an information context, depending on whether the <b>Flags</b> member specifies the <b>PD_RETURNDC</b> or <b>PC_RETURNIC</b> flag. If neither flag is specified, the value of this member is undefined. If both flags are specified, <b>PD_RETURNDC</b> has priority.

### -field Flags

Type: <b>DWORD</b>

Initializes the <b>Print</b> dialog box. When the dialog box returns, it sets these flags to indicate the user's input. This member can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PD_ALLPAGES"></a><a id="pd_allpages"></a><dl>
<dt><b>PD_ALLPAGES</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
The default flag that indicates that the 
						<b>All</b> radio button is initially selected. This flag is used as a placeholder to indicate that the <b>PD_PAGENUMS</b> and <b>PD_SELECTION</b> flags are not specified. 

</td>
</tr>
<tr>
<td width="40%"><a id="PD_COLLATE"></a><a id="pd_collate"></a><dl>
<dt><b>PD_COLLATE</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the <b>Collate</b> check box is selected. 

If this flag is set when the <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> function returns, the application must simulate collation of multiple copies. For more information, see the description of the <b>PD_USEDEVMODECOPIESANDCOLLATE</b> flag.

See <b>PD_NOPAGENUMS</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="PD_DISABLEPRINTTOFILE"></a><a id="pd_disableprinttofile"></a><dl>
<dt><b>PD_DISABLEPRINTTOFILE</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
Disables the <b>Print to File</b> check box.

</td>
</tr>
<tr>
<td width="40%"><a id="PD_ENABLEPRINTHOOK"></a><a id="pd_enableprinthook"></a><dl>
<dt><b>PD_ENABLEPRINTHOOK</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
Enables the hook procedure specified in the <b>lpfnPrintHook</b> member. This enables the hook procedure for the <b>Print</b> dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="PD_ENABLEPRINTTEMPLATE"></a><a id="pd_enableprinttemplate"></a><dl>
<dt><b>PD_ENABLEPRINTTEMPLATE</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
Indicates that the <b>hInstance</b> and <b>lpPrintTemplateName</b> members specify a replacement for the default <b>Print</b> dialog box template. 

</td>
</tr>
<tr>
<td width="40%"><a id="PD_ENABLEPRINTTEMPLATEHANDLE"></a><a id="pd_enableprinttemplatehandle"></a><dl>
<dt><b>PD_ENABLEPRINTTEMPLATEHANDLE</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
Indicates that the <b>hPrintTemplate</b> member identifies a data block that contains a preloaded dialog box template. This template replaces the default template for the <b>Print</b> dialog box. The system ignores the <b>lpPrintTemplateName</b> member if this flag is specified. 

</td>
</tr>
<tr>
<td width="40%"><a id="PD_ENABLESETUPHOOK"></a><a id="pd_enablesetuphook"></a><dl>
<dt><b>PD_ENABLESETUPHOOK</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
Enables the hook procedure specified in the <b>lpfnSetupHook</b> member. This enables the hook procedure for the <b>Print Setup</b> dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="PD_ENABLESETUPTEMPLATE"></a><a id="pd_enablesetuptemplate"></a><dl>
<dt><b>PD_ENABLESETUPTEMPLATE</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
Indicates that the <b>hInstance</b> and <b>lpSetupTemplateName</b> members specify a replacement for the default <b>Print Setup</b> dialog box template. 

</td>
</tr>
<tr>
<td width="40%"><a id="PD_ENABLESETUPTEMPLATEHANDLE"></a><a id="pd_enablesetuptemplatehandle"></a><dl>
<dt><b>PD_ENABLESETUPTEMPLATEHANDLE</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
Indicates that the <b>hSetupTemplate</b> member identifies a data block that contains a preloaded dialog box template. This template replaces the default template for the <b>Print Setup</b> dialog box. The system ignores the <b>lpSetupTemplateName</b> member if this flag is specified. 

</td>
</tr>
<tr>
<td width="40%"><a id="PD_HIDEPRINTTOFILE"></a><a id="pd_hideprinttofile"></a><dl>
<dt><b>PD_HIDEPRINTTOFILE</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
Hides the <b>Print to File</b> check box.

</td>
</tr>
<tr>
<td width="40%"><a id="PD_NONETWORKBUTTON"></a><a id="pd_nonetworkbutton"></a><dl>
<dt><b>PD_NONETWORKBUTTON</b></dt>
<dt>0x00200000</dt>
</dl>
</td>
<td width="60%">
Hides and disables the <b>Network</b> button.

</td>
</tr>
<tr>
<td width="40%"><a id="PD_NOPAGENUMS"></a><a id="pd_nopagenums"></a><dl>
<dt><b>PD_NOPAGENUMS</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Disables the <b>Pages</b> radio button and the associated edit controls. Also, it causes the <b>Collate</b> check box to appear in the dialog.

</td>
</tr>
<tr>
<td width="40%"><a id="PD_NOSELECTION"></a><a id="pd_noselection"></a><dl>
<dt><b>PD_NOSELECTION</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Disables the <b>Selection</b> radio button.

</td>
</tr>
<tr>
<td width="40%"><a id="PD_NOWARNING"></a><a id="pd_nowarning"></a><dl>
<dt><b>PD_NOWARNING</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Prevents the warning message from being displayed when there is no default printer.

</td>
</tr>
<tr>
<td width="40%"><a id="PD_PAGENUMS"></a><a id="pd_pagenums"></a><dl>
<dt><b>PD_PAGENUMS</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the <b>Pages</b> radio button is selected. If this flag is set when the <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> function returns, the <b>nFromPage</b> and <b>nToPage</b> members indicate the starting and ending pages specified by the user.

</td>
</tr>
<tr>
<td width="40%"><a id="PD_PRINTSETUP"></a><a id="pd_printsetup"></a><dl>
<dt><b>PD_PRINTSETUP</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Causes the system to display the <b>Print Setup</b> dialog box rather than the <b>Print</b> dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="PD_PRINTTOFILE"></a><a id="pd_printtofile"></a><dl>
<dt><b>PD_PRINTTOFILE</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the <b>Print to File</b> check box is selected. If this flag is set when the <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> function returns, the offset indicated by the <b>wOutputOffset</b> member of the <a href="/windows/desktop/api/commdlg/ns-commdlg-devnames">DEVNAMES</a> structure contains the string "FILE:". When you call the <a href="/windows/desktop/api/wingdi/nf-wingdi-startdoca">StartDoc</a> function to start the printing operation, specify this "FILE:" string in the <b>lpszOutput</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-docinfoa">DOCINFO</a> structure. Specifying this string causes the print subsystem to query the user for the name of the output file. 

</td>
</tr>
<tr>
<td width="40%"><a id="PD_RETURNDC"></a><a id="pd_returndc"></a><dl>
<dt><b>PD_RETURNDC</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Causes <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> to return a device context matching the selections the user made in the dialog box. The device context is returned in <b>hDC</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="PD_RETURNDEFAULT"></a><a id="pd_returndefault"></a><dl>
<dt><b>PD_RETURNDEFAULT</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> function does not display the dialog box. Instead, it sets the <b>hDevNames</b> and <b>hDevMode</b> members to handles to <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> and <a href="/windows/desktop/api/commdlg/ns-commdlg-devnames">DEVNAMES</a> structures that are initialized for the system default printer. Both <b>hDevNames</b> and <b>hDevMode</b> must be <b>NULL</b>, or <b>PrintDlg</b> returns an error. 

</td>
</tr>
<tr>
<td width="40%"><a id="PD_RETURNIC"></a><a id="pd_returnic"></a><dl>
<dt><b>PD_RETURNIC</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
Similar to the <b>PD_RETURNDC</b> flag, except this flag returns an information context rather than a device context. If neither <b>PD_RETURNDC</b> nor <b>PD_RETURNIC</b> is specified, <b>hDC</b> is undefined on output.

</td>
</tr>
<tr>
<td width="40%"><a id="PD_SELECTION"></a><a id="pd_selection"></a><dl>
<dt><b>PD_SELECTION</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the <b>Selection</b> radio button is selected. If neither <b>PD_PAGENUMS</b> nor <b>PD_SELECTION</b> is set, the <b>All</b> radio button is selected. 

</td>
</tr>
<tr>
<td width="40%"><a id="PD_SHOWHELP"></a><a id="pd_showhelp"></a><dl>
<dt><b>PD_SHOWHELP</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
Causes the dialog box to display the  <b>Help</b> button. The <b>hwndOwner</b> member must specify the window to receive the <a href="/windows/desktop/dlgbox/helpmsgstring">HELPMSGSTRING</a> registered messages that the dialog box sends when the user clicks the <b>Help</b> button.

</td>
</tr>
<tr>
<td width="40%"><a id="PD_USEDEVMODECOPIES"></a><a id="pd_usedevmodecopies"></a><dl>
<dt><b>PD_USEDEVMODECOPIES</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
Same as <b>PD_USEDEVMODECOPIESANDCOLLATE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="PD_USEDEVMODECOPIESANDCOLLATE"></a><a id="pd_usedevmodecopiesandcollate"></a><dl>
<dt><b>PD_USEDEVMODECOPIESANDCOLLATE</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
This flag indicates whether your application supports multiple copies and collation. Set this flag on input to indicate that your application does not support multiple copies and collation. In this case, the <b>nCopies</b> member of the <b>PRINTDLG</b> structure always returns 1, and <b>PD_COLLATE</b> is never set in the <b>Flags</b> member. 

If this flag is not set, the application is responsible for printing and collating multiple copies. In this case, the <b>nCopies</b> member of the <b>PRINTDLG</b> structure indicates the number of copies the user wants to print, and the <b>PD_COLLATE</b> flag in the <b>Flags</b> member indicates whether the user wants collation. 

Regardless of whether this flag is set, an application can determine from <b>nCopies</b> and <b>PD_COLLATE</b> how many copies to render and whether to print them collated.

If this flag is set and the printer driver does not support multiple copies, the <b>Copies</b> edit control is disabled. Similarly, if this flag is set and the printer driver does not support collation, the <b>Collate</b> check box is disabled.

The <b>dmCopies</b> and <b>dmCollate</b> members of the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure contain the copies and collate information used by the printer driver. If this flag is set and the printer driver supports multiple copies, the <b>dmCopies</b> member indicates the number of copies requested by the user. If this flag is set and the printer driver supports collation, the <b>dmCollate</b> member of the <b>DEVMODE</b> structure indicates whether the user wants collation. If this flag is not set, the <b>dmCopies</b> member always returns 1, and the <b>dmCollate</b> member is always zero.

<b>Known issue on Windows 2000/XP/2003:</b> 
If this flag is not set before calling <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a>, <b>PrintDlg</b> might swap <b>nCopies</b> and <b>dmCopies</b> values when it returns. The workaround for this issue is use <b>dmCopies</b> if its value is larger than 1, else, use <b>nCopies</b>, for you to get the actual number of copies to be printed when <b>PrintDlg</b> returns.

</td>
</tr>
</table>
 

To ensure that <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> or <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> returns the correct values in the <b>dmCopies</b> and <b>dmCollate</b> members of the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure, set <b>PD_RETURNDC</b> = <b>TRUE</b> and <b>PD_USEDEVMODECOPIESANDCOLLATE</b> = <b>TRUE</b>. In so doing, the <b>nCopies</b> member of the <b>PRINTDLG</b> structure   is always 1 and <b>PD_COLLATE</b> is always <b>FALSE</b>.

To ensure that <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> or <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> returns the correct values in <b>nCopies</b> and <b>PD_COLLATE</b>, set <b>PD_RETURNDC</b> = <b>TRUE</b> and <b>PD_USEDEVMODECOPIESANDCOLLATE</b> = <b>FALSE</b>. In so doing, <b>dmCopies</b> is always 1 and  <b>dmCollate</b> is always <b>FALSE</b>.

On Windows Vista and Windows 7, when you call <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> or <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> with  <b>PD_RETURNDC</b> set to <b>TRUE</b> and <b>PD_USEDEVMODECOPIESANDCOLLATE</b> set to <b>FALSE</b>, the <b>PrintDlg</b> or <b>PrintDlgEx</b> function sets the number of copies in the  <b>nCopies</b> member of the <b>PRINTDLG</b> structure, and it sets the number of copies in the structure represented by the hDC member of the <b>PRINTDLG</b> structure. 


When making calls to GDI, you must ignore the value of <b>nCopies</b>, consider the value as 1, and use the returned hDC to avoid printing duplicate copies.

### -field nFromPage

Type: <b>WORD</b>

The initial value for the starting page edit control. 

When <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> returns, <b>nFromPage</b> is the starting page specified by the user. If the <b>Pages</b> radio button is selected when the user clicks the <b>Okay</b> button, <b>PrintDlg</b> sets the <b>PD_PAGENUMS</b> flag and does not return until the user enters a starting page value that is within the minimum to maximum page range. 

 If the input value for either <b>nFromPage</b> or <b>nToPage</b> is outside the minimum/maximum range, <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> returns an error only if the <b>PD_PAGENUMS</b> flag is specified; otherwise, it displays the dialog box but changes the out-of-range value to the minimum or maximum value.

### -field nToPage

Type: <b>WORD</b>

The initial value for the ending page edit control. When <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> returns, <b>nToPage</b> is the ending page specified by the user. If the <b>Pages</b> radio button is selected when the use clicks the <b>Okay</b> button, <b>PrintDlg</b> sets the <b>PD_PAGENUMS</b> flag and does not return until the user enters an ending page value that is within the minimum to maximum page range.

### -field nMinPage

Type: <b>WORD</b>

The minimum value for the page range specified in the <b>From</b> and <b>To</b> page edit controls. If <b>nMinPage</b> equals <b>nMaxPage</b>, the <b>Pages</b> radio button and the starting and ending page edit controls are disabled.

### -field nMaxPage

Type: <b>WORD</b>

The maximum value for the page range specified in the <b>From</b> and <b>To</b> page edit controls.

### -field nCopies

Type: <b>WORD</b>

The initial number of copies for the	<b>Copies</b> edit control if <b>hDevMode</b> is <b>NULL</b>; otherwise, the	<b>dmCopies</b> member of the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure contains the initial value. When <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> returns, <b>nCopies</b> contains the actual number of copies to print. This value depends on whether the application or the printer driver is responsible for printing multiple copies. If the <b>PD_USEDEVMODECOPIESANDCOLLATE</b> flag is set in the <b>Flags</b> member, <b>nCopies</b> is always 1 on return, and the printer driver is responsible for printing multiple copies. If the flag is not set, the application is responsible for printing the number of copies specified by <b>nCopies</b>. For more information, see the description of the <b>PD_USEDEVMODECOPIESANDCOLLATE</b> flag.

### -field hInstance

Type: <b>HINSTANCE</b>

If the <b>PD_ENABLEPRINTTEMPLATE</b> or <b>PD_ENABLESETUPTEMPLATE</b> flag is set in the <b>Flags</b> member, <b>hInstance</b> is a handle to the application or module instance that contains the dialog box template named by the <b>lpPrintTemplateName</b> or <b>lpSetupTemplateName</b> member.

### -field lCustData

Type: <b>LPARAM</b>

Application-defined data that the system passes to the hook procedure identified by the <b>lpfnPrintHook</b> or <b>lpfnSetupHook</b> member. When the system sends the <a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a> message to the hook procedure, the message's <i>lParam</i> parameter is a pointer to the <b>PRINTDLG</b> structure specified when the dialog was created. The hook procedure can use this pointer to get the <b>lCustData</b> value.

### -field lpfnPrintHook

Type: <b>LPPRINTHOOKPROC</b>

A pointer to a <a href="/windows/desktop/api/commdlg/nc-commdlg-lpprinthookproc">PrintHookProc</a> hook procedure that can process messages intended for the <b>Print</b> dialog box. This member is ignored unless the <b>PD_ENABLEPRINTHOOK</b> flag is set in the <b>Flags</b> member.

### -field lpfnSetupHook

Type: <b>LPSETUPHOOKPROC</b>

A pointer to a <a href="/windows/desktop/api/commdlg/nc-commdlg-lpsetuphookproc">SetupHookProc</a> hook procedure that can process messages intended for the <b>Print Setup</b> dialog box. This member is ignored unless the <b>PD_ENABLESETUPHOOK</b> flag is set in the <b>Flags</b> member.

### -field lpPrintTemplateName

Type: <b>LPCTSTR</b>

The name of the dialog box template resource in the module identified by the <b>hInstance</b> member. This template replaces the default <b>Print</b> dialog box template. This member is ignored unless the <b>PD_ENABLEPRINTTEMPLATE</b> flag is set in the <b>Flags</b> member.

### -field lpSetupTemplateName

Type: <b>LPCTSTR</b>

The name of the dialog box template resource in the module identified by the <b>hInstance</b> member. This template replaces the default <b>Print Setup</b> dialog box template. This member is ignored unless the <b>PD_ENABLESETUPTEMPLATE</b> flag is set in the <b>Flags</b> member.

### -field hPrintTemplate

Type: <b>HGLOBAL</b>

If the <b>PD_ENABLEPRINTTEMPLATEHANDLE</b> flag is set in the <b>Flags</b> member, <b>hPrintTemplate</b> is a handle to a memory object containing a dialog box template. This template replaces the default <b>Print</b> dialog box template.

### -field hSetupTemplate

Type: <b>HGLOBAL</b>

If the <b>PD_ENABLESETUPTEMPLATEHANDLE</b> flag is set in the <b>Flags</b> member, <b>hSetupTemplate</b> is a handle to a memory object containing a dialog box template. This template replaces the default <b>Print Setup</b> dialog box template.

## -remarks

If both 
				<b>hDevMode</b> and <b>hDevNames</b> are <b>NULL</b>, <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> initializes the dialog box using the current default printer. To initialize the dialog box for a different printer, use the <b>wDeviceOffset</b> member of the <a href="/windows/desktop/api/commdlg/ns-commdlg-devnames">DEVNAMES</a> structure to specify the name of the printer. 

Note that the <b>dmDeviceName</b> member of the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a>  structure also specifies a printer name. However, <b>dmDeviceName</b> is limited to 32 characters, and the <b>wDeviceOffset</b> name is not. If the <b>wDeviceOffset</b> and <b>dmDeviceName</b> names are not the same, <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> initializes the dialog box using the printer specified by <b>wDeviceOffset</b>. 

If the <b>PD_RETURNDEFAULT</b> flag is set and both <b>hDevMode</b> and <b>hDevNames</b> are <b>NULL</b>, <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> uses the <b>hDevNames</b> and <b>hDevMode</b> members to return information about the current default printer without displaying the dialog box.





> [!NOTE]
> The commdlg.h header defines PRINTDLG as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/dlgbox/common-dialog-box-library">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a>



<a href="/windows/desktop/api/commdlg/ns-commdlg-devnames">DEVNAMES</a>



<a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a>



<b>Reference</b>



<a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a>
