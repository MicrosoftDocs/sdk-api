---
UID: NS:prsht._PROPSHEETPAGEA_V2
title: PROPSHEETPAGEA_V2 (prsht.h)
description: The PROPSHEETPAGEA_V2 (ANSI) structure defines a page in a property sheet.
helpviewer_keywords: ["*LPPROPSHEETPAGEA_V2","LPPROPSHEETPAGE","LPPROPSHEETPAGE structure pointer [Windows Controls]","PROPSHEETPAGE","PROPSHEETPAGE structure [Windows Controls]","PROPSHEETPAGEA","PROPSHEETPAGEA_V2","PROPSHEETPAGEW","PSP_DEFAULT","PSP_DLGINDIRECT","PSP_HASHELP","PSP_HIDEHEADER","PSP_PREMATURE","PSP_RTLREADING","PSP_USECALLBACK","PSP_USEFUSIONCONTEXT","PSP_USEHEADERSUBTITLE","PSP_USEHEADERTITLE","PSP_USEHICON","PSP_USEICONID","PSP_USEREFPARENT","PSP_USETITLE","_win32_PROPSHEETPAGE_str","_win32_PROPSHEETPAGE_str_cpp","controls.PROPSHEETPAGE","controls._win32_PROPSHEETPAGE_str","prsht/LPPROPSHEETPAGE","prsht/PROPSHEETPAGE","prsht/PROPSHEETPAGEA","prsht/PROPSHEETPAGEW"]
old-location: controls\PROPSHEETPAGE.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\structures\propsheetpage.htm
ms.date: 08/02/2022
ms.keywords: '*LPPROPSHEETPAGEA_V2, LPPROPSHEETPAGE, LPPROPSHEETPAGE structure pointer [Windows Controls], PROPSHEETPAGE, PROPSHEETPAGE structure [Windows Controls], PROPSHEETPAGEA, PROPSHEETPAGEA_V2, PROPSHEETPAGEW, PSP_DEFAULT, PSP_DLGINDIRECT, PSP_HASHELP, PSP_HIDEHEADER, PSP_PREMATURE, PSP_RTLREADING, PSP_USECALLBACK, PSP_USEFUSIONCONTEXT, PSP_USEHEADERSUBTITLE, PSP_USEHEADERTITLE, PSP_USEHICON, PSP_USEICONID, PSP_USEREFPARENT, PSP_USETITLE, _win32_PROPSHEETPAGE_str, _win32_PROPSHEETPAGE_str_cpp, controls.PROPSHEETPAGE, controls._win32_PROPSHEETPAGE_str, prsht/LPPROPSHEETPAGE, prsht/PROPSHEETPAGE, prsht/PROPSHEETPAGEA, prsht/PROPSHEETPAGEW'
req.header: prsht.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PROPSHEETPAGEW (Unicode) and PROPSHEETPAGEA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PROPSHEETPAGEA_V2, *LPPROPSHEETPAGEA_V2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROPSHEETPAGEA_V2
 - prsht/_PROPSHEETPAGEA_V2
 - LPPROPSHEETPAGEA_V2
 - prsht/LPPROPSHEETPAGEA_V2
 - PROPSHEETPAGEA_V2
 - prsht/PROPSHEETPAGEA_V2
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
 - PROPSHEETPAGE
 - PROPSHEETPAGEA
 - PROPSHEETPAGEW
---

# PROPSHEETPAGEA_V2 structure


## -description

Defines a page in a property sheet.

> [!NOTE]
> This structure is not intended to be used directly in your code. Instead, use the [PROPSHEETPAGE](/windows/win32/controls/pss-propsheetpage) structure.

## -struct-fields

### -field pszHeaderTitle

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>


<a href="/windows/desktop/Controls/common-control-versions">Version 5.80</a> or later. Title of the header area. To use this member under the Wizard97-style wizard, you must also do the following: 
					
                    

<ul>
<li>Set the PSP_USEHEADERTITLE flag in the <b>dwFlags</b> member.</li>
<li>Set the PSH_WIZARD97 flag in the <b>dwFlags</b> member of the page's <a href="/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PROPSHEETHEADER</a> structure.</li>
<li>Make sure that the PSP_HIDEHEADER flag in the <b>dwFlags</b> member is not set.</li>
</ul>

