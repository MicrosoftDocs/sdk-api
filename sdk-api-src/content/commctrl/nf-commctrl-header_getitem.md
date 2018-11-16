---
UID: NF:commctrl.Header_GetItem
title: Header_GetItem macro
author: windows-sdk-content
description: Gets information about an item in a header control. You can use this macro or send the HDM_GETITEM message explicitly.
old-location: controls\Header_GetItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_getitem.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Header_GetItem, Header_GetItem macro [Windows Controls], _win32_Header_GetItem, _win32_Header_GetItem_cpp, commctrl/Header_GetItem, controls.Header_GetItem, controls._win32_Header_GetItem
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
 - Header_GetItem
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
- Header_GetItem
: 
---

# Header_GetItem macro


## -description


Gets information about an item in a header control. You can use this macro or send the <a href="https://msdn.microsoft.com/fb1330d3-fd28-490c-9caa-4b2b5ff86ba0">HDM_GETITEM</a> message explicitly. 


## -parameters




### -param hwndHD

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the header control. 


### -param i

Type: <b>int</b>

The index of the item for which information is to be retrieved. 


### -param phdi

Type: <b>LPHDITEM</b>

A pointer to an <a href="https://msdn.microsoft.com/2a717394-9123-409d-bda9-8e4ac6534101">HDITEM</a> structure. When the message is sent, the <b>mask</b> member indicates the type of information being requested. When the message returns, the other members receive the requested information. If the 
<b>mask</b> member specifies zero, the message returns <b>TRUE</b> but copies no information to the structure. 


## -remarks



If the HDI_TEXT flag is set in the 
				<b>mask</b> member of the <a href="https://msdn.microsoft.com/2a717394-9123-409d-bda9-8e4ac6534101">HDITEM</a> structure, the control may change the 
				<b>pszText</b> member of the structure to point to the new text instead of filling the buffer with the requested text. Applications should not assume that the text will always be placed in the requested buffer.

The <b>Header_GetItem</b> macro is defined as follows:

<pre class="syntax" xml:space="preserve"><code>#define Header_GetItem(hwndHD, index, phdi)      \

    (BOOL)SendMessage((hwndHD), HDM_GETITEM,   \

    (WPARAM)(int)(index), (LPARAM)(LPHDITEM)(phdi))</code></pre>


