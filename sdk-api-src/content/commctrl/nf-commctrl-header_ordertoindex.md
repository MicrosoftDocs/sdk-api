---
UID: NF:commctrl.Header_OrderToIndex
title: Header_OrderToIndex macro (commctrl.h)
description: Retrieves an index value for an item based on its order in the header control. You can use this macro or send the HDM_ORDERTOINDEX message explicitly.
helpviewer_keywords: ["Header_OrderToIndex","Header_OrderToIndex macro [Windows Controls]","_win32_Header_OrderToIndex","_win32_Header_OrderToIndex_cpp","commctrl/Header_OrderToIndex","controls.Header_OrderToIndex","controls._win32_Header_OrderToIndex"]
old-location: controls\Header_OrderToIndex.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_ordertoindex.htm
ms.date: 10/21/2024
ms.keywords: Header_OrderToIndex, Header_OrderToIndex macro [Windows Controls], _win32_Header_OrderToIndex, _win32_Header_OrderToIndex_cpp, commctrl/Header_OrderToIndex, controls.Header_OrderToIndex, controls._win32_Header_OrderToIndex
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
 - Header_OrderToIndex
 - commctrl/Header_OrderToIndex
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
 - Header_OrderToIndex
---

# Header_OrderToIndex macro

## -syntax

```cpp
int Header_OrderToIndex(
   HWND hwnd,
   int  i
);
```

## -returns

Type: **int**

Returns an <b>int</b> that specifies the index of the item. If <i>i</i> is invalid (negative or too large), the return equals <i>i</i>.


## -description

Retrieves an index value for an item based on its order in the header control. You can use this macro or send the <a href="/windows/desktop/controls/hdm-ordertoindex">HDM_ORDERTOINDEX</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a header control.

### -param i

Type: <b>int</b>

The order that the item appears within the header control, from left to right. The index value of the item in the far left column would be 0, the next item to the right would be 1, and so on.
