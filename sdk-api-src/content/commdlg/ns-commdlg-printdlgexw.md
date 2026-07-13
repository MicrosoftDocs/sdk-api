---
UID: NS:commdlg.tagPDEXW
title: PRINTDLGEXW (commdlg.h)
description: Contains information that the PrintDlgEx function uses to initialize the Print property sheet. After the user closes the property sheet, the system uses this structure to return information about the user's selections. (Unicode)
helpviewer_keywords: ["*LPPRINTDLGEXW","LPPRINTDLGEX","LPPRINTDLGEX structure pointer [Dialog Boxes]","PD_ALLPAGES","PD_COLLATE","PD_CURRENTPAGE","PD_DISABLEPRINTTOFILE","PD_ENABLEPRINTTEMPLATE","PD_ENABLEPRINTTEMPLATEHANDLE","PD_EXCLUSIONFLAGS","PD_EXCL_COPIESANDCOLLATE","PD_HIDEPRINTTOFILE","PD_NOCURRENTPAGE","PD_NOPAGENUMS","PD_NOSELECTION","PD_NOWARNING","PD_PAGENUMS","PD_PRINTTOFILE","PD_RESULT_APPLY","PD_RESULT_CANCEL","PD_RESULT_PRINT","PD_RETURNDC","PD_RETURNDEFAULT","PD_RETURNIC","PD_SELECTION","PD_USEDEVMODECOPIES","PD_USEDEVMODECOPIESANDCOLLATE","PD_USELARGETEMPLATE","PRINTDLGEX","PRINTDLGEX structure [Dialog Boxes]","PRINTDLGEXA","PRINTDLGEXW","_win32_PRINTDLGEX_str","_win32_printdlgex_str_cpp","commdlg/LPPRINTDLGEX","commdlg/PRINTDLGEX","commdlg/PRINTDLGEXA","commdlg/PRINTDLGEXW","dlgbox.printdlgex_str","tagPDEXA","tagPDEXW","winui._win32_printdlgex_str"]
old-location: dlgbox\printdlgex_str.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxstructures\printdlgex.htm
ms.date: 12/05/2018
ms.keywords: '*LPPRINTDLGEXW, LPPRINTDLGEX, LPPRINTDLGEX structure pointer [Dialog Boxes], PD_ALLPAGES, PD_COLLATE, PD_CURRENTPAGE, PD_DISABLEPRINTTOFILE, PD_ENABLEPRINTTEMPLATE, PD_ENABLEPRINTTEMPLATEHANDLE, PD_EXCLUSIONFLAGS, PD_EXCL_COPIESANDCOLLATE, PD_HIDEPRINTTOFILE, PD_NOCURRENTPAGE, PD_NOPAGENUMS, PD_NOSELECTION, PD_NOWARNING, PD_PAGENUMS, PD_PRINTTOFILE, PD_RESULT_APPLY, PD_RESULT_CANCEL, PD_RESULT_PRINT, PD_RETURNDC, PD_RETURNDEFAULT, PD_RETURNIC, PD_SELECTION, PD_USEDEVMODECOPIES, PD_USEDEVMODECOPIESANDCOLLATE, PD_USELARGETEMPLATE, PRINTDLGEX, PRINTDLGEX structure [Dialog Boxes], PRINTDLGEXA, PRINTDLGEXW, _win32_PRINTDLGEX_str, _win32_printdlgex_str_cpp, commdlg/LPPRINTDLGEX, commdlg/PRINTDLGEX, commdlg/PRINTDLGEXA, commdlg/PRINTDLGEXW, dlgbox.printdlgex_str, tagPDEXA, tagPDEXW, winui._win32_printdlgex_str'
req.header: commdlg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PRINTDLGEXW (Unicode) and PRINTDLGEXA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PRINTDLGEXW, *LPPRINTDLGEXW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPDEXW
 - commdlg/tagPDEXW
 - LPPRINTDLGEXW
 - commdlg/LPPRINTDLGEXW
 - PRINTDLGEXW
 - commdlg/PRINTDLGEXW
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
 - PRINTDLGEX
 - PRINTDLGEXA
 - PRINTDLGEXW
---

# PRINTDLGEXW structure


## -description

Contains information that the <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> function uses to initialize the <a href="/windows/desktop/dlgbox/print-property-sheet">Print property sheet</a>. After the user closes the property sheet, the system uses this structure to return information about the user's selections.

## -struct-fields

### -field lStructSize

Type: <b>DWORD</b>

