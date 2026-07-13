---
UID: NF:prsht.PropSheet_IdToIndex
title: PropSheet_IdToIndex macro (prsht.h)
description: Takes the resource identifier (ID) of a property sheet page and returns its zero-based index. You can use this macro or send the PSM_IDTOINDEX message explicitly.
helpviewer_keywords: ["PropSheet_IdToIndex","PropSheet_IdToIndex macro [Windows Controls]","_win32_PropSheet_IdToIndex","_win32_PropSheet_IdToIndex_cpp","controls.PropSheet_IdToIndex","controls._win32_PropSheet_IdToIndex","prsht/PropSheet_IdToIndex"]
old-location: controls\PropSheet_IdToIndex.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_idtoindex.htm
ms.date: 10/21/2024
ms.keywords: PropSheet_IdToIndex, PropSheet_IdToIndex macro [Windows Controls], _win32_PropSheet_IdToIndex, _win32_PropSheet_IdToIndex_cpp, controls.PropSheet_IdToIndex, controls._win32_PropSheet_IdToIndex, prsht/PropSheet_IdToIndex
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
 - PropSheet_IdToIndex
 - prsht/PropSheet_IdToIndex
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
 - PropSheet_IdToIndex
---

# PropSheet_IdToIndex macro

## -syntax

```cpp
int PropSheet_IdToIndex(
   HWND hDlg,
   int  id
);
```

## -returns

Type: **int**

Returns the zero-based index of the property sheet page specified by <i>id</i> if successful. Otherwise, it returns -1.


## -description

Takes the resource identifier (ID) of a property sheet page and returns its zero-based index. You can use this macro or send the <a href="/windows/desktop/controls/psm-idtoindex">PSM_IDTOINDEX</a> message explicitly.

## -parameters

### -param hDlg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the property sheet window.

### -param id

Type: <b>int</b>

Resource ID of the page.

## -see-also

<a href="/windows/desktop/api/prsht/nf-prsht-propsheet_indextoid">PropSheet_IndexToId</a>
