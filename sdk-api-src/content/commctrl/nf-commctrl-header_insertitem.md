---
UID: NF:commctrl.Header_InsertItem
title: Header_InsertItem macro
author: windows-sdk-content
description: Inserts a new item into a header control. You can use this macro or send the HDM_INSERTITEM message explicitly.
old-location: controls\Header_InsertItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_insertitem.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: Header_InsertItem, Header_InsertItem macro [Windows Controls], _win32_Header_InsertItem, _win32_Header_InsertItem_cpp, commctrl/Header_InsertItem, controls.Header_InsertItem, controls._win32_Header_InsertItem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Header_InsertItem macro


## -description


Inserts a new item into a header control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775351(v=VS.85).aspx">HDM_INSERTITEM</a> message explicitly. 


## -parameters




### -param hwndHD

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the header control. 


### -param i

Type: <b>int</b>

The index of the item after which the new item is to be inserted. The new item is inserted at the end of the header control if 
					<i>index</i> is greater than or equal to the number of items in the control. If 
					<i>index</i> is zero, the new item is inserted at the beginning of the header control. 


### -param phdi

Type: <b>const LPHDITEM</b>

A pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb775247(v=VS.85).aspx">HDITEM</a> structure that contains information about the new item. 


## -remarks



The <b>Header_InsertItem</b> macro is defined as follows: 

<pre class="syntax" xml:space="preserve"><code>#define Header_InsertItem(hwndHD, index, phdi) \

    (int)SendMessage((hwndHD), HDM_INSERTITEM, (WPARAM)(int)(index), \

    (LPARAM)(const LPHDITEM)(phdi))</code></pre>


