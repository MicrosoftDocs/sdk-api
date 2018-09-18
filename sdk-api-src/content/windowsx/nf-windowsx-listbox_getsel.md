---
UID: NF:windowsx.ListBox_GetSel
title: ListBox_GetSel macro
author: windows-sdk-content
description: Gets the selection state of an item. You can use this macro or send the LB_GETSEL message explicitly.
old-location: controls\ListBox_GetSel.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_getsel.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ListBox_GetSel, ListBox_GetSel macro [Windows Controls], _win32_ListBox_GetSel, _win32_ListBox_GetSel_cpp, controls.ListBox_GetSel, controls._win32_ListBox_GetSel, windowsx/ListBox_GetSel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: windowsx.h
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
 - Windowsx.h
api_name:
 - ListBox_GetSel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListBox_GetSel macro


## -description


Gets the selection state of an item. You can use this macro or send the <a href="https://msdn.microsoft.com/f92c02e7-3c6d-4649-8798-42eb4a0c51b6">LB_GETSEL</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param index

Type: <b>int</b>

The zero-based index of the item.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/f92c02e7-3c6d-4649-8798-42eb4a0c51b6">LB_GETSEL</a>




