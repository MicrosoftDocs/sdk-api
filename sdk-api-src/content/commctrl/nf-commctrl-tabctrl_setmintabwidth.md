---
UID: NF:commctrl.TabCtrl_SetMinTabWidth
title: TabCtrl_SetMinTabWidth macro
author: windows-sdk-content
description: Sets the minimum width of items in a tab control. You can use this macro or send the TCM_SETMINTABWIDTH message explicitly.
old-location: controls\TabCtrl_SetMinTabWidth.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_setmintabwidth.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: TabCtrl_SetMinTabWidth, TabCtrl_SetMinTabWidth macro [Windows Controls], _win32_TabCtrl_SetMinTabWidth, _win32_TabCtrl_SetMinTabWidth_cpp, commctrl/TabCtrl_SetMinTabWidth, controls.TabCtrl_SetMinTabWidth, controls._win32_TabCtrl_SetMinTabWidth
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
 - TabCtrl_SetMinTabWidth
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TabCtrl_SetMinTabWidth macro


## -description


Sets the minimum width of items in a tab control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb760637(v=VS.85).aspx">TCM_SETMINTABWIDTH</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

Handle to the tab control. 


### -param x

Type: <b>int</b>

Minimum width to be set for a tab control item. If this parameter is set to -1, the control will use the default tab width. 

