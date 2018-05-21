---
UID: NF:windowsx.ListBox_SelItemRange
title: ListBox_SelItemRange macro
author: windows-driver-content
description: Selects or deselects one or more consecutive items in a multiple-selection list box. You can use this macro or send the LB_SELITEMRANGE message explicitly.
old-location: controls\ListBox_SelItemRange.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_selitemrange.htm
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: ListBox_SelItemRange, ListBox_SelItemRange macro [Windows Controls], _win32_ListBox_SelItemRange, _win32_ListBox_SelItemRange_cpp, controls.ListBox_SelItemRange, controls._win32_ListBox_SelItemRange, windowsx/ListBox_SelItemRange
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
req.typenames: HANDLE_SHARING_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Windowsx.h
api_name:
-	ListBox_SelItemRange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# ListBox_SelItemRange macro


## -description


Selects or deselects one or more consecutive items in a multiple-selection list box. You can use this macro or send the <a href="https://msdn.microsoft.com/817d62df-98a3-40b3-8d62-86bf07ad797f">LB_SELITEMRANGE</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param fSelect

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> to select the range of items, or <b>FALSE</b> to deselect it.


### -param first

Type: <b>int</b>

The zero-based index of the first item to select.


### -param last

Type: <b>int</b>

The zero-based index of the last item to select.

