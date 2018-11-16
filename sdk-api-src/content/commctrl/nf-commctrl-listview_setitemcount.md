---
UID: NF:commctrl.ListView_SetItemCount
title: ListView_SetItemCount macro
author: windows-sdk-content
description: Causes the list-view control to allocate memory for the specified number of items. You can use this macro or send the LVM_SETITEMCOUNT message explicitly.
old-location: controls\ListView_SetItemCount.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setitemcount.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ListView_SetItemCount, ListView_SetItemCount macro [Windows Controls], _win32_ListView_SetItemCount, _win32_ListView_SetItemCount_cpp, commctrl/ListView_SetItemCount, controls.ListView_SetItemCount, controls._win32_ListView_SetItemCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- commctrl.h
: 
- ListView_SetItemCount
: 
---

# ListView_SetItemCount macro


## -description


Causes the list-view control to allocate memory for the specified number of items. You can use this macro or send the <a href="https://msdn.microsoft.com/5e794c12-ddcb-44fc-b0d2-677352602503">LVM_SETITEMCOUNT</a> message explicitly. 


## -parameters




### -param hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a list-view control. 


### -param cItems

Type: <b>int</b>

The number of items for which the list-view control should allocate memory.


## -remarks



If the list-view control was created without the <a href="List_view_window_styles.htm">LVS_OWNERDATA</a> style, this macro causes the control to allocate its internal data structures for the specified number of items. This prevents the control from having to allocate the data structures every time an item is added. 

If the list-view control was created with the <a href="List_view_window_styles.htm">LVS_OWNERDATA</a> style (a <a href="List_View_Controls_Overview.htm">virtual list view</a>), the <a href="https://msdn.microsoft.com/2d622109-102b-4288-a31d-43e2232f54b9">ListView_SetItemCountEx</a> macro should be used. 



