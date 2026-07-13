---
UID: NS:commdlg.tagPSDW
title: PAGESETUPDLGW (commdlg.h)
description: Contains information the PageSetupDlg function uses to initialize the Page Setup dialog box. After the user closes the dialog box, the system returns information about the user-defined page parameters in this structure. (Unicode)
helpviewer_keywords: ["*LPPAGESETUPDLGW","LPPAGESETUPDLG","LPPAGESETUPDLG structure pointer [Dialog Boxes]","PAGESETUPDLG","PAGESETUPDLG structure [Dialog Boxes]","PAGESETUPDLGA","PAGESETUPDLGW","PSD_DEFAULTMINMARGINS","PSD_DISABLEMARGINS","PSD_DISABLEORIENTATION","PSD_DISABLEPAGEPAINTING","PSD_DISABLEPAPER","PSD_DISABLEPRINTER","PSD_ENABLEPAGEPAINTHOOK","PSD_ENABLEPAGESETUPHOOK","PSD_ENABLEPAGESETUPTEMPLATE","PSD_ENABLEPAGESETUPTEMPLATEHANDLE","PSD_INHUNDREDTHSOFMILLIMETERS","PSD_INTHOUSANDTHSOFINCHES","PSD_INWININIINTLMEASURE","PSD_MARGINS","PSD_MINMARGINS","PSD_NONETWORKBUTTON","PSD_NOWARNING","PSD_RETURNDEFAULT","PSD_SHOWHELP","_win32_PAGESETUPDLG_str","_win32_pagesetupdlg_str_cpp","commdlg/LPPAGESETUPDLG","commdlg/PAGESETUPDLG","commdlg/PAGESETUPDLGA","commdlg/PAGESETUPDLGW","dlgbox.pagesetupdlg_str","tagPSDA","tagPSDW","winui._win32_pagesetupdlg_str"]
old-location: dlgbox\pagesetupdlg_str.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxstructures\pagesetupdlg.htm
ms.date: 12/05/2018
ms.keywords: '*LPPAGESETUPDLGW, LPPAGESETUPDLG, LPPAGESETUPDLG structure pointer [Dialog Boxes], PAGESETUPDLG, PAGESETUPDLG structure [Dialog Boxes], PAGESETUPDLGA, PAGESETUPDLGW, PSD_DEFAULTMINMARGINS, PSD_DISABLEMARGINS, PSD_DISABLEORIENTATION, PSD_DISABLEPAGEPAINTING, PSD_DISABLEPAPER, PSD_DISABLEPRINTER, PSD_ENABLEPAGEPAINTHOOK, PSD_ENABLEPAGESETUPHOOK, PSD_ENABLEPAGESETUPTEMPLATE, PSD_ENABLEPAGESETUPTEMPLATEHANDLE, PSD_INHUNDREDTHSOFMILLIMETERS, PSD_INTHOUSANDTHSOFINCHES, PSD_INWININIINTLMEASURE, PSD_MARGINS, PSD_MINMARGINS, PSD_NONETWORKBUTTON, PSD_NOWARNING, PSD_RETURNDEFAULT, PSD_SHOWHELP, _win32_PAGESETUPDLG_str, _win32_pagesetupdlg_str_cpp, commdlg/LPPAGESETUPDLG, commdlg/PAGESETUPDLG, commdlg/PAGESETUPDLGA, commdlg/PAGESETUPDLGW, dlgbox.pagesetupdlg_str, tagPSDA, tagPSDW, winui._win32_pagesetupdlg_str'
req.header: commdlg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PAGESETUPDLGW (Unicode) and PAGESETUPDLGA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PAGESETUPDLGW, *LPPAGESETUPDLGW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPSDW
 - commdlg/tagPSDW
 - LPPAGESETUPDLGW
 - commdlg/LPPAGESETUPDLGW
 - PAGESETUPDLGW
 - commdlg/PAGESETUPDLGW
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
 - PAGESETUPDLG
 - PAGESETUPDLGA
 - PAGESETUPDLGW
---

# PAGESETUPDLGW structure


## -description

Contains information the <a href="/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)">PageSetupDlg</a> function uses to initialize the <b>Page Setup</b> dialog box. After the user closes the dialog box, the system returns information about the user-defined page parameters in this structure.

## -struct-fields

### -field lStructSize

Type: <b>DWORD</b>

The size, in bytes, of this structure.

### -field hwndOwner

Type: <b>HWND</b>

A handle to the window that owns the dialog box. This member can be any valid window handle, or it can be <b>NULL</b> if the dialog box has no owner.

### -field hDevMode

Type: <b>HGLOBAL</b>