The structure size, in bytes.

### -field hwndOwner

Type: <b>HWND</b>

A handle to the window that owns the property sheet. This member must be a valid window handle; it cannot be <b>NULL</b>.

### -field hDevMode

Type: <b>HGLOBAL</b>

A handle to a movable global memory object that contains a <a href="/windows/win32/api/wingdi/ns-wingdi-devmodew">DEVMODE</a> structure. If <b>hDevMode</b> is not <b>NULL</b> on input, you must allocate a movable block of memory for the <b>DEVMODE</b> structure and initialize its members. The <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> function uses the input data to initialize the controls in the property sheet. When <b>PrintDlgEx</b> returns, the <b>DEVMODE</b> members indicate the user's input.

If <b>hDevMode</b> is <b>NULL</b> on input, <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> allocates memory for the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure, initializes its members to indicate the user's input, and returns a handle that identifies it. 

For more information about the <b>hDevMode</b> and <b>hDevNames</b> members, see the Remarks section at the end of this topic.

### -field hDevNames

Type: <b>HGLOBAL</b>

A handle to a movable global memory object that contains a <a href="/windows/desktop/api/commdlg/ns-commdlg-devnames">DEVNAMES</a> structure. If <b>hDevNames</b> is not <b>NULL</b> on input, you must allocate a movable block of memory for the <b>DEVNAMES</b> structure and initialize its members. The <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> function uses the input data to initialize the controls in the property sheet. When <b>PrintDlgEx</b> returns, the <b>DEVNAMES</b> members contain information for the printer chosen by the user. You can use this information to create a device context or an information context.

The <b>hDevNames</b> member can be <b>NULL</b>, in which case, <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> allocates memory for the <a href="/windows/desktop/api/commdlg/ns-commdlg-devnames">DEVNAMES</a> structure, initializes its members to indicate the user's input, and returns a handle that identifies it. 

For more information about the <b>hDevMode</b> and <b>hDevNames</b> members, see the Remarks section at the end of this topic.

### -field hDC

Type: <b>HDC</b>

A handle to a device context or an information context, depending on whether the <b>Flags</b> member specifies the <b>PD_RETURNDC</b> or <b>PC_RETURNIC</b> flag. If neither flag is specified, the value of this member is undefined. If both flags are specified, <b>PD_RETURNDC</b> has priority.

### -field Flags

Type: <b>DWORD</b>

A set of bit flags that you can use to initialize the <b>Print</b> property sheet. When the <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> function returns, it sets these flags to indicate the user's input. This member can be one or more of the following values. 

To ensure that <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> or <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> returns the correct values in the <b>dmCopies</b> and <b>dmCollate</b> members of the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure, set <b>PD_RETURNDC</b> = <b>TRUE</b> and <b>PD_USEDEVMODECOPIESANDCOLLATE</b> = <b>TRUE</b>. In so doing, the <b>nCopies</b> member of the <a href="/windows/win32/api/commdlg/ns-commdlg-printdlga">PRINTDLG</a> structure   is always 1 and <b>PD_COLLATE</b> is always <b>FALSE</b>.

To ensure that <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> or <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> returns the correct values in <b>nCopies</b> and <b>PD_COLLATE</b>, set <b>PD_RETURNDC</b> = <b>TRUE</b> and <b>PD_USEDEVMODECOPIESANDCOLLATE</b> = <b>FALSE</b>. In so doing, <b>dmCopies</b> is always 1 and  <b>dmCollate</b> is always <b>FALSE</b>.

Starting with Windows Vista, when you call <a href="/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)">PrintDlg</a> or <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> with  <b>PD_RETURNDC</b> set to <b>TRUE</b> and <b>PD_USEDEVMODECOPIESANDCOLLATE</b> set to <b>FALSE</b>, the <b>PrintDlg</b> or <b>PrintDlgEx</b> function sets the number of copies in the  <b>nCopies</b> member of the <a href="/windows/win32/api/commdlg/ns-commdlg-printdlga">PRINTDLG</a> structure, and  it sets the number of copies in the structure represented by the <b>hDC</b> member of the <b>PRINTDLG</b> structure. 


When making calls to GDI, you must ignore the value of <b>nCopies</b>, consider the value as 1, and use the returned <b>hDC</b> to avoid printing duplicate copies.

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
The default flag that indicates that the <b>All</b> radio button is initially selected. This flag is used as a placeholder to indicate that the <b>PD_PAGENUMS</b>, <b>PD_SELECTION</b>, and <b>PD_CURRENTPAGE</b> flags are not specified. 

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

