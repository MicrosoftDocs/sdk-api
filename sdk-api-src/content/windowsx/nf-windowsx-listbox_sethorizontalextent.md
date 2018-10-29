---
UID: NF:windowsx.ListBox_SetHorizontalExtent
title: ListBox_SetHorizontalExtent macro
author: windows-sdk-content
description: Set the width by which a list box can be scrolled horizontally (the scrollable width).
old-location: controls\ListBox_SetHorizontalExtent.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_sethorizontalextent.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ListBox_SetHorizontalExtent, ListBox_SetHorizontalExtent macro [Windows Controls], _win32_ListBox_SetHorizontalExtent, _win32_ListBox_SetHorizontalExtent_cpp, controls.ListBox_SetHorizontalExtent, controls._win32_ListBox_SetHorizontalExtent, windowsx/ListBox_SetHorizontalExtent
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
 - ListBox_SetHorizontalExtent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListBox_SetHorizontalExtent macro


## -description


Set the width by which a list box can be scrolled horizontally (the scrollable width). If the width of the list box is smaller than this value, the horizontal scroll bar horizontally scrolls items in the list box. If the width of the list box is equal to or greater than this value, the horizontal scroll bar is hidden. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761344(v=VS.85).aspx">LB_SETHORIZONTALEXTENT</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param cxExtent

Type: <b>int</b>

The number of pixels by which the list box can be scrolled. 


## -remarks



For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb761344(v=VS.85).aspx">LB_SETHORIZONTALEXTENT</a>.
	



