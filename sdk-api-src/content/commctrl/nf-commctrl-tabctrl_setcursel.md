---
UID: NF:commctrl.TabCtrl_SetCurSel
title: TabCtrl_SetCurSel macro
author: windows-sdk-content
description: Selects a tab in a tab control. You can use this macro or send the TCM_SETCURSEL message explicitly.
old-location: controls\TabCtrl_SetCurSel.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_setcursel.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
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


Selects a tab in a tab control. You can use this macro or send the <a href="https://msdn.microsoft.com/cf709d8c-c522-47c8-8ff3-463dc8e924b5">TCM_SETCURSEL</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tab control. 


### -param i

Type: <b>int</b>

Index of the tab to select. 


## -remarks



A tab control does not send a <a href="https://msdn.microsoft.com/ec7b1bd3-8932-4418-9eed-ecb7c748e4dd">TCN_SELCHANGING</a> or <a href="https://msdn.microsoft.com/f40e30f6-169b-4381-a300-12c3befb5fc5">TCN_SELCHANGE</a> notification code when a tab is selected using the <a href="https://msdn.microsoft.com/cf709d8c-c522-47c8-8ff3-463dc8e924b5">TCM_SETCURSEL</a> message. 



