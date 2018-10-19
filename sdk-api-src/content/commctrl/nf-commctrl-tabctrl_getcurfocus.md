---
UID: NF:commctrl.TabCtrl_GetCurFocus
title: TabCtrl_GetCurFocus macro
author: windows-sdk-content
description: Returns the index of the item that has the focus in a tab control. You can use this macro or send the TCM_GETCURFOCUS message explicitly.
old-location: controls\TabCtrl_GetCurFocus.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_getcurfocus.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: TabCtrl_GetCurFocus, TabCtrl_GetCurFocus macro [Windows Controls], _win32_TabCtrl_GetCurFocus, _win32_TabCtrl_GetCurFocus_cpp, commctrl/TabCtrl_GetCurFocus, controls.TabCtrl_GetCurFocus, controls._win32_TabCtrl_GetCurFocus
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
 - TabCtrl_GetCurFocus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TabCtrl_GetCurFocus macro


## -description


Returns the index of the item that has the focus in a tab control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb760581(v=VS.85).aspx">TCM_GETCURFOCUS</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

Handle to the tab control. 


## -remarks



The item that has the focus may be different than the selected item. 



