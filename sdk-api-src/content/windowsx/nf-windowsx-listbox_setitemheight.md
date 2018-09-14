---
UID: NF:windowsx.ListBox_SetItemHeight
title: ListBox_SetItemHeight macro
author: windows-sdk-content
description: Sets the height of items in a list box.
old-location: controls\ListBox_SetItemHeight.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_setitemheight.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ListBox_SetItemHeight, ListBox_SetItemHeight macro [Windows Controls], _win32_ListBox_SetItemHeight, _win32_ListBox_SetItemHeight_cpp, controls.ListBox_SetItemHeight, controls._win32_ListBox_SetItemHeight, windowsx/ListBox_SetItemHeight
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
 - ListBox_SetItemHeight
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListBox_SetItemHeight macro


## -description


Sets the height of items in a list box. If the list box has the <a href="List_Box_Styles.htm">LBS_OWNERDRAWVARIABLE</a> style, this macro sets the height of the specified item; otherwise, it sets the height of all items. You can use this macro or send the <a href="https://msdn.microsoft.com/3ac8e935-6de8-465f-a525-1f493b06ee7c">LB_SETITEMHEIGHT</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param index

Type: <b>int</b>

The zero-based index of the item. If the list box does not have the <a href="List_Box_Styles.htm">LBS_OWNERDRAWVARIABLE</a> style, set this parameter to zero. 


### -param cy

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

The height of the item or items, in pixels.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/3ac8e935-6de8-465f-a525-1f493b06ee7c">LB_SETITEMHEIGHT</a>.
	



