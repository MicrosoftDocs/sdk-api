---
UID: NF:prsht.PropSheet_Changed
title: PropSheet_Changed macro (prsht.h)
description: Informs a property sheet that information in a page has changed. You can use this macro or send the PSM_CHANGED message explicitly.
helpviewer_keywords: ["PropSheet_Changed","PropSheet_Changed macro [Windows Controls]","_win32_PropSheet_Changed","_win32_PropSheet_Changed_cpp","controls.PropSheet_Changed","controls._win32_PropSheet_Changed","prsht/PropSheet_Changed"]
old-location: controls\PropSheet_Changed.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_changed.htm
ms.date: 10/21/2024
ms.keywords: PropSheet_Changed, PropSheet_Changed macro [Windows Controls], _win32_PropSheet_Changed, _win32_PropSheet_Changed_cpp, controls.PropSheet_Changed, controls._win32_PropSheet_Changed, prsht/PropSheet_Changed
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
 - PropSheet_Changed
 - prsht/PropSheet_Changed
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
 - PropSheet_Changed
---

# PropSheet_Changed macro

## -syntax

```cpp
BOOL PropSheet_Changed(
   HWND hDlg,
   HWND hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

No return value.


## -description

Informs a property sheet that information in a page has changed. You can use this macro or send the <a href="/windows/desktop/Controls/psm-changed">PSM_CHANGED</a> message explicitly.

## -parameters

### -param hDlg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the property sheet.

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the page that has changed.

## -remarks

The property sheet enables the <b>Apply</b> button.

<div class="alert"><b>Note</b>  This macro is not supported when using the Aero wizard style (<a href="/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PSH_AEROWIZARD</a>).</div>
<div> </div>
