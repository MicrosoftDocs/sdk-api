---
UID: NF:prsht.PropSheet_InsertPage
title: PropSheet_InsertPage macro (prsht.h)
description: Inserts a new page into an existing property sheet. The page can be inserted either at a specified index or after a specified page. You can use this macro or send the PSM_INSERTPAGE message explicitly.
helpviewer_keywords: ["PropSheet_InsertPage","PropSheet_InsertPage macro [Windows Controls]","_win32_PropSheet_InsertPage","_win32_PropSheet_InsertPage_cpp","controls.PropSheet_InsertPage","controls._win32_PropSheet_InsertPage","hpageInsertAfter","index","prsht/PropSheet_InsertPage"]
old-location: controls\PropSheet_InsertPage.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_insertpage.htm
ms.date: 10/21/2024
ms.keywords: PropSheet_InsertPage, PropSheet_InsertPage macro [Windows Controls], _win32_PropSheet_InsertPage, _win32_PropSheet_InsertPage_cpp, controls.PropSheet_InsertPage, controls._win32_PropSheet_InsertPage, hpageInsertAfter, index, prsht/PropSheet_InsertPage
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
 - PropSheet_InsertPage
 - prsht/PropSheet_InsertPage
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
 - PropSheet_InsertPage
---

# PropSheet_InsertPage macro

## -syntax

```cpp
BOOL PropSheet_InsertPage(
   HWND hDlg,
   HWND index,
   HWND hpage
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns a nonzero value if the page was successfully inserted, or zero otherwise.


## -description

Inserts a new page into an existing property sheet. The page can be inserted either at a specified index or after a specified page. You can use this macro or send the <a href="/windows/desktop/Controls/psm-insertpage">PSM_INSERTPAGE</a> message explicitly.

## -parameters

### -param hDlg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the property sheet.

### -param index

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Where the page is to be inserted. Set <i>index</i> to <b>NULL</b> to make the new page the first page. To specify where the new page is to be inserted, you can either pass an index or an existing page's HPROPSHEETPAGE handle.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="index"></a><a id="INDEX"></a><dl>
<dt><b>index</b></dt>
</dl>
</td>
<td width="60%">
If <i>index</i> is less than MAXUSHORT (the largest unsigned short integer), it specifies the zero-based index for the new page. For example, to make the inserted page the third page on the property sheet, set <i>index</i> to 2. To make it the first page, set <i>index</i> to 0. If <i>index</i> has a value greater than the number of pages and less than MAXUSHORT, the page will be appended.

</td>
</tr>
<tr>
<td width="40%"><a id="hpageInsertAfter"></a><a id="hpageinsertafter"></a><a id="HPAGEINSERTAFTER"></a><dl>
<dt><b>hpageInsertAfter</b></dt>
</dl>
</td>
<td width="60%">
If you set <i>index</i> to an existing page's HPROPSHEETPAGE handle, the new page will be inserted after it.

</td>
</tr>
</table>

### -param hpage

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the page to be inserted. The page must first be created by a call to the <a href="/windows/desktop/api/prsht/nf-prsht-createpropertysheetpagea">CreatePropertySheetPage</a> function.

## -remarks

The pages after the insertion point are shifted to the right to accommodate the new page.

The property sheet is not resized to fit the new page. Do not make the new page larger than the property sheet's largest page.

A number of messages and one function call occur while the property sheet is manipulating the list of pages. While this action is taking place, attempting to modify the list of pages will have unpredictable results. Accordingly, you should not use the <b>PropSheet_InsertPage</b> macro in your implementation of <a href="/windows/desktop/api/prsht/nc-prsht-lpfnpspcallbacka">PropSheetPageProc</a> or while handling the following notifications and Windows messages.

<ul>
<li>
<a href="/windows/desktop/Controls/psn-apply">PSN_APPLY</a>
</li>
<li>
<a href="/windows/desktop/Controls/psn-killactive">PSN_KILLACTIVE</a>
</li>
<li>
<a href="/windows/desktop/Controls/psn-reset">PSN_RESET</a>
</li>
<li>
<a href="/windows/desktop/Controls/psn-setactive">PSN_SETACTIVE</a>
</li>
<li>
<a href="/windows/desktop/winmsg/wm-destroy">WM_DESTROY</a>
</li>
<li>
<a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a>
</li>
</ul>
If you need to modify a property sheet page while you are handling one of these messages or while <a href="/windows/desktop/api/prsht/nc-prsht-lpfnpspcallbacka">PropSheetPageProc</a> is in operation, post yourself a private Windows message. Your application will not receive that message until after the property sheet manager has finished its tasks. Then you can modify the list of pages.

The following notifications are also affected by property sheet modification.

<ul>
<li>
<a href="/windows/desktop/Controls/psn-wizback">PSN_WIZBACK</a>
</li>
<li>
<a href="/windows/desktop/Controls/psn-wiznext">PSN_WIZNEXT</a>
</li>
</ul>
You can add or remove pages in response to these notifications, provided that you return (via DWL_MSGRESULT) a nonzero value to specify the desired new page. Note, however, that if you insert a page that is located before the current page (that has a smaller index than the current page), <a href="/windows/desktop/Controls/psn-killactive">PSN_KILLACTIVE</a> might be sent to the wrong page.

<div class="alert"><b>Note</b>  This macro is not supported when using the Aero wizard style (<a href="/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PSH_AEROWIZARD</a>).</div>
<div> </div>
