---
UID: NF:commctrl.TabCtrl_SetCurSel
title: TabCtrl_SetCurSel macro
author: windows-sdk-content
description: Selects a tab in a tab control. You can use this macro or send the TCM_SETCURSEL message explicitly.
old-location: controls\TabCtrl_SetCurSel.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_setcursel.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: TabCtrl_SetCurSel, TabCtrl_SetCurSel macro [Windows Controls], _win32_TabCtrl_SetCurSel, _win32_TabCtrl_SetCurSel_cpp, commctrl/TabCtrl_SetCurSel, controls.TabCtrl_SetCurSel, controls._win32_TabCtrl_SetCurSel
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
 - TabCtrl_SetCurSel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TabCtrl_SetCurSel macro


## -description


Selects a tab in a tab control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb760612(v=VS.85).aspx">TCM_SETCURSEL</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

Handle to the tab control. 


### -param i

Type: <b>int</b>

Index of the tab to select. 


## -remarks



A tab control does not send a <a href="https://msdn.microsoft.com/en-us/library/Bb760571(v=VS.85).aspx">TCN_SELCHANGING</a> or <a href="https://msdn.microsoft.com/en-us/library/Bb760569(v=VS.85).aspx">TCN_SELCHANGE</a> notification code when a tab is selected using the <a href="https://msdn.microsoft.com/en-us/library/Bb760612(v=VS.85).aspx">TCM_SETCURSEL</a> message. 



