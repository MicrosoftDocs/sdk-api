---
UID: NF:commctrl.ListView_GetCallbackMask
title: ListView_GetCallbackMask macro (commctrl.h)
description: Gets the callback mask for a list-view control. You can use this macro or send the LVM_GETCALLBACKMASK message explicitly.
helpviewer_keywords: ["ListView_GetCallbackMask","ListView_GetCallbackMask macro [Windows Controls]","_win32_ListView_GetCallbackMask","_win32_ListView_GetCallbackMask_cpp","commctrl/ListView_GetCallbackMask","controls.ListView_GetCallbackMask","controls._win32_ListView_GetCallbackMask"]
old-location: controls\ListView_GetCallbackMask.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getcallbackmask.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetCallbackMask, ListView_GetCallbackMask macro [Windows Controls], _win32_ListView_GetCallbackMask, _win32_ListView_GetCallbackMask_cpp, commctrl/ListView_GetCallbackMask, controls.ListView_GetCallbackMask, controls._win32_ListView_GetCallbackMask
req.header: commctrl.h
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
 - ListView_GetCallbackMask
 - commctrl/ListView_GetCallbackMask
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
 - ListView_GetCallbackMask
---

# ListView_GetCallbackMask macro

## -syntax

```cpp
UINT ListView_GetCallbackMask(
   HWND hwnd
);
```

## -returns

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

Returns the callback mask.


## -description

Gets the callback mask for a list-view control. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-getcallbackmask">LVM_GETCALLBACKMASK</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

## -see-also

<a href="/windows/desktop/Controls/lvm-setcallbackmask">LVM_SETCALLBACKMASK</a>
