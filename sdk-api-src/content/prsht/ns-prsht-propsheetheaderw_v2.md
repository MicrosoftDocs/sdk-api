---
UID: NS:prsht._PROPSHEETHEADERW_V2
title: PROPSHEETHEADERW_V2 (prsht.h)
description: The PROPSHEETHEADERW_V2 (Unicode) structure defines the frame and pages of a property sheet.
helpviewer_keywords: ["*LPPROPSHEETHEADERW_V2","LPPROPSHEETHEADER","LPPROPSHEETHEADER structure pointer [Windows Controls]","PROPSHEETHEADER","PROPSHEETHEADER structure [Windows Controls]","PROPSHEETHEADERA","PROPSHEETHEADERW","PROPSHEETHEADERW_V2","PSH_AEROWIZARD","PSH_DEFAULT","PSH_HASHELP","PSH_HEADER","PSH_HEADERBITMAP","PSH_MODELESS","PSH_NOAPPLYNOW","PSH_NOCONTEXTHELP","PSH_NOMARGIN","PSH_PROPSHEETPAGE","PSH_PROPTITLE","PSH_RESIZABLE","PSH_RTLREADING","PSH_STRETCHWATERMARK","PSH_USECALLBACK","PSH_USEHBMHEADER","PSH_USEHBMWATERMARK","PSH_USEHICON","PSH_USEHPLWATERMARK","PSH_USEICONID","PSH_USEPAGELANG","PSH_USEPSTARTPAGE","PSH_WATERMARK","PSH_WIZARD","PSH_WIZARD97","PSH_WIZARDCONTEXTHELP","PSH_WIZARDHASFINISH","PSH_WIZARD_LITE","_win32_PROPSHEETHEADER","_win32_PROPSHEETHEADER_cpp","controls.PROPSHEETHEADER","controls._win32_PROPSHEETHEADER","prsht/LPPROPSHEETHEADER","prsht/PROPSHEETHEADER","prsht/PROPSHEETHEADERA","prsht/PROPSHEETHEADERW"]
old-location: controls\PROPSHEETHEADER.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\structures\propsheetheader.htm
ms.date: 08/02/2022
ms.keywords: '*LPPROPSHEETHEADERW_V2, LPPROPSHEETHEADER, LPPROPSHEETHEADER structure pointer [Windows Controls], PROPSHEETHEADER, PROPSHEETHEADER structure [Windows Controls], PROPSHEETHEADERA, PROPSHEETHEADERW, PROPSHEETHEADERW_V2, PSH_AEROWIZARD, PSH_DEFAULT, PSH_HASHELP, PSH_HEADER, PSH_HEADERBITMAP, PSH_MODELESS, PSH_NOAPPLYNOW, PSH_NOCONTEXTHELP, PSH_NOMARGIN, PSH_PROPSHEETPAGE, PSH_PROPTITLE, PSH_RESIZABLE, PSH_RTLREADING, PSH_STRETCHWATERMARK, PSH_USECALLBACK, PSH_USEHBMHEADER, PSH_USEHBMWATERMARK, PSH_USEHICON, PSH_USEHPLWATERMARK, PSH_USEICONID, PSH_USEPAGELANG, PSH_USEPSTARTPAGE, PSH_WATERMARK, PSH_WIZARD, PSH_WIZARD97, PSH_WIZARDCONTEXTHELP, PSH_WIZARDHASFINISH, PSH_WIZARD_LITE, _win32_PROPSHEETHEADER, _win32_PROPSHEETHEADER_cpp, controls.PROPSHEETHEADER, controls._win32_PROPSHEETHEADER, prsht/LPPROPSHEETHEADER, prsht/PROPSHEETHEADER, prsht/PROPSHEETHEADERA, prsht/PROPSHEETHEADERW'
req.header: prsht.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PROPSHEETHEADERW (Unicode) and PROPSHEETHEADERA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PROPSHEETHEADERW_V2, *LPPROPSHEETHEADERW_V2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROPSHEETHEADERW_V2
 - prsht/_PROPSHEETHEADERW_V2
 - LPPROPSHEETHEADERW_V2
 - prsht/LPPROPSHEETHEADERW_V2
 - PROPSHEETHEADERW_V2
 - prsht/PROPSHEETHEADERW_V2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Prsht.h
