---
UID: NF:prsht.PropSheet_HwndToIndex
title: PropSheet_HwndToIndex macro (prsht.h)
description: Takes a window handle of the property sheet page and returns its zero-based index. You can use this macro or send the PSM_HWNDTOINDEX message explicitly.
helpviewer_keywords: ["PropSheet_HwndToIndex","PropSheet_HwndToIndex macro [Windows Controls]","_win32_PropSheet_HwndToIndex","_win32_PropSheet_HwndToIndex_cpp","controls.PropSheet_HwndToIndex","controls._win32_PropSheet_HwndToIndex","prsht/PropSheet_HwndToIndex"]
old-location: controls\PropSheet_HwndToIndex.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_hwndtoindex.htm
ms.date: 10/21/2024
ms.keywords: PropSheet_HwndToIndex, PropSheet_HwndToIndex macro [Windows Controls], _win32_PropSheet_HwndToIndex, _win32_PropSheet_HwndToIndex_cpp, controls.PropSheet_HwndToIndex, controls._win32_PropSheet_HwndToIndex, prsht/PropSheet_HwndToIndex
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
 - PropSheet_HwndToIndex
 - prsht/PropSheet_HwndToIndex
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
 - PropSheet_HwndToIndex
---

# PropSheet_HwndToIndex macro

## -syntax

```cpp
int PropSheet_HwndToIndex(
   HWND hDlg,
   HWND hwnd
);
```

## -returns

Type: **int**

Returns the zero-based index of the property sheet page specified by <i>hwnd</i> if successful. Otherwise, it returns -1.


## -description

Takes a window handle of the property sheet page and returns its zero-based index. You can use this macro or send the <a href="/windows/desktop/controls/psm-hwndtoindex">PSM_HWNDTOINDEX</a> message explicitly.

## -parameters

### -param hDlg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the property sheet's window.

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the page's window.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-getparent">GetParent</a>



<b>Other Resources</b>



<a href="/windows/desktop/api/prsht/nf-prsht-propsheet_getcurrentpagehwnd">PropSheet_GetCurrentPageHwnd</a>



<b>Reference</b>
