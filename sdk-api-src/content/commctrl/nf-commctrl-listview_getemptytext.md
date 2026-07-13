---
UID: NF:commctrl.ListView_GetEmptyText
title: ListView_GetEmptyText macro (commctrl.h)
description: Gets the text meant for display when the list-view control appears empty. Use this macro or send the LVM_GETEMPTYTEXT message explicitly.
helpviewer_keywords: ["ListView_GetEmptyText","ListView_GetEmptyText macro [Windows Controls]","_shell_ListView_GetEmptyText","_shell_ListView_GetEmptyText_cpp","commctrl/ListView_GetEmptyText","controls.ListView_GetEmptyText","controls._shell_ListView_GetEmptyText"]
old-location: controls\ListView_GetEmptyText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getemptytext.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetEmptyText, ListView_GetEmptyText macro [Windows Controls], _shell_ListView_GetEmptyText, _shell_ListView_GetEmptyText_cpp, commctrl/ListView_GetEmptyText, controls.ListView_GetEmptyText, controls._shell_ListView_GetEmptyText
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - ListView_GetEmptyText
 - commctrl/ListView_GetEmptyText
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - ListView_GetEmptyText
---

# ListView_GetEmptyText macro

## -syntax

```cpp
BOOL ListView_GetEmptyText(
  [in]      HWND  hwnd,
  [in, out] PWSTR pszText,
  [in]      UINT  cchText
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Gets the text meant for display when the list-view control appears empty. Use this macro or send the <a href="/windows/desktop/Controls/lvm-getemptytext">LVM_GETEMPTYTEXT</a> message explicitly.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param pszText [in, out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">PWSTR</a></b>

A pointer to a null-terminated, Unicode buffer of size specified by <i>cchText</i> to receive the text. The caller is responsible for allocating the buffer.

### -param cchText [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The size of the buffer pointed to by <i>pszText</i>, including the terminating               <b>NULL</b>.