api_name:
 - PROPSHEETHEADER
 - PROPSHEETHEADERA
 - PROPSHEETHEADERW
---

# PROPSHEETHEADERW_V2 structure


## -description

Defines the frame and pages of a property sheet.

> [!NOTE]
> This structure is not intended to be used directly in your code. Instead, use the [PROPSHEETHEADER](/windows/win32/controls/pss-propsheetheader) structure.

## -struct-fields

### -field DUMMYUNIONNAME4

### -field DUMMYUNIONNAME4.hbmWatermark

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HBITMAP</a></b>


<a href="/windows/desktop/Controls/common-control-versions">Version 5.80</a> or later. Handle to the watermark bitmap. If the <b>dwFlags</b> member does not include PSH_USEHBMWATERMARK, this member is ignored.

### -field DUMMYUNIONNAME4.pszbmWatermark

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>


<a href="/windows/desktop/Controls/common-control-versions">Version 5.80</a> or later. Bitmap resource to use as the watermark. This member can specify either the identifier of the bitmap resource or the address of the string that specifies the name of the bitmap resource. If the <b>dwFlags</b> member includes PSH_USEHBMWATERMARK, this member is ignored.

### -field hplWatermark

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HPALETTE</a></b>


<a href="/windows/desktop/Controls/common-control-versions">Version 5.80</a> or later. <b>HPALETTE</b> structure used for drawing the watermark bitmap and/or header bitmap. If the <b>dwFlags</b> member does not include PSH_USEHPLWATERMARK, this member is ignored.

### -field DUMMYUNIONNAME5

### -field DUMMYUNIONNAME5.hbmHeader

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HBITMAP</a></b>


<a href="/windows/desktop/Controls/common-control-versions">Version 5.80</a> or later. Handle to the header bitmap. If the <b>dwFlags</b> member does not include PSH_USEHBMHEADER, this member is ignored.

### -field DUMMYUNIONNAME5.pszbmHeader

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>


<a href="/windows/desktop/Controls/common-control-versions">Version 5.80</a> or later. Bitmap resource to use as the header. This member can specify either the identifier of the bitmap resource or the address of the string that specifies the name of the bitmap resource. If the <b>dwFlags</b> member includes PSH_USEHBMHEADER, this member is ignored.


#### - dwFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Flags that indicate which options to use when creating the property sheet page. This member can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PSH_DEFAULT"></a><a id="psh_default"></a><dl>
<dt><b>PSH_DEFAULT</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Uses the default meaning for all structure members, and creates a normal property sheet. This flag has a value of zero and is not combined with other flags.

</td>
</tr>
<tr>
<td width="40%"><a id="PSH_AEROWIZARD"></a><a id="psh_aerowizard"></a><dl>
<dt><b>PSH_AEROWIZARD</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.00</a> and <b>Windows Vista.</b>. Creates a wizard property sheet that uses the newer Aero style. The PSH_WIZARD flag must also be set. The single-threaded apartment (STA) model must be used.

</td>
</tr>
<tr>
<td width="40%"><a id="PSH_HASHELP"></a><a id="psh_hashelp"></a><dl>
<dt><b>PSH_HASHELP</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
Permits property sheet pages to display a <b>Help</b> button. You must also set the PSP_HASHELP flag in the page's <a href="/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2">PROPSHEETPAGE</a> structure when the page is created. If any of the initial property sheet pages enable a <b>Help</b> button, PSH_HASHELP will be set automatically. If none of the initial pages enable a <b>Help</b> button, you must explicitly set PSH_HASHELP if you want to have <b>Help</b> buttons on any pages that might be added later. This flag is not supported in conjunction with PSH_AEROWIZARD.

