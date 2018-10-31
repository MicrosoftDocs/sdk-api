---
UID: NF:commctrl.TabCtrl_SetItemSize
title: TabCtrl_SetItemSize macro
author: windows-sdk-content
description: Sets the width and height of tabs in a fixed-width or owner-drawn tab control. You can use this macro or send the TCM_SETITEMSIZE message explicitly.
old-location: controls\TabCtrl_SetItemSize.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_setitemsize.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: TabCtrl_SetItemSize, TabCtrl_SetItemSize macro [Windows Controls], _win32_TabCtrl_SetItemSize, _win32_TabCtrl_SetItemSize_cpp, commctrl/TabCtrl_SetItemSize, controls.TabCtrl_SetItemSize, controls._win32_TabCtrl_SetItemSize
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
 - TabCtrl_SetItemSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TabCtrl_SetItemSize macro


## -description


Sets the width and height of tabs in a fixed-width or owner-drawn tab control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb760635(v=VS.85).aspx">TCM_SETITEMSIZE</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

Handle to the tab control. 


### -param x

Type: <b>int</b>

New width, in pixels. 


### -param y

Type: <b>int</b>

New height, in pixels. 

