---
UID: NF:prsht.PropSheet_HwndToIndex
title: PropSheet_HwndToIndex macro (prsht.h)
description: Takes a window handle of the property sheet page and returns its zero-based index. You can use this macro or send the PSM_HWNDTOINDEX message explicitly.helpviewer_keywords: ["PropSheet_HwndToIndex","PropSheet_HwndToIndex macro [Windows Controls]","_win32_PropSheet_HwndToIndex","_win32_PropSheet_HwndToIndex_cpp","controls.PropSheet_HwndToIndex","controls._win32_PropSheet_HwndToIndex","prsht/PropSheet_HwndToIndex"]
old-location: controls\PropSheet_HwndToIndex.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_hwndtoindex.htm
ms.date: 12/05/2018
ms.keywords: PropSheet_HwndToIndex, PropSheet_HwndToIndex macro [Windows Controls], _win32_PropSheet_HwndToIndex, _win32_PropSheet_HwndToIndex_cpp, controls.PropSheet_HwndToIndex, controls._win32_PropSheet_HwndToIndex, prsht/PropSheet_HwndToIndex
ms.topic: macro
f1_keywords:
- prsht/PropSheet_HwndToIndex
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Prsht.h
api_name:
- PropSheet_HwndToIndex
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PropSheet_HwndToIndex macro


## -description


Takes a window handle of the property sheet page and returns its zero-based index. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/controls/psm-hwndtoindex">PSM_HWNDTOINDEX</a> message explicitly.


## -parameters




### -param hDlg

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the property sheet's window.


### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the page's window.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getparent">GetParent</a>



<b>Other Resources</b>



<a href="https://docs.microsoft.com/windows/desktop/api/prsht/nf-prsht-propsheet_getcurrentpagehwnd">PropSheet_GetCurrentPageHwnd</a>



<b>Reference</b>
 

 

