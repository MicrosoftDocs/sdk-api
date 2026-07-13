---
UID: NF:prsht.PropSheet_SetCurSel
title: PropSheet_SetCurSel macro (prsht.h)
description: Activates the specified page in a property sheet. You can use this macro or send the PSM_SETCURSEL message explicitly.
helpviewer_keywords: ["PropSheet_SetCurSel","PropSheet_SetCurSel macro [Windows Controls]","_win32_PropSheet_SetCurSel","_win32_PropSheet_SetCurSel_cpp","controls.PropSheet_SetCurSel","controls._win32_PropSheet_SetCurSel","prsht/PropSheet_SetCurSel"]
old-location: controls\PropSheet_SetCurSel.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_setcursel.htm
ms.date: 10/21/2024
ms.keywords: PropSheet_SetCurSel, PropSheet_SetCurSel macro [Windows Controls], _win32_PropSheet_SetCurSel, _win32_PropSheet_SetCurSel_cpp, controls.PropSheet_SetCurSel, controls._win32_PropSheet_SetCurSel, prsht/PropSheet_SetCurSel
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
 - PropSheet_SetCurSel
 - prsht/PropSheet_SetCurSel
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
 - PropSheet_SetCurSel
---

# PropSheet_SetCurSel macro

## -syntax

```cpp
BOOL PropSheet_SetCurSel(
   HWND           hDlg,
   HPROPSHEETPAGE hpage,
   UINT           index
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Activates the specified page in a property sheet. You can use this macro or send the <a href="/windows/desktop/Controls/psm-setcursel">PSM_SETCURSEL</a> message explicitly.

## -parameters

### -param hDlg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the property sheet.

### -param hpage

Type: <b>HPROPSHEETPAGE</b>

Handle to the page to activate. An application can specify the index or the handle, or both. If both are specified, <i>hpage</i> takes precedence.

### -param index

Type: <b>UINT</b>

Zero-based index of the page. An application can specify the index or the handle, or both. If both are specified, <i>hpage</i> takes precedence.

## -remarks

The window that is losing the activation receives the <a href="/windows/desktop/Controls/psn-killactive">PSN_KILLACTIVE</a> notification code, and the window that is gaining the activation receives the <a href="/windows/desktop/Controls/psn-setactive">PSN_SETACTIVE</a> notification code.
