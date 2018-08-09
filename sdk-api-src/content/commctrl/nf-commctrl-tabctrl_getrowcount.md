---
UID: NF:commctrl.TabCtrl_GetRowCount
title: TabCtrl_GetRowCount macro
author: windows-sdk-content
description: Retrieves the current number of rows of tabs in a tab control. You can use this macro or send the TCM_GETROWCOUNT message explicitly.
old-location: controls\TabCtrl_GetRowCount.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_getrowcount.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TabCtrl_GetRowCount, TabCtrl_GetRowCount macro [Windows Controls], _win32_TabCtrl_GetRowCount, _win32_TabCtrl_GetRowCount_cpp, commctrl/TabCtrl_GetRowCount, controls.TabCtrl_GetRowCount, controls._win32_TabCtrl_GetRowCount
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
 - TabCtrl_GetRowCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TabCtrl_GetRowCount macro


## -description


Retrieves the current number of rows of tabs in a tab control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb760596(v=VS.85).aspx">TCM_GETROWCOUNT</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tab control. 


## -remarks



Only tab controls that have the <a href="Tab_Control_Styles.htm">TCS_MULTILINE</a> style can have multiple rows of tabs. 



