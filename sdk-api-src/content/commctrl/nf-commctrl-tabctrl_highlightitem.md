---
UID: NF:commctrl.TabCtrl_HighlightItem
title: TabCtrl_HighlightItem macro
author: windows-sdk-content
description: Sets the highlight state of a tab item. You can use this macro or send the TCM_HIGHLIGHTITEM message explicitly.
old-location: controls\TabCtrl_HighlightItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_highlightitem.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: TabCtrl_HighlightItem, TabCtrl_HighlightItem macro [Windows Controls], _win32_TabCtrl_HighlightItem, _win32_TabCtrl_HighlightItem_cpp, commctrl/TabCtrl_HighlightItem, controls.TabCtrl_HighlightItem, controls._win32_TabCtrl_HighlightItem
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
 - TabCtrl_HighlightItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TabCtrl_HighlightItem macro


## -description


Sets the highlight state of a tab item. You can use this macro or send the <a href="https://msdn.microsoft.com/b0d0850a-62d9-46a1-8846-81f67a886ea8">TCM_HIGHLIGHTITEM</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tab control. 


### -param i

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

Zero-based index of a tab control item. 


### -param fHighlight

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WORD</a></b>

Value specifying the highlight state to be set. If this value is nonzero, the tab is highlighted. If this value is zero, the tab is set to its default state. 


## -remarks



In Comctl32.dll version 6.0, this macro has no visible effect when a theme is active.



