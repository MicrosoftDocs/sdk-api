---
UID: NF:windowsx.ListBox_SetHorizontalExtent
title: ListBox_SetHorizontalExtent macro
author: windows-sdk-content
description: Set the width by which a list box can be scrolled horizontally (the scrollable width).
old-location: controls\ListBox_SetHorizontalExtent.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_sethorizontalextent.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ListBox_SetHorizontalExtent, ListBox_SetHorizontalExtent macro [Windows Controls], _win32_ListBox_SetHorizontalExtent, _win32_ListBox_SetHorizontalExtent_cpp, controls.ListBox_SetHorizontalExtent, controls._win32_ListBox_SetHorizontalExtent, windowsx/ListBox_SetHorizontalExtent
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: HANDLE_SHARING_OPTIONS
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# ListBox_SetHorizontalExtent macro


## -description


Set the width by which a list box can be scrolled horizontally (the scrollable width). If the width of the list box is smaller than this value, the horizontal scroll bar horizontally scrolls items in the list box. If the width of the list box is equal to or greater than this value, the horizontal scroll bar is hidden. You can use this macro or send the <a href="https://msdn.microsoft.com/7d59b6de-2a22-4246-936b-4c669d285392">LB_SETHORIZONTALEXTENT</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param cxExtent

Type: <b>int</b>

The number of pixels by which the list box can be scrolled. 


## -remarks



For more information, see <a href="https://msdn.microsoft.com/7d59b6de-2a22-4246-936b-4c669d285392">LB_SETHORIZONTALEXTENT</a>.
	



