---
UID: NC:prsht.LPFNPSPCALLBACKW
title: LPFNPSPCALLBACKW (prsht.h)
description: Specifies an application-defined callback function that a property sheet calls when a page is created and when it is about to be destroyed. An application can use this function to perform initialization and cleanup operations for the page. (Unicode)
helpviewer_keywords: ["LPFNPSPCALLBACK","LPFNPSPCALLBACK callback","LPFNPSPCALLBACK callback function [Windows Controls]","LPFNPSPCALLBACKA","LPFNPSPCALLBACKW","PSPCB_ADDREF","PSPCB_CREATE","PSPCB_RELEASE","_win32_PropSheetPageProc","_win32_PropSheetPageProc_cpp","controls.PropSheetPageProc","controls._win32_PropSheetPageProc","prsht/LPFNPSPCALLBACK"]
old-location: controls\PropSheetPageProc.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\functions\propsheetpageproc.htm
ms.date: 12/05/2018
ms.keywords: LPFNPSPCALLBACK, LPFNPSPCALLBACK callback, LPFNPSPCALLBACK callback function [Windows Controls], LPFNPSPCALLBACKA, LPFNPSPCALLBACKW, PSPCB_ADDREF, PSPCB_CREATE, PSPCB_RELEASE, _win32_PropSheetPageProc, _win32_PropSheetPageProc_cpp, controls.PropSheetPageProc, controls._win32_PropSheetPageProc, prsht/LPFNPSPCALLBACK
req.header: prsht.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPFNPSPCALLBACKW
 - prsht/LPFNPSPCALLBACKW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Prsht.h
api_name:
 - LPFNPSPCALLBACK
 - LPFNPSPCALLBACK - LPFNPSPCALLBACKW
---

# LPFNPSPCALLBACKW callback function


## -description

Specifies an application-defined callback function that a property sheet calls when a page is created and when it is about to be destroyed. An application can use this function to perform initialization and cleanup operations for the page.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Reserved; must be <b>NULL</b>.

### -param uMsg [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Action flag. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PSPCB_ADDREF"></a><a id="pspcb_addref"></a><dl>
<dt><b>PSPCB_ADDREF</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 5.80</a> or later. A page is being created. The return value is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="PSPCB_CREATE"></a><a id="pspcb_create"></a><dl>
<dt><b>PSPCB_CREATE</b></dt>
</dl>
</td>
<td width="60%">
A dialog box for a page is being created. Return nonzero to allow it to be created, or zero to prevent it.

</td>
</tr>
<tr>
<td width="40%"><a id="PSPCB_RELEASE"></a><a id="pspcb_release"></a><dl>
<dt><b>PSPCB_RELEASE</b></dt>
</dl>
</td>
<td width="60%">
A page is being destroyed. The return value is ignored.

</td>
</tr>
</table>

### -param ppsp [in, out]

Type: <b>LPPROPSHEETPAGE</b>

Pointer to a <a href="/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2">PROPSHEETPAGE</a> structure that defines the page being created or destroyed. See the Remarks section for further discussion.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The return value depends on the value of the <i>uMsg</i> parameter.

## -remarks

An application must specify the address of this callback function in the <b>pfnCallback</b> member of a <a href="/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2">PROPSHEETPAGE</a> structure before passing the structure to the <a href="/windows/desktop/api/prsht/nf-prsht-createpropertysheetpagea">CreatePropertySheetPage</a> function.

<div class="alert"><b>Note</b>  The property sheet is in the process of manipulating the list of pages when this function is called. Do not attempt to add, remove, or insert pages while handling this notification. Doing so will have unpredictable results.</div>
<div> </div>
With the exception of the <b>lParam</b> member, your application should not modify the <a href="/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2">PROPSHEETPAGE</a> structure. Doing so will have unpredictable results. The <b>lParam</b> member contains application-defined data and can be modified as needed.




> [!NOTE]
> The prsht.h header defines LPFNPSPCALLBACK as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
