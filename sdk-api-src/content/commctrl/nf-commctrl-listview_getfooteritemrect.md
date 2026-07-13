---
UID: NF:commctrl.ListView_GetFooterItemRect
title: ListView_GetFooterItemRect macro (commctrl.h)
description: Gets the coordinates of a footer for a specified item in a list-view control. Use this macro or send the LVM_GETFOOTERITEMRECT message explicitly.
helpviewer_keywords: ["ListView_GetFooterItemRect","ListView_GetFooterItemRect macro [Windows Controls]","_shell_ListView_GetFooterItemRect","_shell_ListView_GetFooterItemRect_cpp","commctrl/ListView_GetFooterItemRect","controls.ListView_GetFooterItemRect","controls._shell_ListView_GetFooterItemRect"]
old-location: controls\ListView_GetFooterItemRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getfooteritemrect.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetFooterItemRect, ListView_GetFooterItemRect macro [Windows Controls], _shell_ListView_GetFooterItemRect, _shell_ListView_GetFooterItemRect_cpp, commctrl/ListView_GetFooterItemRect, controls.ListView_GetFooterItemRect, controls._shell_ListView_GetFooterItemRect
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
 - ListView_GetFooterItemRect
 - commctrl/ListView_GetFooterItemRect
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
 - ListView_GetFooterItemRect
---

# ListView_GetFooterItemRect macro

## -syntax

```cpp
BOOL ListView_GetFooterItemRect(
  [in]      HWND hwnd,
  [in]      UINT iItem,
  [in, out] RECT *prc
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Gets the coordinates of a  footer for a specified item in a list-view control. Use this macro or send the <a href="/windows/desktop/Controls/lvm-getfooteritemrect">LVM_GETFOOTERITEMRECT</a> message explicitly.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param iItem [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the item in the list-view control.

### -param prc [in, out]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure to receive the coordinates. The calling application is responsible for allocating this structure. The coordinates received are expressed as client coordinates.