A handle to a global memory object that contains a <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure. On input, if a handle is specified, the values in the corresponding <b>DEVMODE</b> structure are used to initialize the controls in the dialog box. On output, the dialog box sets <b>hDevMode</b> to a global memory handle to a <b>DEVMODE</b> structure that contains values specifying the user's selections. If the user's selections are not available, the dialog box sets <b>hDevMode</b> to <b>NULL</b>.

### -field hDevNames

Type: <b>HGLOBAL</b>

A handle to a global memory object that contains a <a href="/windows/desktop/api/commdlg/ns-commdlg-devnames">DEVNAMES</a> structure. This structure contains three strings that specify the driver name, the printer name, and the output port name. On input, if a handle is specified, the strings in the corresponding <b>DEVNAMES</b> structure are used to initialize controls in the dialog box. On output, the dialog box sets 
					<b>hDevNames</b> to a global memory handle to a <b>DEVNAMES</b> structure that contains strings specifying the user's selections. If the user's selections are not available, the dialog box sets <b>hDevNames</b> to <b>NULL</b>.

### -field Flags

Type: <b>DWORD</b>

A set of bit flags that you can use to initialize the <b>Page Setup</b> dialog box. When the dialog box returns, it sets these flags to indicate the user's input. This member can be one or more of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PSD_DEFAULTMINMARGINS"></a><a id="psd_defaultminmargins"></a><dl>
<dt><b>PSD_DEFAULTMINMARGINS</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Sets the minimum values that the user can specify for the page margins to be the minimum margins allowed by the printer. This is the default. This flag is ignored if the <b>PSD_MARGINS</b> and <b>PSD_MINMARGINS</b> flags are also specified.

</td>
</tr>
<tr>
<td width="40%"><a id="PSD_DISABLEMARGINS"></a><a id="psd_disablemargins"></a><dl>
<dt><b>PSD_DISABLEMARGINS</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Disables the margin controls, preventing the user from setting the margins.

</td>
</tr>
<tr>
<td width="40%"><a id="PSD_DISABLEORIENTATION"></a><a id="psd_disableorientation"></a><dl>
<dt><b>PSD_DISABLEORIENTATION</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Disables the orientation controls, preventing the user from setting the page orientation.

</td>
</tr>
<tr>
<td width="40%"><a id="PSD_DISABLEPAGEPAINTING"></a><a id="psd_disablepagepainting"></a><dl>
<dt><b>PSD_DISABLEPAGEPAINTING</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
Prevents the dialog box from drawing the contents of the sample page. If you enable a <a href="/windows/desktop/api/commdlg/nc-commdlg-lppagepainthook">PagePaintHook</a> hook procedure, you can still draw the contents of the sample page.

</td>
</tr>
<tr>
<td width="40%"><a id="PSD_DISABLEPAPER"></a><a id="psd_disablepaper"></a><dl>
<dt><b>PSD_DISABLEPAPER</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
Disables the paper controls, preventing the user from setting page parameters such as the paper size and source.

</td>
</tr>
<tr>
<td width="40%"><a id="PSD_DISABLEPRINTER"></a><a id="psd_disableprinter"></a><dl>
<dt><b>PSD_DISABLEPRINTER</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Obsolete.

<b>Windows XP/2000:  </b>Disables the <b>Printer</b> button, preventing the user from invoking a dialog box that contains additional printer setup information.

</td>
</tr>
<tr>
<td width="40%"><a id="PSD_ENABLEPAGEPAINTHOOK"></a><a id="psd_enablepagepainthook"></a><dl>
<dt><b>PSD_ENABLEPAGEPAINTHOOK</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
Enables the hook procedure specified in the 
						<b>lpfnPagePaintHook</b> member. 

</td>
</tr>
<tr>
<td width="40%"><a id="PSD_ENABLEPAGESETUPHOOK"></a><a id="psd_enablepagesetuphook"></a><dl>
<dt><b>PSD_ENABLEPAGESETUPHOOK</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
Enables the hook procedure specified in the <b>lpfnPageSetupHook</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="PSD_ENABLEPAGESETUPTEMPLATE"></a><a id="psd_enablepagesetuptemplate"></a><dl>
<dt><b>PSD_ENABLEPAGESETUPTEMPLATE</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
Indicates that the <b>hInstance</b> and <b>lpPageSetupTemplateName</b> members specify a dialog box template to use in place of the default template.