If this flag is set when the <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> function returns, the application must simulate collation of multiple copies. For more information, see the description of the <b>PD_USEDEVMODECOPIESANDCOLLATE</b> flag.

See <b>PD_NOPAGENUMS</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="PD_CURRENTPAGE"></a><a id="pd_currentpage"></a><dl>
<dt><b>PD_CURRENTPAGE</b></dt>
<dt>0x00400000</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the <b>Current Page</b> radio button is selected. If none of the <b>PD_PAGENUMS</b>, <b>PD_SELECTION</b>, or <b>PD_CURRENTPAGE</b> flags is set, the <b>All</b> radio button is selected. 

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
<td width="40%"><a id="PD_ENABLEPRINTTEMPLATE"></a><a id="pd_enableprinttemplate"></a><dl>
<dt><b>PD_ENABLEPRINTTEMPLATE</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
Indicates that the <b>hInstance</b> and <b>lpPrintTemplateName</b> members specify a replacement for the default dialog box template in the lower portion of the <b>General</b> page. The default template contains controls similar to those of the <b>Print</b> dialog box. The system uses the specified template to create a window that is a child of the <b>General</b> page.

</td>
</tr>
<tr>
<td width="40%"><a id="PD_ENABLEPRINTTEMPLATEHANDLE"></a><a id="pd_enableprinttemplatehandle"></a><dl>
<dt><b>PD_ENABLEPRINTTEMPLATEHANDLE</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
Indicates that the <b>hInstance</b> member identifies a data block that contains a preloaded dialog box template. This template replaces the default dialog box template in the lower portion of the <b>General</b> page. The system uses the specified template to create a window that is a child of the <b>General</b> page. The system ignores the <b>lpPrintTemplateName</b> member if this flag is specified.

</td>
</tr>
<tr>
<td width="40%"><a id="PD_EXCLUSIONFLAGS"></a><a id="pd_exclusionflags"></a><dl>
<dt><b>PD_EXCLUSIONFLAGS</b></dt>
<dt>0x01000000</dt>
</dl>
</td>
<td width="60%">
Indicates that the <b>ExclusionFlags</b> member identifies items to be excluded from the printer driver property pages. If this flag is not set, items will be excluded by default from the printer driver property pages. The exclusions prevent the duplication of items among the <b>General</b> page, any application-specified pages, and the printer driver pages.

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
<td width="40%"><a id="PD_NOCURRENTPAGE"></a><a id="pd_nocurrentpage"></a><dl>
<dt><b>PD_NOCURRENTPAGE</b></dt>
<dt>0x00800000</dt>
</dl>
</td>
<td width="60%">
Disables the <b>Current Page</b> radio button. 

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
Prevents the warning message from being displayed when an error occurs.

</td>
</tr>
<tr>
<td width="40%"><a id="PD_PAGENUMS"></a><a id="pd_pagenums"></a><dl>
<dt><b>PD_PAGENUMS</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the <b>Pages</b> radio button is selected. If none of the <b>PD_PAGENUMS</b>, <b>PD_SELECTION</b>, or <b>PD_CURRENTPAGE</b> flags is set, the <b>All</b> radio button is selected. If this flag is set when the <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> function returns, the <b>lpPageRanges</b> member indicates the page ranges specified by the user. 

</td>
</tr>
<tr>
<td width="40%"><a id="PD_PRINTTOFILE"></a><a id="pd_printtofile"></a><dl>
<dt><b>PD_PRINTTOFILE</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the <b>Print to File</b> check box is selected. If this flag is set when <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> returns, the offset indicated by the <b>wOutputOffset</b> member of the <a href="/windows/desktop/api/commdlg/ns-commdlg-devnames">DEVNAMES</a> structure contains the string "FILE:". When you call the <a href="/windows/desktop/api/wingdi/nf-wingdi-startdoca">StartDoc</a> function to start the printing operation, specify this "FILE:" string in the <b>lpszOutput</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-docinfoa">DOCINFO</a> structure. Specifying this string causes the print subsystem to query the user for the name of the output file. 

