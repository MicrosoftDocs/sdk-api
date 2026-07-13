---
UID: NF:prsht.PropSheet_SetHeaderTitle
title: PropSheet_SetHeaderTitle macro (prsht.h)
description: Sets the title text for the header of a wizard's interior page. You can use this macro or send the PSM_SETHEADERTITLE message explicitly.
helpviewer_keywords: ["PropSheet_SetHeaderTitle","PropSheet_SetHeaderTitle macro [Windows Controls]","_win32_PropSheet_SetHeaderTitle","_win32_PropSheet_SetHeaderTitle_cpp","controls.PropSheet_SetHeaderTitle","controls._win32_PropSheet_SetHeaderTitle","prsht/PropSheet_SetHeaderTitle"]
old-location: controls\PropSheet_SetHeaderTitle.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_setheadertitle.htm
ms.date: 10/21/2024
ms.keywords: PropSheet_SetHeaderTitle, PropSheet_SetHeaderTitle macro [Windows Controls], _win32_PropSheet_SetHeaderTitle, _win32_PropSheet_SetHeaderTitle_cpp, controls.PropSheet_SetHeaderTitle, controls._win32_PropSheet_SetHeaderTitle, prsht/PropSheet_SetHeaderTitle
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
 - PropSheet_SetHeaderTitle
 - prsht/PropSheet_SetHeaderTitle
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
 - PropSheet_SetHeaderTitle
---

# PropSheet_SetHeaderTitle macro

## -syntax

```cpp
int PropSheet_SetHeaderTitle(
   HWND    hDlg,
   int     index,
   LPCTSTR lpszText
);
```

## -returns

Type: **int**

No return value.


## -description

Sets the title text for the header of a wizard's interior page. You can use this macro or send the <a href="/windows/desktop/Controls/psm-setheadertitle">PSM_SETHEADERTITLE</a> message explicitly.

## -parameters

### -param hDlg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the wizard's window.

### -param index

Type: <b>int</b>

Zero-based index of the page.

### -param lpszText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

New header title.

## -remarks

If you specify the current page, it will immediately be repainted to display the new title.
