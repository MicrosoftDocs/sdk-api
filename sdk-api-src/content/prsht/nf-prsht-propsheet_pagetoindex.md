---
UID: NF:prsht.PropSheet_PageToIndex
title: PropSheet_PageToIndex macro (prsht.h)
description: Takes the HPROPSHEETPAGE handle of a property sheet page and returns its zero-based index. You can use this macro or send the PSM_PAGETOINDEX message explicitly.
helpviewer_keywords: ["PropSheet_PageToIndex","PropSheet_PageToIndex macro [Windows Controls]","_win32_PropSheet_PageToIndex","_win32_PropSheet_PageToIndex_cpp","controls.PropSheet_PageToIndex","controls._win32_PropSheet_PageToIndex","prsht/PropSheet_PageToIndex"]
old-location: controls\PropSheet_PageToIndex.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_pagetoindex.htm
ms.date: 10/21/2024
ms.keywords: PropSheet_PageToIndex, PropSheet_PageToIndex macro [Windows Controls], _win32_PropSheet_PageToIndex, _win32_PropSheet_PageToIndex_cpp, controls.PropSheet_PageToIndex, controls._win32_PropSheet_PageToIndex, prsht/PropSheet_PageToIndex
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
 - PropSheet_PageToIndex
 - prsht/PropSheet_PageToIndex
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
 - PropSheet_PageToIndex
---

# PropSheet_PageToIndex macro

## -syntax

```cpp
int PropSheet_PageToIndex(
   HWND           hDlg,
   HPROPSHEETPAGE hpage
);
```

## -returns

Type: **int**

Returns the zero-based index of the property sheet page specified by <i>hpage</i>  if successful. Otherwise, it returns -1.


## -description

Takes the HPROPSHEETPAGE handle of a property sheet page and returns its zero-based index. You can use this macro or send the <a href="/windows/desktop/controls/psm-pagetoindex">PSM_PAGETOINDEX</a> message explicitly.

## -parameters

### -param hDlg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the property sheet.

### -param hpage

Type: <b>HPROPSHEETPAGE</b>

HPROPSHEETPAGE handle to the property sheet page.

## -see-also

<a href="/windows/desktop/api/prsht/nf-prsht-createpropertysheetpagea">CreatePropertySheetPage</a>



<a href="/windows/desktop/api/prsht/nf-prsht-propsheet_indextopage">PropSheet_IndexToPage</a>



<b>Reference</b>
