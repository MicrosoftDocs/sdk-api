---
UID: NF:windowsx.ListBox_GetItemRect
title: ListBox_GetItemRect macro
author: windows-sdk-content
description: Gets the dimensions of the rectangle that bounds a list box item as it is currently displayed in the list box. You can use this macro or send the LB_GETITEMRECT message explicitly.
old-location: controls\ListBox_GetItemRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_getitemrect.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ListBox_GetItemRect, ListBox_GetItemRect macro [Windows Controls], _win32_ListBox_GetItemRect, _win32_ListBox_GetItemRect_cpp, controls.ListBox_GetItemRect, controls._win32_ListBox_GetItemRect, windowsx/ListBox_GetItemRect
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
 - ListBox_GetItemRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListBox_GetItemRect macro


## -description


Gets the dimensions of the rectangle that bounds a list box item as it is currently displayed in the list box. You can use this macro or send the <a href="https://msdn.microsoft.com/84f94bc9-f7a4-4c2d-8c35-1bd291082af9">LB_GETITEMRECT</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param index

Type: <b>int</b>

The zero-based index of the item in the list box.


### -param lprc

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that receives the client coordinates for the item in the list box.

