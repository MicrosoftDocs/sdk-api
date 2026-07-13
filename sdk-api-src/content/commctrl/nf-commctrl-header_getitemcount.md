---
UID: NF:commctrl.Header_GetItemCount
title: Header_GetItemCount macro (commctrl.h)
description: Gets a count of the items in a header control. You can use this macro or send the HDM_GETITEMCOUNT message explicitly.
helpviewer_keywords: ["Header_GetItemCount","Header_GetItemCount macro [Windows Controls]","_win32_Header_GetItemCount","_win32_Header_GetItemCount_cpp","commctrl/Header_GetItemCount","controls.Header_GetItemCount","controls._win32_Header_GetItemCount"]
old-location: controls\Header_GetItemCount.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_getitemcount.htm
ms.date: 10/21/2024
ms.keywords: Header_GetItemCount, Header_GetItemCount macro [Windows Controls], _win32_Header_GetItemCount, _win32_Header_GetItemCount_cpp, commctrl/Header_GetItemCount, controls.Header_GetItemCount, controls._win32_Header_GetItemCount
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
 - Header_GetItemCount
 - commctrl/Header_GetItemCount
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
 - Header_GetItemCount
---

# Header_GetItemCount macro

## -syntax

```cpp
int Header_GetItemCount(
   HWND hwndHD
);
```

## -returns

Type: **int**

Returns the number of items if successful, or -1 otherwise.


## -description

Gets a count of the items in a header control. You can use this macro or send the <a href="/windows/desktop/Controls/hdm-getitemcount">HDM_GETITEMCOUNT</a> message explicitly.

## -parameters

### -param hwndHD

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the header control.

## -remarks

The <b>Header_GetItemCount</b> macro is defined as follows. 


``` syntax
#define Header_GetItemCount(hwndHD)   \

       (int)SendMessage((hwndHD), HDM_GETITEMCOUNT, 0, 0L)
```

