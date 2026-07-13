---
UID: NF:prsht.PropSheet_IndexToPage
title: PropSheet_IndexToPage macro (prsht.h)
description: Takes the index of a property sheet page and returns its HPROPSHEETPAGE handle. You can use this macro or send the PSM_INDEXTOPAGE message explicitly.
helpviewer_keywords: ["PropSheet_IndexToPage","PropSheet_IndexToPage macro [Windows Controls]","_win32_PropSheet_IndexToPage","_win32_PropSheet_IndexToPage_cpp","controls.PropSheet_IndexToPage","controls._win32_PropSheet_IndexToPage","prsht/PropSheet_IndexToPage"]
old-location: controls\PropSheet_IndexToPage.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_indextopage.htm
ms.date: 10/21/2024
ms.keywords: PropSheet_IndexToPage, PropSheet_IndexToPage macro [Windows Controls], _win32_PropSheet_IndexToPage, _win32_PropSheet_IndexToPage_cpp, controls.PropSheet_IndexToPage, controls._win32_PropSheet_IndexToPage, prsht/PropSheet_IndexToPage
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
 - PropSheet_IndexToPage
 - prsht/PropSheet_IndexToPage
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
 - PropSheet_IndexToPage
---

# PropSheet_IndexToPage macro

## -syntax

```cpp
HPROPSHEETPAGE PropSheet_IndexToPage(
   HWND hDlg,
   int  i
);
```

## -returns

Type: **HPROPSHEETPAGE**

Returns the HPROPSHEETPAGE handle of the property sheet page specified by <i>i</i> if successful. Otherwise, it returns zero.


## -description

Takes the index of a property sheet page and returns its HPROPSHEETPAGE handle. You can use this macro or send the <a href="/windows/desktop/Controls/psm-indextopage">PSM_INDEXTOPAGE</a> message explicitly.

## -parameters

### -param hDlg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the property sheet window.

### -param i

Type: <b>int</b>

Zero-based index of the page.

## -see-also

<a href="/windows/desktop/api/prsht/nf-prsht-propsheet_pagetoindex">PropSheet_PageToIndex</a>