### -field pszHeaderSubTitle

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>


<a href="/windows/desktop/Controls/common-control-versions">Version 5.80</a>. Subtitle of the header area. To use this member, you must do the following:

					

<ul>
<li>Set the PSP_USEHEADERSUBTITLE flag in the <b>dwFlags</b> member.</li>
<li>Set the PSH_WIZARD97 flag in the <b>dwFlags</b> member of the page's <a href="/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PROPSHEETHEADER</a> structure.</li>
<li>Make sure that the PSP_HIDEHEADER flag in the <b>dwFlags</b> member is not set.</li>
</ul>
<div class="alert"><b>Note</b>  This member is ignored when using the Aero-style wizard (<a href="/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PSH_AEROWIZARD</a>).</div>
<div> </div>

#### - dwFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Flags that indicate which options to use when creating the property sheet page. This member can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PSP_DEFAULT"></a><a id="psp_default"></a><dl>
<dt><b>PSP_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Uses the default meaning for all structure members. This flag is not supported when using the Aero-style wizard (<a href="/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PSH_AEROWIZARD</a>).

</td>
</tr>
<tr>
<td width="40%"><a id="PSP_DLGINDIRECT"></a><a id="psp_dlgindirect"></a><dl>
<dt><b>PSP_DLGINDIRECT</b></dt>
</dl>
</td>
<td width="60%">
Creates the page from the dialog box template in memory pointed to by the <b>pResource</b> member. The <a href="/windows/desktop/api/prsht/nf-prsht-propertysheeta">PropertySheet</a> function assumes that the template that is in memory is not write-protected. A read-only template will cause an exception in some versions of Windows.

</td>
</tr>
<tr>
<td width="40%"><a id="PSP_HASHELP"></a><a id="psp_hashelp"></a><dl>
<dt><b>PSP_HASHELP</b></dt>
</dl>
</td>
<td width="60%">
Enables the property sheet <b>Help</b> button when the page is active. This flag is not supported when using the Aero-style wizard (<a href="/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PSH_AEROWIZARD</a>).

</td>
</tr>
<tr>
<td width="40%"><a id="PSP_HIDEHEADER"></a><a id="psp_hideheader"></a><dl>
<dt><b>PSP_HIDEHEADER</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 5.80</a> and later. Causes the wizard property sheet to hide the header area when the page is selected. If a watermark has been provided, it will be painted on the left side of the page. This flag should be set for welcome and completion pages, and omitted for interior pages. This flag is not supported when using the Aero-style wizard (<a href="/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PSH_AEROWIZARD</a>).

</td>
</tr>
<tr>
<td width="40%"><a id="PSP_PREMATURE"></a><a id="psp_premature"></a><dl>
<dt><b>PSP_PREMATURE</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 4.71</a> or later. Causes the page to be created when the property sheet is created. If this flag is not specified, the page will not be created until it is selected the first time. This flag is not supported when using the Aero-style wizard (<a href="/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PSH_AEROWIZARD</a>).

</td>
</tr>
<tr>
<td width="40%"><a id="PSP_RTLREADING"></a><a id="psp_rtlreading"></a><dl>
<dt><b>PSP_RTLREADING</b></dt>
</dl>
</td>
<td width="60%">
Reverses the direction in which <b>pszTitle</b> is displayed. Normal windows display all text, including <b>pszTitle</b>, left-to-right (LTR). For languages such as Hebrew or Arabic that read right-to-left (RTL), a window can be <i>mirrored</i> and all text will be displayed RTL. If PSP_RTLREADING is set, <b>pszTitle</b> will instead read RTL in a normal parent window, and LTR in a mirrored parent window.

</td>
</tr>
<tr>
<td width="40%"><a id="PSP_USECALLBACK"></a><a id="psp_usecallback"></a><dl>
<dt><b>PSP_USECALLBACK</b></dt>
</dl>
</td>
<td width="60%">
Calls the function specified by the <b>pfnCallback</b> member when creating or destroying the property sheet page defined by this structure.

</td>
</tr>
<tr>
<td width="40%"><a id="PSP_USEFUSIONCONTEXT"></a><a id="psp_usefusioncontext"></a><dl>
<dt><b>PSP_USEFUSIONCONTEXT</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.0</a> and later. Use an activation context. To use an activation context, you must set this flag and assign the activation context handle to <b>hActCtx</b>. See the Remarks.

</td>
</tr>
<tr>
<td width="40%"><a id="PSP_USEHEADERSUBTITLE"></a><a id="psp_useheadersubtitle"></a><dl>
<dt><b>PSP_USEHEADERSUBTITLE</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 5.80</a> or later. Displays the string pointed to by the <b>pszHeaderSubTitle</b> member as the subtitle of the header area of a Wizard97 page. To use this flag, you must also set the PSH_WIZARD97 flag in the <b>dwFlags</b> member of the associated <a href="/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PROPSHEETHEADER</a> structure. The PSP_USEHEADERSUBTITLE flag is ignored if PSP_HIDEHEADER is set. In Aero-style wizards, the title appears near the top of the client area.

</td>
</tr>
<tr>
<td width="40%"><a id="PSP_USEHEADERTITLE"></a><a id="psp_useheadertitle"></a><dl>
<dt><b>PSP_USEHEADERTITLE</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 5.80</a> or later. Displays the string pointed to by the <b>pszHeaderTitle</b> member as the title in the header of a Wizard97 interior page. You must also set the PSH_WIZARD97 flag in the <b>dwFlags</b> member of the associated <a href="/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PROPSHEETHEADER</a> structure. The PSP_USEHEADERTITLE flag is ignored if PSP_HIDEHEADER is set. This flag is not supported when using the Aero-style wizard (<a href="/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PSH_AEROWIZARD</a>).

</td>
</tr>
<tr>
<td width="40%"><a id="PSP_USEHICON"></a><a id="psp_usehicon"></a><dl>
<dt><b>PSP_USEHICON</b></dt>
</dl>
</td>
<td width="60%">
Uses <b>hIcon</b> as the small icon on the tab for the page. This flag is not supported when using the Aero-style wizard (<a href="/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PSH_AEROWIZARD</a>).

</td>
</tr>
<tr>
<td width="40%"><a id="PSP_USEICONID"></a><a id="psp_useiconid"></a><dl>
<dt><b>PSP_USEICONID</b></dt>
</dl>
</td>
<td width="60%">
Uses <b>pszIcon</b> as the name of the icon resource to load and use as the small icon on the tab for the page. This flag is not supported when using the Aero-style wizard (<a href="/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PSH_AEROWIZARD</a>).

</td>
</tr>
<tr>
<td width="40%"><a id="PSP_USEREFPARENT"></a><a id="psp_userefparent"></a><dl>
<dt><b>PSP_USEREFPARENT</b></dt>
</dl>
</td>
<td width="60%">
Maintains the reference count specified by the <b>pcRefParent</b> member for the lifetime of the property sheet page created from this structure.

</td>
</tr>
<tr>
<td width="40%"><a id="PSP_USETITLE"></a><a id="psp_usetitle"></a><dl>
<dt><b>PSP_USETITLE</b></dt>
</dl>
</td>
<td width="60%">
Uses the <b>pszTitle</b> member as the title of the property sheet dialog box instead of the title stored in the dialog box template. This flag is not supported when using the Aero-style wizard (<a href="/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PSH_AEROWIZARD</a>).

</td>
</tr>
</table>
 


#### - dwSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Size, in bytes, of this structure. 


#### - hActCtx

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HANDLE</a></b>


<a href="/windows/desktop/Controls/common-control-versions">Version 6.0</a> or later. An activation context handle. Set this member to the handle that is returned when you create the activation context with <a href="/windows/desktop/api/winbase/nf-winbase-createactctxa">CreateActCtx</a>. The system will activate this context before creating the dialog box. You do not need to use this member if you use a global manifest. See the Remarks.


#### - hIcon

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HICON</a></b>

Handle to the icon to use as the icon in the tab of the page. If the <b>dwFlags</b> member does not include PSP_USEHICON, this member is ignored. This member is declared as a union with <b>pszIcon</b>.


#### - hInstance

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HINSTANCE</a></b>

Handle to the instance from which to load an icon or string resource. If the <b>pszIcon</b>, <b>pszTitle</b>, <b>pszHeaderTitle</b>, or <b>pszHeaderSubTitle</b> member identifies a resource to load, <b>hInstance</b> must be specified.


#### - lParam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

When the page is created, a copy of the page's <b>PROPSHEETPAGE</b> structure is passed to the dialog box procedure with a <a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a> message. The <b>lParam</b> member is provided to allow you to pass application-specific information to the dialog box procedure. It has no effect on the page itself. For more information, see <a href="/windows/desktop/Controls/property-sheets">Property Sheet Creation</a>.


#### - pResource

Type: <b>LPCDLGTEMPLATE</b>

Pointer to a dialog box template in memory. The <a href="/windows/desktop/api/prsht/nf-prsht-propertysheeta">PropertySheet</a> function assumes that the template is not write-protected. A read-only template will cause an exception in some versions of Windows. To use this member, you must set the PSP_DLGINDIRECT flag in the <b>dwFlags</b> member. This member is declared as a union with <b>pszTemplate</b>.


#### - pcRefParent

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

Pointer to the reference count value. To use this member, you must set the PSP_USEREFPARENT flag in the <b>dwFlags</b> member.



<div class="alert"><b>Note</b>   When a property sheet page is created, the value pointed to by <b>pcRefParent</b> is incremented. You create a property sheet page implicitly by setting the PSH_PROPSHEETPAGE flag in the <b>dwFlags</b> member of <a href="/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PROPSHEETHEADER</a> and calling the <a href="/windows/desktop/api/prsht/nf-prsht-propertysheeta">PropertySheet</a> function. You can do it explicitly by using the <a href="/windows/desktop/api/prsht/nf-prsht-createpropertysheetpagea">CreatePropertySheetPage</a> function. When a property sheet page is destroyed, the value pointed to by the <b>pcRefParent</b> member is decremented. This takes place automatically when the property sheet is destroyed. You can explicitly destroy a property sheet page by using the <a href="/windows/desktop/api/prsht/nf-prsht-destroypropertysheetpage">DestroyPropertySheetPage</a> function.</div>
<div> </div>

#### - pfnCallback

Type: <b>LPFNPSPCALLBACK</b>

Pointer to an application-defined callback function that is called when the page is created and when it is about to be destroyed. For more information about the callback function, see <a href="/windows/desktop/api/prsht/nc-prsht-lpfnpspcallbacka">PropSheetPageProc</a>. To use this member, you must set the PSP_USECALLBACK flag in the <b>dwFlags</b> member.


#### - pfnDlgProc

Type: <b>DLGPROC</b>

Pointer to the dialog box procedure for the page. Because the pages are created as modeless dialog boxes, the dialog box procedure must not call the <a href="/windows/desktop/api/winuser/nf-winuser-enddialog">EndDialog</a> function.


#### - pszIcon

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

Icon resource to use as the icon in the tab of the page. This member can specify either the identifier of the icon resource or the address of the string that specifies the name of the icon resource. To use this member, you must set the PSP_USEICONID flag in the <b>dwFlags</b> member. This member is declared as a union with <b>hIcon</b>.


#### - pszTemplate

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

Dialog box template to use to create the page. This member can specify either the resource identifier of the template or the address of a string that specifies the name of the template. If the PSP_DLGINDIRECT flag in the <b>dwFlags</b> member is set, <b>pszTemplate</b> is ignored. This member is declared as a union with <b>pResource</b>.


#### - pszTitle

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

Title of the property sheet dialog box. This title overrides the title specified in the dialog box template. This member can specify either the identifier of a string resource or the address of a string that specifies the title. To use this member, you must set the PSP_USETITLE flag in the <b>dwFlags</b> member.

## -remarks

Comctl32.dll version 6 and later are not redistributable. To use Comctl32.dll version 6 or later, specify the .dll file in a manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.