</td>
</tr>
<tr>
<td width="40%"><a id="PSH_HEADER"></a><a id="psh_header"></a><dl>
<dt><b>PSH_HEADER</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 5.80</a> and later. Indicates that a header bitmap will be used with a Wizard97 wizard. You must also set the PSH_WIZARD97 flag. The header bitmap is obtained from the <b>pszbmHeader</b> member, unless the PSH_USEHBMHEADER flag is also set. In that case, the header bitmap is obtained from the <b>hbmHeader</b> member. This flag is not supported in conjunction with PSH_AEROWIZARD.

</td>
</tr>
<tr>
<td width="40%"><a id="PSH_HEADERBITMAP"></a><a id="psh_headerbitmap"></a><dl>
<dt><b>PSH_HEADERBITMAP</b></dt>
<dt>0x08000000</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.00</a> and <b>Windows Vista.</b>.The <b>pszbmHeader</b> member specifies a bitmap that is displayed in the header area. Must be used in combination with PSH_AEROWIZARD.

</td>
</tr>
<tr>
<td width="40%"><a id="PSH_MODELESS"></a><a id="psh_modeless"></a><dl>
<dt><b>PSH_MODELESS</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
Causes the <a href="/windows/desktop/api/prsht/nf-prsht-propertysheeta">PropertySheet</a> function to create the property sheet as a modeless dialog box instead of as a modal dialog box. When this flag is set, <b>PropertySheet</b> returns immediately after the dialog box is created, and the return value from <b>PropertySheet</b> is the window handle to the property sheet dialog box. This flag is not supported in conjunction with PSH_AEROWIZARD.

</td>
</tr>
<tr>
<td width="40%"><a id="PSH_NOAPPLYNOW"></a><a id="psh_noapplynow"></a><dl>
<dt><b>PSH_NOAPPLYNOW</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Removes the <b>Apply</b> button. This flag is not supported in conjunction with PSH_AEROWIZARD.

</td>
</tr>
<tr>
<td width="40%"><a id="PSH_NOCONTEXTHELP"></a><a id="psh_nocontexthelp"></a><dl>
<dt><b>PSH_NOCONTEXTHELP</b></dt>
<dt>0x02000000</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 5.80</a> and later. Removes the context-sensitive <b>Help</b> button ("?"), which is usually present on the caption bar of property sheets. This flag is not valid for wizards. See <a href="/windows/desktop/Controls/property-sheets">About Property Sheets</a> for a discussion of how to remove the caption bar <b>Help</b> button for earlier versions of the common controls. This flag is not supported in conjunction with PSH_AEROWIZARD.

</td>
</tr>
<tr>
<td width="40%"><a id="PSH_NOMARGIN"></a><a id="psh_nomargin"></a><dl>
<dt><b>PSH_NOMARGIN</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.00</a> and <b>Windows Vista.</b>. Specifies that no margin is inserted between the page and the frame. Must be used in combination with PSH_AEROWIZARD.

</td>
</tr>
<tr>
<td width="40%"><a id="PSH_PROPSHEETPAGE"></a><a id="psh_propsheetpage"></a><dl>
<dt><b>PSH_PROPSHEETPAGE</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Uses the <b>ppsp</b> member and ignores the <b>phpage</b> member when creating the pages for the property sheet.

</td>
</tr>
<tr>
<td width="40%"><a id="PSH_PROPTITLE"></a><a id="psh_proptitle"></a><dl>
<dt><b>PSH_PROPTITLE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Displays a title in the title bar of the property sheet. The title takes the appropriate form for the Windows version. In more recent versions of Windows, the title is the string specified by the <b>pszCaption</b> followed by the string "Properties". In older versions of Windows, the title is the string "Properties for", followed by the string specified by the <b>pszCaption</b> member. This flag is not supported for wizards.

</td>
</tr>
<tr>
<td width="40%"><a id="PSH_RESIZABLE"></a><a id="psh_resizable"></a><dl>
<dt><b>PSH_RESIZABLE</b></dt>
<dt>0x04000000</dt>
</dl>
</td>
<td width="60%">
Allows the wizard to be resized by the user. Maximize and minimize buttons appear in the wizard's frame and the frame is sizable. To use this flag, you must also set PSH_AEROWIZARD.

