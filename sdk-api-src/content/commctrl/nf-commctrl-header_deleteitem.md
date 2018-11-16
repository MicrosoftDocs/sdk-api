---
UID: NF:commctrl.Header_DeleteItem
title: Header_DeleteItem macro
author: windows-sdk-content
description: Deletes an item from a header control. You can use this macro or send the HDM_DELETEITEM message explicitly.
old-location: controls\Header_DeleteItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_deleteitem.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Header_DeleteItem, Header_DeleteItem macro [Windows Controls], _win32_Header_DeleteItem, _win32_Header_DeleteItem_cpp, commctrl/Header_DeleteItem, controls.Header_DeleteItem, controls._win32_Header_DeleteItem
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
 - Header_DeleteItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- commctrl.h
: 
- Header_DeleteItem
: 
---

# Header_DeleteItem macro


## -description


Deletes an item from a header control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775310(v=VS.85).aspx">HDM_DELETEITEM</a> message explicitly. 


## -parameters




### -param hwndHD

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the header control. 


### -param i

Type: <b>int</b>

An index of the item to delete. 


## -remarks



The <b>Header_DeleteItem</b> macro is defined as follows. 

<pre class="syntax" xml:space="preserve"><code>#define Header_DeleteItem(hwndHD, index)     \

      (BOOL)SendMessage((hwndHD), HDM_DELETEITEM, (WPARAM)(int)(index), 0L)</code></pre>


