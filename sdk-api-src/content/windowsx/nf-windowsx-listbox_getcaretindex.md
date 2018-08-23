---
UID: NF:windowsx.ListBox_GetCaretIndex
title: ListBox_GetCaretIndex macro
author: windows-sdk-content
description: Retrieves the index of the list box item that has the focus rectangle in a multiple-selection list box. The item may or may not be selected. You can use this macro or send the LB_GETCARETINDEX message explicitly.
old-location: controls\ListBox_GetCaretIndex.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_getcaretindex.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ListBox_GetCaretIndex, ListBox_GetCaretIndex macro [Windows Controls], _win32_ListBox_GetCaretIndex, _win32_ListBox_GetCaretIndex_cpp, controls.ListBox_GetCaretIndex, controls._win32_ListBox_GetCaretIndex, windowsx/ListBox_GetCaretIndex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: windowsx.h
req.include-header: 
req.redist: 
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
 - ListBox_GetCaretIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# ListBox_GetCaretIndex macro


## -description


Retrieves the index of the list box item that has the focus rectangle in a multiple-selection list box. The item may or may not be selected. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775193(v=VS.85).aspx">LB_GETCARETINDEX</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


## -remarks



The contents of the list box are scrolled till the item is fully visible.

For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb775193(v=VS.85).aspx">LB_GETCARETINDEX</a>.



