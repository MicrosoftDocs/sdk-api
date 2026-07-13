---
UID: NF:prsht.PropSheet_RemovePage
title: PropSheet_RemovePage macro (prsht.h)
description: Removes a page from a property sheet. You can use this macro or send the PSM_REMOVEPAGE message explicitly.
helpviewer_keywords: ["PropSheet_RemovePage","PropSheet_RemovePage macro [Windows Controls]","_win32_PropSheet_RemovePage","_win32_PropSheet_RemovePage_cpp","controls.PropSheet_RemovePage","controls._win32_PropSheet_RemovePage","prsht/PropSheet_RemovePage"]
old-location: controls\PropSheet_RemovePage.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_removepage.htm
ms.date: 10/21/2024
ms.keywords: PropSheet_RemovePage, PropSheet_RemovePage macro [Windows Controls], _win32_PropSheet_RemovePage, _win32_PropSheet_RemovePage_cpp, controls.PropSheet_RemovePage, controls._win32_PropSheet_RemovePage, prsht/PropSheet_RemovePage
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
 - PropSheet_RemovePage
 - prsht/PropSheet_RemovePage
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
 - PropSheet_RemovePage
---

# PropSheet_RemovePage macro

## -syntax

```cpp
VOID PropSheet_RemovePage(
   HWND           hDlg,
   int            index,
   HPROPSHEETPAGE hpage
);
```

## -returns

Type: **[VOID](/windows/desktop/winprog/windows-data-types)**

No return value.


## -description

Removes a page from a property sheet. You can use this macro or send the <a href="/windows/desktop/Controls/psm-removepage">PSM_REMOVEPAGE</a> message explicitly.

## -parameters

### -param hDlg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the property sheet.

### -param index

Type: <b>int</b>

Zero-based index of the page to be removed.

### -param hpage

Type: <b>HPROPSHEETPAGE</b>

Handle to the page to be removed.

## -remarks

An application can specify the page to be removed by assigning a value to either <i>index</i> or <i>hpage</i>. If values are assigned to both <i>index</i> and <i>hpage</i>, <i>hpage</i> takes precedence.

A number of messages and one function call occur while the property sheet is manipulating the list of pages. While this action is taking place, attempting to modify the list of pages will have unpredictable results. Accordingly, you should not use the <b>PropSheet_RemovePage</b> macro in your implementation of <a href="/windows/desktop/api/prsht/nc-prsht-lpfnpspcallbacka">PropSheetPageProc</a> or while handling the following notifications and Windows messages.

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
You can add or remove pages in response to these notifications, provided that you return (via DWL_MSGRESULT) a nonzero value to specify the desired new page. Note, however, that if you remove a page that is located before the current page (that has a smaller index than the current page), <a href="/windows/desktop/Controls/psn-killactive">PSN_KILLACTIVE</a> might be sent to the wrong page.

<div class="alert"><b>Note</b>  This macro is not supported when using the Aero wizard style (<a href="/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PSH_AEROWIZARD</a>).</div>
<div> </div>
