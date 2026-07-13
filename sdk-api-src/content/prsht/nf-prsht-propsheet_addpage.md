---
UID: NF:prsht.PropSheet_AddPage
title: PropSheet_AddPage macro (prsht.h)
description: Adds a new page to the end of an existing property sheet. You can use this macro or send the PSM_ADDPAGE message explicitly.
helpviewer_keywords: ["PropSheet_AddPage","PropSheet_AddPage macro [Windows Controls]","_win32_PropSheet_AddPage","_win32_PropSheet_AddPage_cpp","controls.PropSheet_AddPage","controls._win32_PropSheet_AddPage","prsht/PropSheet_AddPage"]
old-location: controls\PropSheet_AddPage.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_addpage.htm
ms.date: 10/21/2024
ms.keywords: PropSheet_AddPage, PropSheet_AddPage macro [Windows Controls], _win32_PropSheet_AddPage, _win32_PropSheet_AddPage_cpp, controls.PropSheet_AddPage, controls._win32_PropSheet_AddPage, prsht/PropSheet_AddPage
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
 - PropSheet_AddPage
 - prsht/PropSheet_AddPage
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
 - PropSheet_AddPage
---

# PropSheet_AddPage macro

## -syntax

```cpp
BOOL PropSheet_AddPage(
   HWND           hDlg,
   HPROPSHEETPAGE hpage
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Adds a new page to the end of an existing property sheet. You can use this macro or send the <a href="/windows/desktop/Controls/psm-addpage">PSM_ADDPAGE</a> message explicitly.

## -parameters

### -param hDlg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the property sheet.

### -param hpage

Type: <b>HPROPSHEETPAGE</b>

Handle to the page to add. The page must have been created by a previous call to the <a href="/windows/desktop/api/prsht/nf-prsht-createpropertysheetpagea">CreatePropertySheetPage</a> function.

## -remarks

The new page should be no larger than the largest page currently in the property sheet because the property sheet is not resized to fit the new page.

A number of messages and one function call occur while the property sheet is manipulating the list of pages. While this action is taking place, attempting to modify the list of pages will have unpredictable results. Accordingly, you should not use the <b>PropSheet_AddPage</b> macro in your implementation of <a href="/windows/desktop/api/prsht/nc-prsht-lpfnpspcallbacka">PropSheetPageProc</a> or while handling the following notifications and Microsoft Windows messages:

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
