---
UID: NF:windowsx.ListBox_SetTopIndex
title: ListBox_SetTopIndex macro
author: windows-driver-content
description: Ensures that the specified item in a list box is visible. You can use this macro or send the LB_SETTOPINDEX message explicitly.
old-location: controls\ListBox_SetTopIndex.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_settopindex.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ListBox_SetTopIndex, ListBox_SetTopIndex macro [Windows Controls], _win32_ListBox_SetTopIndex, _win32_ListBox_SetTopIndex_cpp, controls.ListBox_SetTopIndex, controls._win32_ListBox_SetTopIndex, windowsx/ListBox_SetTopIndex
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
-	ListBox_SetTopIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# ListBox_SetTopIndex macro


## -description


Ensures that the specified item in a list box is visible. You can use this macro or send the <a href="https://msdn.microsoft.com/0e938cd1-7d6c-4b81-91b2-f388465c5d7e">LB_SETTOPINDEX</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param indexTop

TBD






#### - index

Type: <b>int</b>

The zero-based index of the item to put at the top of the visible part of the list.


## -remarks



The list box contents are scrolled so that either the specified item appears at the top of the list box or the maximum scroll range has been reached.



