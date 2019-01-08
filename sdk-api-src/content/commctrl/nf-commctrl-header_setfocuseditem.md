---
UID: NF:commctrl.Header_SetFocusedItem
title: Header_SetFocusedItem macro
author: windows-sdk-content
description: Sets the focus to a specified item in a header control. Use this macro or send the HDM_SETFOCUSEDITEM message explicitly.
old-location: controls\Header_SetFocusedItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_setfocuseditem.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Header_SetFocusedItem, Header_SetFocusedItem macro [Windows Controls], _shell_Header_SetFocusedItem, _shell_Header_SetFocusedItem_cpp, commctrl/Header_SetFocusedItem, controls.Header_SetFocusedItem, controls._shell_Header_SetFocusedItem
ms.topic: macro
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - Header_SetFocusedItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Header_SetFocusedItem macro


## -description


Sets the focus to a specified item in a header control. Use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775361(v=VS.85).aspx">HDM_SETFOCUSEDITEM</a> message explicitly.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the header control.


### -param iItem [in]

Type: <b>int</b>

The index of item.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb775238(v=VS.85).aspx">About Header Controls</a>
 

 