</td>
</tr>
<tr>
<td width="40%"><a id="PSD_ENABLEPAGESETUPTEMPLATEHANDLE"></a><a id="psd_enablepagesetuptemplatehandle"></a><dl>
<dt><b>PSD_ENABLEPAGESETUPTEMPLATEHANDLE</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
Indicates that the <b>hPageSetupTemplate</b> member identifies a data block that contains a preloaded dialog box template. The system ignores the <b>lpPageSetupTemplateName</b> member if this flag is specified. 

</td>
</tr>
<tr>
<td width="40%"><a id="PSD_INHUNDREDTHSOFMILLIMETERS"></a><a id="psd_inhundredthsofmillimeters"></a><dl>
<dt><b>PSD_INHUNDREDTHSOFMILLIMETERS</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Indicates that hundredths of millimeters are the unit of measurement for margins and paper size. The values in the <b>rtMargin</b>, <b>rtMinMargin</b>, and <b>ptPaperSize</b> members are in hundredths of millimeters. You can set this flag on input to override the default unit of measurement for the user's locale. When the function returns, the dialog box sets this flag to indicate the units used.

</td>
</tr>
<tr>
<td width="40%"><a id="PSD_INTHOUSANDTHSOFINCHES"></a><a id="psd_inthousandthsofinches"></a><dl>
<dt><b>PSD_INTHOUSANDTHSOFINCHES</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Indicates that thousandths of inches are the unit of measurement for margins and paper size. The values in the <b>rtMargin</b>, <b>rtMinMargin</b>, and <b>ptPaperSize</b> members are in thousandths of inches. You can set this flag on input to override the default unit of measurement for the user's locale. When the function returns, the dialog box sets this flag to indicate the units used.

</td>
</tr>
<tr>
<td width="40%"><a id="PSD_INWININIINTLMEASURE"></a><a id="psd_inwininiintlmeasure"></a><dl>
<dt><b>PSD_INWININIINTLMEASURE</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
<tr>
<td width="40%"><a id="PSD_MARGINS"></a><a id="psd_margins"></a><dl>
<dt><b>PSD_MARGINS</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Causes the system to use the values specified in the <b>rtMargin</b> member as the initial widths for the left, top, right, and bottom margins. If <b>PSD_MARGINS</b> is not set, the system sets the initial widths to one inch for all margins. 

</td>
</tr>
<tr>
<td width="40%"><a id="PSD_MINMARGINS"></a><a id="psd_minmargins"></a><dl>
<dt><b>PSD_MINMARGINS</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Causes the system to use the values specified in the <b>rtMinMargin</b> member as the minimum allowable widths for the left, top, right, and bottom margins. The system prevents the user from entering a width that is less than the specified minimum. If <b>PSD_MINMARGINS</b> is not specified, the system sets the minimum allowable widths to those allowed by the printer. 

</td>
</tr>
<tr>
<td width="40%"><a id="PSD_NONETWORKBUTTON"></a><a id="psd_nonetworkbutton"></a><dl>
<dt><b>PSD_NONETWORKBUTTON</b></dt>
<dt>0x00200000</dt>
</dl>
</td>
<td width="60%">
Hides and disables the <b>Network</b> button. 

</td>
</tr>
<tr>
<td width="40%"><a id="PSD_NOWARNING"></a><a id="psd_nowarning"></a><dl>
<dt><b>PSD_NOWARNING</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Prevents the system from displaying a warning message when there is no default printer.

</td>
</tr>
<tr>
<td width="40%"><a id="PSD_RETURNDEFAULT"></a><a id="psd_returndefault"></a><dl>
<dt><b>PSD_RETURNDEFAULT</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">

<a href="/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)">PageSetupDlg</a> does not display the dialog box. Instead, it sets the <b>hDevNames</b> and <b>hDevMode</b> members to handles to <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> and <a href="/windows/desktop/api/commdlg/ns-commdlg-devnames">DEVNAMES</a> structures that are initialized for the system default printer. <b>PageSetupDlg</b> returns an error if either <b>hDevNames</b> or 	<b>hDevMode</b> is not <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="PSD_SHOWHELP"></a><a id="psd_showhelp"></a><dl>
<dt><b>PSD_SHOWHELP</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
Causes the dialog box to display the 	<b>Help</b> button. The <b>hwndOwner</b> member must specify the window to receive the <a href="/windows/desktop/dlgbox/helpmsgstring">HELPMSGSTRING</a> registered messages that the dialog box sends when the user clicks the <b>Help</b> button.

</td>
</tr>
</table>

### -field ptPaperSize

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

The dimensions of the paper selected by the user. The <b>PSD_INTHOUSANDTHSOFINCHES</b> or <b>PSD_INHUNDREDTHSOFMILLIMETERS</b> flag indicates the units of measurement.

### -field rtMinMargin

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