</td>
</tr>
<tr>
<td width="40%"><a id="PD_RETURNDC"></a><a id="pd_returndc"></a><dl>
<dt><b>PD_RETURNDC</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Causes <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> to return a device context matching the selections the user made in the property sheet. The device context is returned in <b>hDC</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="PD_RETURNDEFAULT"></a><a id="pd_returndefault"></a><dl>
<dt><b>PD_RETURNDEFAULT</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> function does not display the property sheet. Instead, it sets the <b>hDevNames</b> and <b>hDevMode</b> members to handles to <a href="/windows/desktop/api/commdlg/ns-commdlg-devnames">DEVNAMES</a> and <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structures that are initialized for the system default printer. Both <b>hDevNames</b> and <b>hDevMode</b> must be <b>NULL</b>, or <b>PrintDlgEx</b> returns an error. 

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
If this flag is set, the <b>Selection</b> radio button is selected. If none of the <b>PD_PAGENUMS</b>, <b>PD_SELECTION</b>, or <b>PD_CURRENTPAGE</b> flags is set, the <b>All</b> radio button is selected. 

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
This flag indicates whether your application supports multiple copies and collation. Set this flag on input to indicate that your application does not support multiple copies and collation. In this case, the <b>nCopies</b> member of the <b>PRINTDLGEX</b> structure always returns 1, and <b>PD_COLLATE</b> is never set in the <b>Flags</b> member.

If this flag is not set, the application is responsible for printing and collating multiple copies. In this case, the <b>nCopies</b> member of the <b>PRINTDLGEX</b> structure indicates the number of copies the user wants to print, and the <b>PD_COLLATE</b> flag in the <b>Flags</b> member indicates whether the user wants collation. 

Regardless of whether this flag is set, an application can determine from <b>nCopies</b> and <b>PD_COLLATE</b> how many copies to render and whether to print them collated.

If this flag is set and the printer driver does not support multiple copies, the <b>Copies</b> edit control is disabled. Similarly, if this flag is set and the printer driver does not support collation, the <b>Collate</b> check box is disabled.

The <b>dmCopies</b> and <b>dmCollate</b> members of the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure contain the copies and collate information used by the printer driver. If this flag is set and the printer driver supports multiple copies, the	<b>dmCopies</b> member indicates the number of copies requested by the user. If this flag is set and the printer driver supports collation, the <b>dmCollate</b> member of the <b>DEVMODE</b> structure indicates whether the user wants collation. If this flag is not set, the <b>dmCopies</b> member always returns 1, and the <b>dmCollate</b> member is always zero.

In Windows versions prior to Windows Vista, if this flag is not set by the calling application and the <b>dmCopies</b> member of the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure is greater than 1, use that value for the number of copies; otherwise, use the value of the <b>nCopies</b> member of the <b>PRINTDLGEX</b> structure.


</td>
</tr>
<tr>
<td width="40%"><a id="PD_USELARGETEMPLATE"></a><a id="pd_uselargetemplate"></a><dl>
<dt><b>PD_USELARGETEMPLATE</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
Forces the property sheet to use a large template for the <b>General</b> page. The larger template provides more space for applications that specify a custom template for the lower portion of the <b>General</b> page.

</td>
</tr>
</table>

### -field Flags2

Type: <b>DWORD</b>

### -field ExclusionFlags

Type: <b>DWORD</b>

A set of bit flags that can exclude items from the printer driver property pages in the <b>Print</b> property sheet. This value is used only if the <b>PD_EXCLUSIONFLAGS</b> flag is set in the <b>Flags</b> member. Exclusion flags should be used only if the item to be excluded will be included on either the <b>General</b> page or on an application-defined page in the <b>Print</b> property sheet. This member can specify the following flag. 



#### PD_EXCL_COPIESANDCOLLATE

Excludes the <b>Copies</b> and <b>Collate</b> controls from the printer driver property pages in a <b>Print</b> property sheet. This flag should always be set when the application uses the default <b>Copies</b> and <b>Collate</b> controls provided by the lower portion of the <b>General</b> page of the <b>Print</b> property sheet.

### -field nPageRanges

Type: <b>DWORD</b>

On input, set this member to the initial number of page ranges specified in the <b>lpPageRanges</b> array. When the <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> function returns, <b>nPageRanges</b> indicates the number of user-specified page ranges stored in the <b>lpPageRanges</b> array. If the <b>PD_NOPAGENUMS</b> flag is specified, this value is not valid.

### -field nMaxPageRanges

Type: <b>DWORD</b>

The size, in array elements, of the <b>lpPageRanges</b> buffer. This value indicates the maximum number of page ranges that can be stored in the array. If the <b>PD_NOPAGENUMS</b> flag is specified, this value is not valid. If the <b>PD_NOPAGENUMS</b> flag is not specified, this value must be greater than zero.

