---
UID: NF:prsht.PropSheet_IndexToId
title: PropSheet_IndexToId macro (prsht.h)
description: Takes the index of a property sheet page and returns its resource identifier (ID). You can use this macro or send the PSM_INDEXTOID message explicitly.
helpviewer_keywords: ["PropSheet_IndexToId","PropSheet_IndexToId macro [Windows Controls]","_win32_PropSheet_IndexToId","_win32_PropSheet_IndexToId_cpp","controls.PropSheet_IndexToId","controls._win32_PropSheet_IndexToId","prsht/PropSheet_IndexToId"]
old-location: controls\PropSheet_IndexToId.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_indextoid.htm
ms.date: 10/21/2024
ms.keywords: PropSheet_IndexToId, PropSheet_IndexToId macro [Windows Controls], _win32_PropSheet_IndexToId, _win32_PropSheet_IndexToId_cpp, controls.PropSheet_IndexToId, controls._win32_PropSheet_IndexToId, prsht/PropSheet_IndexToId
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
 - PropSheet_IndexToId
 - prsht/PropSheet_IndexToId
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
 - PropSheet_IndexToId
---

# PropSheet_IndexToId macro

## -syntax

```cpp
int PropSheet_IndexToId(
   HWND hDlg,
   int  i
);
```

## -returns

Type: **int**

Returns the resource ID of the property sheet page specified by <i>i</i> if successful. Otherwise, it returns zero.

## -description

Takes the index of a property sheet page and returns its resource identifier (ID). You can use this macro or send the <a href="/windows/desktop/Controls/psm-indextoid">PSM_INDEXTOID</a> message explicitly.

## -parameters

### -param hDlg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the property sheet.

### -param i

Type: <b>int</b>

Zero-based index of the page.

## -see-also

<a href="/windows/desktop/Controls/psm-indextoid">PSM_INDEXTOID</a>