</td>
</tr>
<tr>
<td width="40%"><a id="PSH_RTLREADING"></a><a id="psh_rtlreading"></a><dl>
<dt><b>PSH_RTLREADING</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
Displays the title of the property sheet (<b>pszCaption</b>) using right-to-left (RTL) reading order for Hebrew or Arabic languages. If this flag is not specified, the title is displayed in left-to-right (LTR) reading order.  

</td>
</tr>
<tr>
<td width="40%"><a id="PSH_STRETCHWATERMARK"></a><a id="psh_stretchwatermark"></a><dl>
<dt><b>PSH_STRETCHWATERMARK</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
Stretches the watermark in Internet Explorer 4.0-compatible Wizard97-style wizards. This flag is not supported in conjunction with PSH_AEROWIZARD.
                        

<div class="alert"><b>Note</b>   This style flag is only included to provide backward compatibility for certain applications. Its use is not recommended, and it is only supported by common controls <a href="/windows/desktop/Controls/common-control-versions">versions 4.0 and 4.01</a>. With common controls version 5.80 and later, this flag is ignored.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="PSH_USECALLBACK"></a><a id="psh_usecallback"></a><dl>
<dt><b>PSH_USECALLBACK</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Calls the function specified by the <b>pfnCallback</b> member when initializing the property sheet defined by this structure.

</td>
</tr>
<tr>
<td width="40%"><a id="PSH_USEHBMHEADER"></a><a id="psh_usehbmheader"></a><dl>
<dt><b>PSH_USEHBMHEADER</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 5.80</a> or later. Obtains the header bitmap from the <b>hbmHeader</b> member instead of the <b>pszbmHeader</b> member. You must also set either the PSH_AEROWIZARD flag or the PSH_WIZARD97 flag together with the PSH_HEADER flag.

</td>
</tr>
<tr>
<td width="40%"><a id="PSH_USEHBMWATERMARK"></a><a id="psh_usehbmwatermark"></a><dl>
<dt><b>PSH_USEHBMWATERMARK</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 5.80</a> or later. Obtains the watermark bitmap from the <b>hbmWatermark</b> member instead of the <b>pszbmWatermark</b> member. You must also set PSH_WIZARD97 and PSH_WATERMARK. This flag is not supported in conjunction with PSH_AEROWIZARD.

</td>
</tr>
<tr>
<td width="40%"><a id="PSH_USEHICON"></a><a id="psh_usehicon"></a><dl>
<dt><b>PSH_USEHICON</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Uses <b>hIcon</b> as the small icon in the title bar of the property sheet dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="PSH_USEHPLWATERMARK"></a><a id="psh_usehplwatermark"></a><dl>
<dt><b>PSH_USEHPLWATERMARK</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 5.80</a> or later. Uses the <b>HPALETTE</b> structure pointed to by the <b>hplWatermark</b> member instead of the default palette to draw the watermark bitmap and/or header bitmap for a Wizard97 wizard. You must also set PSH_WIZARD97, and PSH_WATERMARK or PSH_HEADER. This flag is not supported in conjunction with PSH_AEROWIZARD.

</td>
</tr>
<tr>
<td width="40%"><a id="PSH_USEICONID"></a><a id="psh_useiconid"></a><dl>
<dt><b>PSH_USEICONID</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Uses <b>pszIcon</b> as the name of the icon resource to load and use as the small icon in the title bar of the property sheet dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="PSH_USEPAGELANG"></a><a id="psh_usepagelang"></a><dl>
<dt><b>PSH_USEPAGELANG</b></dt>
<dt>0x00200000</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 5.80</a> or later. Specifies that the language for the property sheet will be taken from the first page's resource. That page must be specified by resource identifier.

</td>
</tr>
<tr>
<td width="40%"><a id="PSH_USEPSTARTPAGE"></a><a id="psh_usepstartpage"></a><dl>
<dt><b>PSH_USEPSTARTPAGE</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Uses the <b>pStartPage</b> member instead of the <b>nStartPage</b> member when displaying the initial page of the property sheet.

