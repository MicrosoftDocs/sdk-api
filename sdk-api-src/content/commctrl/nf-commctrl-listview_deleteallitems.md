---
UID: NF:commctrl.ListView_DeleteAllItems
title: ListView_DeleteAllItems macro (commctrl.h)
description: Removes all items from a list-view control. You can use this macro or send the LVM_DELETEALLITEMS message explicitly.
helpviewer_keywords: ["ListView_DeleteAllItems","ListView_DeleteAllItems macro [Windows Controls]","_win32_ListView_DeleteAllItems","_win32_ListView_DeleteAllItems_cpp","commctrl/ListView_DeleteAllItems","controls.ListView_DeleteAllItems","controls._win32_ListView_DeleteAllItems"]
old-location: controls\ListView_DeleteAllItems.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_deleteallitems.htm
ms.date: 12/05/2018
ms.keywords: ListView_DeleteAllItems, ListView_DeleteAllItems macro [Windows Controls], _win32_ListView_DeleteAllItems, _win32_ListView_DeleteAllItems_cpp, commctrl/ListView_DeleteAllItems, controls.ListView_DeleteAllItems, controls._win32_ListView_DeleteAllItems
f1_keywords:
- commctrl/ListView_DeleteAllItems
dev_langs:
- c++
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
- ListView_DeleteAllItems
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_DeleteAllItems macro


## -description


Removes all items from a list-view control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-deleteallitems">LVM_DELETEALLITEMS</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control. 


## -remarks



When a list-view control receives the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-deleteallitems">LVM_DELETEALLITEMS</a> message, it sends the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvn-deleteallitems">LVN_DELETEALLITEMS</a> notification code to its parent window. 



