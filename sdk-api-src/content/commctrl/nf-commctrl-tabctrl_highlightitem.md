---
UID: NF:commctrl.TabCtrl_HighlightItem
title: TabCtrl_HighlightItem macro (commctrl.h)
description: Sets the highlight state of a tab item. You can use this macro or send the TCM_HIGHLIGHTITEM message explicitly.
helpviewer_keywords: ["TabCtrl_HighlightItem","TabCtrl_HighlightItem macro [Windows Controls]","_win32_TabCtrl_HighlightItem","_win32_TabCtrl_HighlightItem_cpp","commctrl/TabCtrl_HighlightItem","controls.TabCtrl_HighlightItem","controls._win32_TabCtrl_HighlightItem"]
old-location: controls\TabCtrl_HighlightItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_highlightitem.htm
ms.date: 12/05/2018
ms.keywords: TabCtrl_HighlightItem, TabCtrl_HighlightItem macro [Windows Controls], _win32_TabCtrl_HighlightItem, _win32_TabCtrl_HighlightItem_cpp, commctrl/TabCtrl_HighlightItem, controls.TabCtrl_HighlightItem, controls._win32_TabCtrl_HighlightItem
f1_keywords:
- commctrl/TabCtrl_HighlightItem
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
- TabCtrl_HighlightItem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TabCtrl_HighlightItem macro


## -description


Sets the highlight state of a tab item. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/tcm-highlightitem">TCM_HIGHLIGHTITEM</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tab control. 


### -param i

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">INT</a></b>

Zero-based index of a tab control item. 


### -param fHighlight

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">WORD</a></b>

Value specifying the highlight state to be set. If this value is nonzero, the tab is highlighted. If this value is zero, the tab is set to its default state. 


## -remarks



In Comctl32.dll version 6.0, this macro has no visible effect when a theme is active.