### -field lpPageRanges

Type: <b>LPPRINTPAGERANGE</b>

Pointer to a buffer containing an array of <a href="/windows/desktop/api/commdlg/ns-commdlg-printpagerange">PRINTPAGERANGE</a> structures. On input, the array contains the initial page ranges to display in the <b>Pages</b> edit control. When the <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> function returns, the array contains the page ranges specified by the user. If the <b>PD_NOPAGENUMS</b> flag is specified, this value is not valid. If the <b>PD_NOPAGENUMS</b> flag is not specified, <b>lpPageRanges</b> must be non-<b>NULL</b>.

### -field nMinPage

Type: <b>DWORD</b>

The minimum value for the page ranges specified in the <b>Pages</b> edit control. If the <b>PD_NOPAGENUMS</b> flag is specified, this value is not valid.

### -field nMaxPage

Type: <b>DWORD</b>

The maximum value for the page ranges specified in the <b>Pages</b> edit control. If the <b>PD_NOPAGENUMS</b> flag is specified, this value is not valid.

### -field nCopies

Type: <b>DWORD</b>

Contains the initial number of copies for the <b>Copies</b> edit control if <b>hDevMode</b> is <b>NULL</b>; otherwise, the <b>dmCopies</b> member of the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure contains the initial value. When <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> returns, <b>nCopies</b> contains the actual number of copies the application must print. This value depends on whether the application or the printer driver is responsible for printing multiple copies. If the <b>PD_USEDEVMODECOPIESANDCOLLATE</b> flag is set in the <b>Flags</b> member, <b>nCopies</b> is always 1 on return, and the printer driver is responsible for printing multiple copies. If the flag is not set, the application is responsible for printing the number of copies specified by <b>nCopies</b>. For more information, see the description of the <b>PD_USEDEVMODECOPIESANDCOLLATE</b> flag.

### -field hInstance

Type: <b>HINSTANCE</b>

If the <b>PD_ENABLEPRINTTEMPLATE</b> flag is set in the <b>Flags</b> member, <b>hInstance</b> is a handle to the application or module instance that contains the dialog box template named by the <b>lpPrintTemplateName</b> member. If the <b>PD_ENABLEPRINTTEMPLATEHANDLE</b> flag is set in the <b>Flags</b> member, <b>hInstance</b> is a handle to a memory object containing a dialog box template. If neither of the template flags is set in the <b>Flags</b> member, <b>hInstance</b> should be <b>NULL</b>.

### -field lpPrintTemplateName

Type: <b>LPCTSTR</b>

The name of the dialog box template resource in the module identified by the <b>hInstance</b> member. This template replaces the default dialog box template in the lower portion of the <b>General</b> page. The default template contains controls similar to those of the <b>Print</b> dialog box. This member is ignored unless the PD_ENABLEPRINTTEMPLATE flag is set in the <b>Flags</b> member.

### -field lpCallback

Type: <b>LPUNKNOWN</b>

A pointer to an application-defined  callback object. 

The object should contain the <a href="/windows/desktop/api/commdlg/nn-commdlg-iprintdialogcallback">IPrintDialogCallback</a> class to receive messages for the child dialog box in the lower portion of the <b>General</b> page. 

The callback object should also contain the <a href="/windows/desktop/api/ocidl/nn-ocidl-iobjectwithsite">IObjectWithSite</a> class to receive a pointer to the <a href="/windows/desktop/api/commdlg/nn-commdlg-iprintdialogservices">IPrintDialogServices</a> interface. The <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> function calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> on the callback object for both <b>IID_IPrintDialogCallback</b> and <b>IID_IObjectWithSite</b> to determine which interfaces are supported. 

If you do not want to retrieve any of the callback information, set <b>lpCallback</b> to <b>NULL</b>.

### -field nPropertyPages

Type: <b>DWORD</b>

The number of property page handles in the 
					<b>lphPropertyPages</b> array.

### -field lphPropertyPages

Type: <b>HPROPSHEETPAGE*</b>

Contains an array of property page handles to add to the <b>Print</b> property sheet. The additional property pages follow the <b>General</b> page. Use the <a href="/windows/desktop/api/prsht/nf-prsht-createpropertysheetpagea">CreatePropertySheetPage</a> function to create these additional pages. When the <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> function returns, all the <b>HPROPSHEETPAGE</b> handles in the <b>lphPropertyPages</b> array have been destroyed. If <b>nPropertyPages</b> is zero, <b>lphPropertyPages</b> should be <b>NULL</b>.

