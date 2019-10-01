---
UID: NF:commctrl.TabCtrl_GetCurFocus
title: TabCtrl_GetCurFocus macro (commctrl.h)
author: windows-sdk-content
description: Returns the index of the item that has the focus in a tab control. You can use this macro or send the TCM_GETCURFOCUS message explicitly.
old-location: controls\TabCtrl_GetCurFocus.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_getcurfocus.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TabCtrl_GetCurFocus, TabCtrl_GetCurFocus macro [Windows Controls], _win32_TabCtrl_GetCurFocus, _win32_TabCtrl_GetCurFocus_cpp, commctrl/TabCtrl_GetCurFocus, controls.TabCtrl_GetCurFocus, controls._win32_TabCtrl_GetCurFocus
ms.topic: macro
f1_keywords: 
 - "commctrl/TabCtrl_GetCurFocus"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TabCtrl_GetCurFocus macro


## -description


Returns the index of the item that has the focus in a tab control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/tcm-getcurfocus">TCM_GETCURFOCUS</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tab control. 


## -remarks



The item that has the focus may be different than the selected item. 