</td>
</tr>
<tr>
<td width="40%"><a id="PSH_WATERMARK"></a><a id="psh_watermark"></a><dl>
<dt><b>PSH_WATERMARK</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 5.80</a> or later. Specifies that a watermark bitmap will be used with a Wizard97 wizard on pages that have the PSP_HIDEHEADER style. You must also set the PSH_WIZARD97 flag. The watermark bitmap is obtained from the <b>pszbmWatermark</b> member, unless PSH_USEHBMWATERMARK is set. In that case, the header bitmap is obtained from the <b>hbmWatermark</b> member. This flag is not supported in conjunction with PSH_AEROWIZARD.

</td>
</tr>
<tr>
<td width="40%"><a id="PSH_WIZARD"></a><a id="psh_wizard"></a><dl>
<dt><b>PSH_WIZARD</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Creates a wizard property sheet. When using PSH_AEROWIZARD, you must also set this flag.

</td>
</tr>
<tr>
<td width="40%"><a id="PSH_WIZARD97"></a><a id="psh_wizard97"></a><dl>
<dt><b>PSH_WIZARD97</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 5.80</a> or later. Creates a Wizard97-style property sheet, which supports bitmaps in the header of interior pages and on the left side of exterior pages. This flag is not supported in conjunction with PSH_AEROWIZARD.

</td>
</tr>
<tr>
<td width="40%"><a id="PSH_WIZARDCONTEXTHELP"></a><a id="psh_wizardcontexthelp"></a><dl>
<dt><b>PSH_WIZARDCONTEXTHELP</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
Adds a context-sensitive <b>Help</b> button ("?"), which is usually absent from the caption bar of a wizard. This flag is not valid for regular property sheets. This flag is not supported in conjunction with PSH_AEROWIZARD.

</td>
</tr>
<tr>
<td width="40%"><a id="PSH_WIZARDHASFINISH"></a><a id="psh_wizardhasfinish"></a><dl>
<dt><b>PSH_WIZARDHASFINISH</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Always displays the <b>Finish</b> button on the wizard. You must also set either PSH_WIZARD, PSH_WIZARD97, or PSH_AEROWIZARD.

</td>
</tr>
<tr>
<td width="40%"><a id="PSH_WIZARD_LITE"></a><a id="psh_wizard_lite"></a><dl>
<dt><b>PSH_WIZARD_LITE</b></dt>
<dt>0x00400000</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 5.80</a> or later. Uses the Wizard-lite style. This style is similar in appearance to PSH_WIZARD97, but it is implemented much like PSH_WIZARD. There are few restrictions on how the pages are formatted. For instance, there are no enforced borders, and the PSH_WIZARD_LITE style does not paint the watermark and header bitmaps for you the way Wizard97 does. This flag is not supported in conjunction with PSH_AEROWIZARD.

</td>
</tr>
</table>
 


#### - dwSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Size, in bytes, of this structure. The property sheet manager uses this member to determine which version of the <b>PROPSHEETHEADER</b> structure you are using. For more information, see the Remarks.


#### - hIcon

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HICON</a></b>

Handle to the icon to use as the small icon in the title bar of the property sheet dialog box. If the <b>dwFlags</b>  member does not include PSH_USEHICON, this member is ignored. This member is declared as a union with <b>pszIcon</b>.


#### - hInstance

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HINSTANCE</a></b>

Handle to the instance from which to load the icon or title string resource. If the <b>pszIcon</b> or <b>pszCaption</b> member identifies a resource to load, this member must be specified.


#### - hwndParent

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the property sheet's owner window.


#### - nPages

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of elements in the <b>phpage</b> array.


#### - nStartPage

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Zero-based index of the initial page that appears when the property sheet dialog box is created. This member is declared as a union with <b>pStartPage</b>.


#### - pStartPage

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

Name of the initial page that appears when the property sheet dialog box is created. This member can specify either the identifier of a string resource or the address of a string that specifies the name. This member is declared as a union with <b>nStartPage</b>.


#### - pfnCallback

Type: <b>PFNPROPSHEETCALLBACK</b>

