---
UID: NF:commctrl.ListView_SetCheckState
title: ListView_SetCheckState macro (commctrl.h)
description: Selects or deselects an item in a list-view control. You can use this macro or send the LVM_SETITEMSTATE message explicitly.
helpviewer_keywords: ["ListView_SetCheckState","ListView_SetCheckState macro [Windows Controls]","_win32_ListView_SetCheckState","_win32_ListView_SetCheckState_cpp","commctrl/ListView_SetCheckState","controls.ListView_SetCheckState","controls._win32_ListView_SetCheckState"]
old-location: controls\ListView_SetCheckState.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setcheckstate.htm
ms.date: 12/05/2018
ms.keywords: ListView_SetCheckState, ListView_SetCheckState macro [Windows Controls], _win32_ListView_SetCheckState, _win32_ListView_SetCheckState_cpp, commctrl/ListView_SetCheckState, controls.ListView_SetCheckState, controls._win32_ListView_SetCheckState
f1_keywords:
- commctrl/ListView_SetCheckState
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
- ListView_SetCheckState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_SetCheckState macro


## -description


Selects or deselects an item in a list-view control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-setitemstate">LVM_SETITEMSTATE</a> message explicitly.


## -parameters




### -param hwndLV

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a list-view control. 


### -param i

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the item for which to set the check state. 


### -param fCheck

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

A value that is set to <b>TRUE</b> to select the item, or <b>FALSE</b> to deselect it. 


## -remarks



This macro should only be used for list-view controls with the <a href="https://docs.microsoft.com/windows/desktop/Controls/extended-list-view-styles">LVS_EX_CHECKBOXES</a> style. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-listview_setitemstate">ListView_SetItemState</a>
 

 

