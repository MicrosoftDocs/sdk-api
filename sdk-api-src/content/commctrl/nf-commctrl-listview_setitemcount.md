---
UID: NF:commctrl.ListView_SetItemCount
title: ListView_SetItemCount macro (commctrl.h)
description: Causes the list-view control to allocate memory for the specified number of items. You can use this macro or send the LVM_SETITEMCOUNT message explicitly.helpviewer_keywords: ["ListView_SetItemCount","ListView_SetItemCount macro [Windows Controls]","_win32_ListView_SetItemCount","_win32_ListView_SetItemCount_cpp","commctrl/ListView_SetItemCount","controls.ListView_SetItemCount","controls._win32_ListView_SetItemCount"]
old-location: controls\ListView_SetItemCount.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setitemcount.htm
ms.date: 12/05/2018
ms.keywords: ListView_SetItemCount, ListView_SetItemCount macro [Windows Controls], _win32_ListView_SetItemCount, _win32_ListView_SetItemCount_cpp, commctrl/ListView_SetItemCount, controls.ListView_SetItemCount, controls._win32_ListView_SetItemCount
f1_keywords:
- commctrl/ListView_SetItemCount
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
- ListView_SetItemCount
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_SetItemCount macro


## -description


Causes the list-view control to allocate memory for the specified number of items. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-setitemcount">LVM_SETITEMCOUNT</a> message explicitly. 


## -parameters




### -param hwndLV

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a list-view control. 


### -param cItems

Type: <b>int</b>

The number of items for which the list-view control should allocate memory.


## -remarks



If the list-view control was created without the <a href="https://docs.microsoft.com/windows/desktop/Controls/list-view-window-styles">LVS_OWNERDATA</a> style, this macro causes the control to allocate its internal data structures for the specified number of items. This prevents the control from having to allocate the data structures every time an item is added. 

If the list-view control was created with the <a href="https://docs.microsoft.com/windows/desktop/Controls/list-view-window-styles">LVS_OWNERDATA</a> style (a <a href="https://docs.microsoft.com/windows/desktop/Controls/list-view-controls-overview">virtual list view</a>), the <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-listview_setitemcountex">ListView_SetItemCountEx</a> macro should be used. 



