---
UID: NF:commctrl.TabCtrl_SetToolTips
title: TabCtrl_SetToolTips macro
author: windows-sdk-content
description: Assigns a tooltip control to a tab control. You can use this macro or send the TCM_SETTOOLTIPS message explicitly.
old-location: controls\TabCtrl_SetToolTips.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_settooltips.htm
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: TabCtrl_SetToolTips, TabCtrl_SetToolTips macro [Windows Controls], _win32_TabCtrl_SetToolTips, _win32_TabCtrl_SetToolTips_cpp, commctrl/TabCtrl_SetToolTips, controls.TabCtrl_SetToolTips, controls._win32_TabCtrl_SetToolTips
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
 - TabCtrl_SetToolTips
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TabCtrl_SetToolTips macro


## -description


Assigns a tooltip control to a tab control. You can use this macro or send the <a href="https://msdn.microsoft.com/c1b173b1-9da6-441a-a2b6-3875e2c343f8">TCM_SETTOOLTIPS</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tab control. 


### -param hwndTT

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tooltip control. 


## -remarks



You can retrieve the tooltip control associated with a tab control by using the <a href="https://msdn.microsoft.com/d7dcca4f-8629-4eeb-844f-b3171438f528">TCM_GETTOOLTIPS</a> message. 



