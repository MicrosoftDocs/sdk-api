---
UID: NF:commctrl.TabCtrl_SetItem
title: TabCtrl_SetItem macro (commctrl.h)
description: Sets some or all of a tab's attributes. You can use this macro or send the TCM_SETITEM message explicitly.
helpviewer_keywords: ["TabCtrl_SetItem","TabCtrl_SetItem macro [Windows Controls]","_win32_TabCtrl_SetItem","_win32_TabCtrl_SetItem_cpp","commctrl/TabCtrl_SetItem","controls.TabCtrl_SetItem","controls._win32_TabCtrl_SetItem"]
old-location: controls\TabCtrl_SetItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_setitem.htm
ms.date: 12/05/2018
ms.keywords: TabCtrl_SetItem, TabCtrl_SetItem macro [Windows Controls], _win32_TabCtrl_SetItem, _win32_TabCtrl_SetItem_cpp, commctrl/TabCtrl_SetItem, controls.TabCtrl_SetItem, controls._win32_TabCtrl_SetItem
f1_keywords:
- commctrl/TabCtrl_SetItem
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
- TabCtrl_SetItem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TabCtrl_SetItem macro


## -description


Sets some or all of a tab's attributes. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/tcm-setitem">TCM_SETITEM</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tab control. 


### -param iItem

Type: <b>int</b>

Index of the item. 


### -param pitem

Type: <b>LPTCITEM</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-tcitema">TCITEM</a> structure that contains the new item attributes. The <b>mask</b> member specifies which attributes to set. If the <b>mask</b> member specifies the LVIF_TEXT value, the <b>pszText</b> member is the address of a null-terminated string and the <b>cchTextMax</b> member is ignored.

