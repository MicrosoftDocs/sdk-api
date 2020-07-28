---
UID: NF:commctrl.ListView_GetCheckState
title: ListView_GetCheckState macro (commctrl.h)
description: Determines if an item in a list-view control is selected. This should be used only for list-view controls that have the LVS_EX_CHECKBOXES style.
helpviewer_keywords: ["ListView_GetCheckState","ListView_GetCheckState macro [Windows Controls]","_win32_ListView_GetCheckState","_win32_ListView_GetCheckState_cpp","commctrl/ListView_GetCheckState","controls.ListView_GetCheckState","controls._win32_ListView_GetCheckState"]
old-location: controls\ListView_GetCheckState.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getcheckstate.htm
ms.date: 12/05/2018
ms.keywords: ListView_GetCheckState, ListView_GetCheckState macro [Windows Controls], _win32_ListView_GetCheckState, _win32_ListView_GetCheckState_cpp, commctrl/ListView_GetCheckState, controls.ListView_GetCheckState, controls._win32_ListView_GetCheckState
f1_keywords:
- commctrl/ListView_GetCheckState
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
- ListView_GetCheckState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_GetCheckState macro


## -description


Determines if an item in a list-view control is selected. This should be used only for list-view controls that have the <a href="https://docs.microsoft.com/windows/desktop/Controls/extended-list-view-styles">LVS_EX_CHECKBOXES</a> style. 


## -parameters




### -param hwndLV

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a list-view control. 


### -param i

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the item for which to retrieve the check state. 