Pointer to an application-defined callback function that is called when the property sheet is initialized. For more information about the callback function, see the description of the <a href="/windows/desktop/api/prsht/nc-prsht-pfnpropsheetcallback">PropSheetProc</a> function. If the 
<b>dwFlags</b> member does not include PSH_USECALLBACK, this member is ignored.


#### - phpage

Type: <b>HPROPSHEETPAGE*</b>

Pointer to an array of handles to the property sheet pages. Each handle must have been created by a previous call to the <a href="/windows/desktop/api/prsht/nf-prsht-createpropertysheetpagea">CreatePropertySheetPage</a> function. If the <b>dwFlags</b> member includes PSH_PROPSHEETPAGE, <b>phpage</b> is ignored and should be set to <b>NULL</b>. When the <a href="/windows/desktop/api/prsht/nf-prsht-propertysheeta">PropertySheet</a> function returns, any HPROPSHEETPAGE handles in the <b>phpage</b> array will have been destroyed. This member is declared as a union with <b>ppsp</b>.


#### - ppsp

Type: <b>LPCPROPSHEETPAGE</b>

Pointer to an array of <a href="/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2">PROPSHEETPAGE</a> structures that define the pages in the property sheet. If the <b>dwFlags</b> member does not include PSH_PROPSHEETPAGE, this member is ignored. Note that the <b>PROPSHEETPAGE</b> structure is variable in size. Applications that parse the array pointed to by <b>ppsp</b> must take the size of each page into account. This member is declared as a union with <b>phpage</b>.


#### - pszCaption

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

Title of the property sheet dialog box. This member can specify either the identifier of a string resource or the address of a string that specifies the title. If the <b>dwFlags</b> member includes PSH_PROPTITLE, the string "Properties for" is inserted at the beginning of the title. This field is ignored for Wizard97 wizards. For Aero wizards, the string alone is used for the caption, regardless of whether the PSH_PROPTITLE flag is set.


#### - pszIcon

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

Icon resource to use as the small icon in the title bar of the property sheet dialog box. This member can specify either the identifier of the icon resource or the address of the string that specifies the name of the icon resource. If the <b>dwFlags</b> member does not include PSH_USEICONID, this member is ignored. This member is declared as a union with <b>hIcon</b>.

## -remarks

If the user chooses a setting such as Large Fonts, which enlarges the dialog box, the watermark that is painted on the start and finish pages will be enlarged as well. The size and position of the original bitmap will remain the same. The additional area will be filled with the color of the pixel in the upper-left corner of the bitmap.

Note that several members of this structure are only supported for Comctl32.dll versions 4.71 and later. You can enable these members by including one of the following in your header. 

                

<code>#define _WIN32_IE 0x0400 // For version 4.71</code>

or
                

<code>#define _WIN32_IE 0x0500 // For version 5.80</code>

However, you must initialize the structure with its size. If you use the size of the currently defined structure, the application may not run with the earlier versions of Comctl32.dll, which expect a smaller structure. This includes all systems with Windows 95 or Microsoft Windows NT 4.0 that do not have Internet Explorer 4.0 or later installed. You can run your application on pre-4.71 versions of Comctl32.dll by defining the appropriate <a href="/windows/desktop/Controls/common-controls-intro">version number</a>. However, this may cause problems if your application also needs to run on systems with more recent versions.

You can remain compatible with all Comctl32.dll versions by using the current header files and setting the size of the <b>PROPSHEETHEADER</b> structure appropriately. Before you initialize the structure, use the <a href="/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc">DllGetVersion</a> function to determine which Comctl32.dll version is installed on the system. If it is version 4.71 or greater, use

<code>psh.dwSize = sizeof(PROPSHEETHEADER);</code>

to initialize the <b>dwSize</b> member. For earlier versions, the size of the pre-4.71 structure is given by the PROPSHEETHEADER_V1_SIZE constant. Use

<code>psh.dwSize = PROPSHEETHEADER_V1_SIZE;</code>

The PSH_WIZARD, PSH_WIZARD97, and PSH_WIZARD_LITE styles are mutually incompatible. Only one of these style flags should be set. PSH_AEROWIZARD should be combined with PSH_WIZARD.