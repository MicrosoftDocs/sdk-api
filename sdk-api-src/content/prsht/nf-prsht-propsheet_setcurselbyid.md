---
UID: NF:prsht.PropSheet_SetCurSelByID
title: PropSheet_SetCurSelByID macro (prsht.h)
description: Activates the specified page in a property sheet based on the resource identifier of the page. You can use this macro or send the PSM_SETCURSELID message explicitly.
helpviewer_keywords: ["PropSheet_SetCurSelByID","PropSheet_SetCurSelByID macro [Windows Controls]","_win32_PropSheet_SetCurSelByID","_win32_PropSheet_SetCurSelByID_cpp","controls.PropSheet_SetCurSelByID","controls._win32_PropSheet_SetCurSelByID","prsht/PropSheet_SetCurSelByID"]
old-location: controls\PropSheet_SetCurSelByID.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_setcurselbyid.htm
ms.date: 10/21/2024
ms.keywords: PropSheet_SetCurSelByID, PropSheet_SetCurSelByID macro [Windows Controls], _win32_PropSheet_SetCurSelByID, _win32_PropSheet_SetCurSelByID_cpp, controls.PropSheet_SetCurSelByID, controls._win32_PropSheet_SetCurSelByID, prsht/PropSheet_SetCurSelByID
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
 - PropSheet_SetCurSelByID
 - prsht/PropSheet_SetCurSelByID
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
 - PropSheet_SetCurSelByID
---

# PropSheet_SetCurSelByID macro

## -syntax

```cpp
BOOL PropSheet_SetCurSelByID(
   HWND hDlg,
   int  id
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Activates the specified page in a property sheet based on the resource identifier of the page. You can use this macro or send the <a href="/windows/desktop/Controls/psm-setcurselid">PSM_SETCURSELID</a> message explicitly.

## -parameters

### -param hDlg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the property sheet.

### -param id

Type: <b>int</b>

Resource identifier of the page to activate.

## -remarks

The window that is losing the activation receives the <a href="/windows/desktop/Controls/psn-killactive">PSN_KILLACTIVE</a> notification code, and the window that is gaining the activation receives the <a href="/windows/desktop/Controls/psn-setactive">PSN_SETACTIVE</a> notification code.