### -field nStartPage

Type: <b>DWORD</b>

The property page that is initially displayed. To display the <b>General</b> page, specify <b>START_PAGE_GENERAL</b>. Otherwise, specify the zero-based index of a property page in the array specified in the <b>lphPropertyPages</b> member. For consistency, it is recommended that the property sheet always be started on the <b>General</b> page.

### -field dwResultAction

Type: <b>DWORD</b>

On input, set this member to zero. If the <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> function returns S_OK, <b>dwResultAction</b> contains the outcome of the dialog. If <b>PrintDlgEx</b> returns an error, this member should be ignored. The <b>dwResultAction</b> member can be one of the following values. 



#### PD_RESULT_APPLY

The user clicked the <b>Apply</b> button and later clicked the <b>Cancel</b> button. This indicates that the user wants to apply the changes made in the property sheet, but does not want to print yet. The <b>PRINTDLGEX</b> structure contains the information specified by the user at the time the <b>Apply</b> button was clicked.



#### PD_RESULT_CANCEL

The user clicked the <b>Cancel</b> button. The information in the <b>PRINTDLGEX</b> structure is unchanged.



#### PD_RESULT_PRINT

The user clicked the <b>Print</b> button. The <b>PRINTDLGEX</b> structure contains the information specified by the user.


##### - ExclusionFlags.PD_EXCL_COPIESANDCOLLATE

Excludes the <b>Copies</b> and <b>Collate</b> controls from the printer driver property pages in a <b>Print</b> property sheet. This flag should always be set when the application uses the default <b>Copies</b> and <b>Collate</b> controls provided by the lower portion of the <b>General</b> page of the <b>Print</b> property sheet.


##### - dwResultAction.PD_RESULT_APPLY

The user clicked the <b>Apply</b> button and later clicked the <b>Cancel</b> button. This indicates that the user wants to apply the changes made in the property sheet, but does not want to print yet. The <b>PRINTDLGEX</b> structure contains the information specified by the user at the time the <b>Apply</b> button was clicked.


##### - dwResultAction.PD_RESULT_CANCEL

The user clicked the <b>Cancel</b> button. The information in the <b>PRINTDLGEX</b> structure is unchanged.


##### - dwResultAction.PD_RESULT_PRINT

The user clicked the <b>Print</b> button. The <b>PRINTDLGEX</b> structure contains the information specified by the user.

## -remarks

If both <b>hDevMode</b> and <b>hDevNames</b> are <b>NULL</b>, <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> initializes the property sheet using the current default printer. To initialize the property sheet for a different printer, use the <b>wDeviceOffset</b> member of the <a href="/windows/desktop/api/commdlg/ns-commdlg-devnames">DEVNAMES</a> structure to specify the name of the printer. 

Note that the <b>dmDeviceName</b> member of the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure also specifies a printer name. However, <b>dmDeviceName</b> is limited to 32 characters, and the <b>wDeviceOffset</b> name is not. If the <b>wDeviceOffset</b> and <b>dmDeviceName</b> names are not the same, <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> initializes the property sheet using the printer specified by <b>wDeviceOffset</b>. 

If the PD_RETURNDEFAULT flag is set and both <b>hDevMode</b> and <b>hDevNames</b> are <b>NULL</b>, <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> uses the <b>hDevNames</b> and <b>hDevMode</b> members to return information about the current default printer without displaying the dialog box.

During the execution of <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a>, the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> and <b>DEVNAMES</b> structures that you specified in the <b>PRINTDLGEX</b> structure may not always contain current data. For this reason, application-specific property pages as well as <a href="/windows/desktop/api/commdlg/nn-commdlg-iprintdialogcallback">IPrintDialogCallback</a> routines for the initial page should use the <a href="/windows/desktop/api/commdlg/nn-commdlg-iprintdialogservices">IPrintDialogServices</a> interface to retrieve information about the state of the current printer. 





> [!NOTE]
> The commdlg.h header defines PRINTDLGEX as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/dlgbox/common-dialog-box-library">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a>



<a href="/windows/desktop/api/commdlg/ns-commdlg-devnames">DEVNAMES</a>



<a href="/windows/desktop/api/commdlg/nn-commdlg-iprintdialogcallback">IPrintDialogCallback</a>



<a href="/windows/desktop/api/commdlg/nn-commdlg-iprintdialogservices">IPrintDialogServices</a>



<a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a>



<b>Reference</b>