The minimum allowable widths for the left, top, right, and bottom margins. The system ignores this member if the <b>PSD_MINMARGINS</b> flag is not set. These values must be less than or equal to the values specified in the <b>rtMargin</b> member. The <b>PSD_INTHOUSANDTHSOFINCHES</b> or <b>PSD_INHUNDREDTHSOFMILLIMETERS</b> flag indicates the units of measurement.

### -field rtMargin

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

The widths of the left, top, right, and bottom margins. If you set the <b>PSD_MARGINS</b> flag, <b>rtMargin</b> specifies the initial margin values. When <a href="/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)">PageSetupDlg</a> returns, <b>rtMargin</b> contains the margin widths selected by the user. The <b>PSD_INHUNDREDTHSOFMILLIMETERS</b> or <b>PSD_INTHOUSANDTHSOFINCHES</b> flag indicates the units of measurement.

### -field hInstance

Type: <b>HINSTANCE</b>

If the <b>PSD_ENABLEPAGESETUPTEMPLATE</b> flag is set in the <b>Flags</b> member, <b>hInstance</b> is a handle to the application or module instance that contains the dialog box template named by the <b>lpPageSetupTemplateName</b> member.

### -field lCustData

Type: <b>LPARAM</b>

Application-defined data that the system passes to the hook procedure identified by the <b>lpfnPageSetupHook</b> member. When the system sends the <a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a> message to the hook procedure, the message's <i>lParam</i> parameter is a pointer to the <b>PAGESETUPDLG</b> structure specified when the dialog was created. The hook procedure can use this pointer to get the <b>lCustData</b> value.

### -field lpfnPageSetupHook

Type: <b>LPPAGESETUPHOOK</b>

A pointer to a <a href="/windows/desktop/api/commdlg/nc-commdlg-lppagesetuphook">PageSetupHook</a> hook procedure that can process messages intended for the dialog box. This member is ignored unless the <b>PSD_ENABLEPAGESETUPHOOK</b> flag is set in the <b>Flags</b> member.

### -field lpfnPagePaintHook

Type: <b>LPPAGEPAINTHOOK</b>

A pointer to a <a href="/windows/desktop/api/commdlg/nc-commdlg-lppagepainthook">PagePaintHook</a> hook procedure that receives <b>WM_PSD_*</b> messages from the dialog box whenever the sample page is redrawn. By processing the messages, the hook procedure can customize the appearance of the sample page. This member is ignored unless the <b>PSD_ENABLEPAGEPAINTHOOK</b> flag is set in the <b>Flags</b> member.

### -field lpPageSetupTemplateName

Type: <b>LPCTSTR</b>

The name of the dialog box template resource in the module identified by the <b>hInstance</b> member. This template is substituted for the standard dialog box template. For numbered dialog box resources, <b>lpPageSetupTemplateName</b> can be a value returned by the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro. This member is ignored unless the <b>PSD_ENABLEPAGESETUPTEMPLATE</b> flag is set in the <b>Flags</b> member.

### -field hPageSetupTemplate

Type: <b>HGLOBAL</b>

If the <b>PSD_ENABLEPAGESETUPTEMPLATEHANDLE</b> flag is set in the <b>Flags</b> member, <b>hPageSetupTemplate</b> is a handle to a memory object containing a dialog box template.

## -remarks

If the <b>PSD_INHUNDREDTHSOFMILLIMETERS</b> and <b>PSD_INTHOUSANDTHSOFINCHES</b> flags are not specified, the system queries the <b>LOCALE_IMEASURE</b> value of the default user locale to determine the unit of measure (either hundredths of millimeters or thousandths of inches) for the margin widths and paper size. 

If both <b>hDevNames</b> and <b>hDevMode</b> have valid handles and the printer name specified by the 
				<b>wDeviceOffset</b> member of the <a href="/windows/desktop/api/commdlg/ns-commdlg-devnames">DEVNAMES</a> structure is not the same as the name specified by the <b>dmDeviceName</b> member of the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure, the system uses the name specified by <b>wDeviceOffset</b> by default. 





> [!NOTE]
> The commdlg.h header defines PAGESETUPDLG as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/dlgbox/common-dialog-box-library">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a>



<a href="/windows/desktop/api/commdlg/ns-commdlg-devnames">DEVNAMES</a>



<a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a>



<b>Other Resources</b>



<a href="/windows/desktop/api/commdlg/nc-commdlg-lppagepainthook">PagePaintHook</a>



<a href="/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)">PageSetupDlg</a>



<a href="/windows/desktop/api/commdlg/nc-commdlg-lppagesetuphook">PageSetupHook</a>



<b>Reference</b>



<a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a>
