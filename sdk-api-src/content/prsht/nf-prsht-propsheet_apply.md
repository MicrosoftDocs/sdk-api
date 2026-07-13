---
UID: NF:prsht.PropSheet_Apply
title: PropSheet_Apply macro (prsht.h)
description: Simulates the selection of the Apply button, indicating that one or more pages have changed and the changes need to be validated and recorded. You can use this macro or send the PSM_APPLY message explicitly.
helpviewer_keywords: ["PropSheet_Apply","PropSheet_Apply macro [Windows Controls]","_win32_PropSheet_Apply","_win32_PropSheet_Apply_cpp","controls.PropSheet_Apply","controls._win32_PropSheet_Apply","prsht/PropSheet_Apply"]
old-location: controls\PropSheet_Apply.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_apply.htm
ms.date: 10/21/2024
ms.keywords: PropSheet_Apply, PropSheet_Apply macro [Windows Controls], _win32_PropSheet_Apply, _win32_PropSheet_Apply_cpp, controls.PropSheet_Apply, controls._win32_PropSheet_Apply, prsht/PropSheet_Apply
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
 - PropSheet_Apply
 - prsht/PropSheet_Apply
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
 - PropSheet_Apply
---

# PropSheet_Apply macro

## -syntax

```cpp
BOOL PropSheet_Apply(
   HWND hDlg
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if all pages successfully applied the changes, or <b>FALSE</b> otherwise.


## -description

Simulates the selection of the <b>Apply</b> button, indicating that one or more pages have changed and the changes need to be validated and recorded. You can use this macro or send the <a href="/windows/desktop/Controls/psm-apply">PSM_APPLY</a> message explicitly.

## -parameters

### -param hDlg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the property sheet.

## -remarks

The property sheet sends the <a href="/windows/desktop/Controls/psn-killactive">PSN_KILLACTIVE</a> notification code to the current page. If the current page returns <b>FALSE</b>, the property sheet sends the <a href="/windows/desktop/Controls/psn-apply">PSN_APPLY</a> notification code to all active pages.

<div class="alert"><b>Note</b>  This macro is not supported when using the Aero wizard style (<a href="/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PSH_AEROWIZARD</a>).</div>
<div> </div>
