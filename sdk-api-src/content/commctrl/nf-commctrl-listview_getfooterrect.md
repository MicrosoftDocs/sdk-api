---
UID: NF:commctrl.ListView_GetFooterRect
title: ListView_GetFooterRect macro (commctrl.h)
description: Gets the coordinates of the footer for a specified list-view control. Use this macro or send the LVM_GETFOOTERRECT message explicitly.
helpviewer_keywords: ["ListView_GetFooterRect","ListView_GetFooterRect macro [Windows Controls]","_shell_ListView_GetFooterRect","_shell_ListView_GetFooterRect_cpp","commctrl/ListView_GetFooterRect","controls.ListView_GetFooterRect","controls._shell_ListView_GetFooterRect"]
old-location: controls\ListView_GetFooterRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getfooterrect.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetFooterRect, ListView_GetFooterRect macro [Windows Controls], _shell_ListView_GetFooterRect, _shell_ListView_GetFooterRect_cpp, commctrl/ListView_GetFooterRect, controls.ListView_GetFooterRect, controls._shell_ListView_GetFooterRect
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
 - ListView_GetFooterRect
 - commctrl/ListView_GetFooterRect
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
 - ListView_GetFooterRect
---

# ListView_GetFooterRect macro

## -syntax

```cpp
BOOL ListView_GetFooterRect(
  [in]      HWND hwnd,
  [in, out] RECT *prc
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Gets the coordinates of the footer for a specified list-view control. Use this macro or send the <a href="/windows/desktop/Controls/lvm-getfooterrect">LVM_GETFOOTERRECT</a> message explicitly.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param prc [in, out]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure to receive the coordinates. The caller is responsible for allocating this structure. The coordinates received are expressed as client coordinates.
