---
UID: NF:commctrl.TabCtrl_DeselectAll
title: TabCtrl_DeselectAll macro
author: windows-sdk-content
description: Resets items in a tab control, clearing any that were set to the TCIS_BUTTONPRESSED state. You can use this macro or send the TCM_DESELECTALL message explicitly.
old-location: controls\TabCtrl_DeselectAll.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_deselectall.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: TabCtrl_DeselectAll, TabCtrl_DeselectAll macro [Windows Controls], _win32_TabCtrl_DeselectAll, _win32_TabCtrl_DeselectAll_cpp, commctrl/TabCtrl_DeselectAll, controls.TabCtrl_DeselectAll, controls._win32_TabCtrl_DeselectAll
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
 - TabCtrl_DeselectAll
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
- TabCtrl_DeselectAll
: 
---

# TabCtrl_DeselectAll macro


## -description


Resets items in a tab control, clearing any that were set to the <a href="https://msdn.microsoft.com/en-us/library/Bb760547(v=VS.85).aspx">TCIS_BUTTONPRESSED</a> state. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb760579(v=VS.85).aspx">TCM_DESELECTALL</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

Handle to the tab control. 


### -param fExcludeFocus

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Flag value that specifies the scope of the item deselection. If this parameter is set to <b>FALSE</b>, all tab items will be reset. If it is set to <b>TRUE</b>, all but the currently selected tab item will be reset. 


## -remarks



This message is only meaningful if the <a href="https://msdn.microsoft.com/en-us/library/Bb760549(v=VS.85).aspx">TCS_BUTTONS</a> style flag has been set. 



