---
UID: NF:commctrl.TabCtrl_GetToolTips
title: TabCtrl_GetToolTips macro
author: windows-sdk-content
description: Retrieves the handle to the tooltip control associated with a tab control. You can use this macro or send the TCM_GETTOOLTIPS message explicitly.
old-location: controls\TabCtrl_GetToolTips.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_gettooltips.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: TabCtrl_GetToolTips, TabCtrl_GetToolTips macro [Windows Controls], _win32_TabCtrl_GetToolTips, _win32_TabCtrl_GetToolTips_cpp, commctrl/TabCtrl_GetToolTips, controls.TabCtrl_GetToolTips, controls._win32_TabCtrl_GetToolTips
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: STGOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - TabCtrl_GetToolTips
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TabCtrl_GetToolTips macro


## -description


Retrieves the handle to the tooltip control associated with a tab control. You can use this macro or send the <a href="https://msdn.microsoft.com/library/Bb760598(v=VS.85).aspx">TCM_GETTOOLTIPS</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tab control. 


## -remarks



A tab control creates a tooltip control if it has the <a href="https://msdn.microsoft.com/library/Bb760549(v=VS.85).aspx">TCS_TOOLTIPS</a>. You can also assign a tooltip control to a tab control by using the <a href="https://msdn.microsoft.com/library/Bb760641(v=VS.85).aspx">TCM_SETTOOLTIPS</a> message. 



