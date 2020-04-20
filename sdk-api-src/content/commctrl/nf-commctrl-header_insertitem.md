---
UID: NF:commctrl.Header_InsertItem
title: Header_InsertItem macro (commctrl.h)
description: Inserts a new item into a header control. You can use this macro or send the HDM_INSERTITEM message explicitly.helpviewer_keywords: ["Header_InsertItem","Header_InsertItem macro [Windows Controls]","_win32_Header_InsertItem","_win32_Header_InsertItem_cpp","commctrl/Header_InsertItem","controls.Header_InsertItem","controls._win32_Header_InsertItem"]
old-location: controls\Header_InsertItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_insertitem.htm
ms.date: 12/05/2018
ms.keywords: Header_InsertItem, Header_InsertItem macro [Windows Controls], _win32_Header_InsertItem, _win32_Header_InsertItem_cpp, commctrl/Header_InsertItem, controls.Header_InsertItem, controls._win32_Header_InsertItem
f1_keywords:
- commctrl/Header_InsertItem
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Commctrl.h
api_name:
- Header_InsertItem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Header_InsertItem macro


## -description


Inserts a new item into a header control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/hdm-insertitem">HDM_INSERTITEM</a> message explicitly. 


## -parameters




### -param hwndHD

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the header control. 


### -param i

Type: <b>int</b>

The index of the item after which the new item is to be inserted. The new item is inserted at the end of the header control if 
					<i>index</i> is greater than or equal to the number of items in the control. If 
					<i>index</i> is zero, the new item is inserted at the beginning of the header control. 


### -param phdi

Type: <b>const LPHDITEM</b>

A pointer to an <a href="https://docs.microsoft.com/windows/win32/api/commctrl/ns-commctrl-hditema">HDITEM</a> structure that contains information about the new item. 


## -remarks



The <b>Header_InsertItem</b> macro is defined as follows: 

<pre class="syntax" xml:space="preserve"><code>#define Header_InsertItem(hwndHD, index, phdi) \

    (int)SendMessage((hwndHD), HDM_INSERTITEM, (WPARAM)(int)(index), \

    (LPARAM)(const LPHDITEM)(phdi))</code></pre>


