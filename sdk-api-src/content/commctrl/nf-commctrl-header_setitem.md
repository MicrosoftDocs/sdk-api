---
UID: NF:commctrl.Header_SetItem
title: Header_SetItem macro
author: windows-sdk-content
description: Sets the attributes of the specified item in a header control. You can use this macro or send the HDM_SETITEM message explicitly.
old-location: controls\Header_SetItem.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\header\macros\header_setitem.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: Header_SetItem, Header_SetItem macro [Windows Controls], _win32_Header_SetItem, _win32_Header_SetItem_cpp, commctrl/Header_SetItem, controls.Header_SetItem, controls._win32_Header_SetItem
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
 - Header_SetItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Header_SetItem macro


## -description


Sets the attributes of the specified item in a header control. You can use this macro or send the <a href="https://msdn.microsoft.com/c8f0d526-3ebe-48c5-8aea-ea3703e2d983">HDM_SETITEM</a> message explicitly. 


## -parameters




### -param hwndHD

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a header control. 


### -param i

Type: <b>int</b>

The current index of the item whose attributes are to be changed. 


### -param phdi

Type: <b>LPHDITEM</b>

A pointer to an <a href="https://msdn.microsoft.com/2a717394-9123-409d-bda9-8e4ac6534101">HDITEM</a> structure that contains item information. When this message is sent, the 
					<b>mask</b> member of the structure must be set to indicate which attributes are being set. 


## -remarks



The <a href="https://msdn.microsoft.com/2a717394-9123-409d-bda9-8e4ac6534101">HDITEM</a> structure that supports this macro supports item order and image list information. By using these members, you can control the order in which items are displayed and specify images to appear with items. 



