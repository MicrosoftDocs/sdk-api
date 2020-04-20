---
UID: NF:commctrl.Header_SetItem
title: Header_SetItem macro (commctrl.h)
description: Sets the attributes of the specified item in a header control. You can use this macro or send the HDM_SETITEM message explicitly.helpviewer_keywords: ["Header_SetItem","Header_SetItem macro [Windows Controls]","_win32_Header_SetItem","_win32_Header_SetItem_cpp","commctrl/Header_SetItem","controls.Header_SetItem","controls._win32_Header_SetItem"]
old-location: controls\Header_SetItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_setitem.htm
ms.date: 12/05/2018
ms.keywords: Header_SetItem, Header_SetItem macro [Windows Controls], _win32_Header_SetItem, _win32_Header_SetItem_cpp, commctrl/Header_SetItem, controls.Header_SetItem, controls._win32_Header_SetItem
f1_keywords:
- commctrl/Header_SetItem
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
- Header_SetItem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Header_SetItem macro


## -description


Sets the attributes of the specified item in a header control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/hdm-setitem">HDM_SETITEM</a> message explicitly. 


## -parameters




### -param hwndHD

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a header control. 


### -param i

Type: <b>int</b>

The current index of the item whose attributes are to be changed. 


### -param phdi

Type: <b>LPHDITEM</b>

A pointer to an <a href="https://docs.microsoft.com/windows/win32/api/commctrl/ns-commctrl-hditema">HDITEM</a> structure that contains item information. When this message is sent, the 
					<b>mask</b> member of the structure must be set to indicate which attributes are being set. 


## -remarks



The <a href="https://docs.microsoft.com/windows/win32/api/commctrl/ns-commctrl-hditema">HDITEM</a> structure that supports this macro supports item order and image list information. By using these members, you can control the order in which items are displayed and specify images to appear with items. 



