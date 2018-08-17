---
UID: NF:commctrl.TabCtrl_SetPadding
title: TabCtrl_SetPadding macro
author: windows-sdk-content
description: Sets the amount of space (padding) around each tab's icon and label in a tab control. You can use this macro or send the TCM_SETPADDING message explicitly.
old-location: controls\TabCtrl_SetPadding.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_setpadding.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TabCtrl_SetPadding, TabCtrl_SetPadding macro [Windows Controls], _win32_TabCtrl_SetPadding, _win32_TabCtrl_SetPadding_cpp, commctrl/TabCtrl_SetPadding, controls.TabCtrl_SetPadding, controls._win32_TabCtrl_SetPadding
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.redist: 
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
 - TabCtrl_SetPadding
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TabCtrl_SetPadding macro


## -description


Sets the amount of space (padding) around each tab's icon and label in a tab control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb760639(v=VS.85).aspx">TCM_SETPADDING</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

Handle to the tab control. 


### -param cx

Type: <b>int</b>

Amount of horizontal padding, in pixels. 


### -param cy

Type: <b>int</b>

Amount of vertical padding, in pixels. 

