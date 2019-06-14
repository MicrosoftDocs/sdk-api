---
UID: NF:commctrl.TabCtrl_SetCurFocus
title: TabCtrl_SetCurFocus macro (commctrl.h)
author: windows-sdk-content
description: Sets the focus to a specified tab in a tab control. You can use this macro or send the TCM_SETCURFOCUS message explicitly.
old-location: controls\TabCtrl_SetCurFocus.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_setcurfocus.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TabCtrl_SetCurFocus, TabCtrl_SetCurFocus macro [Windows Controls], _win32_TabCtrl_SetCurFocus, _win32_TabCtrl_SetCurFocus_cpp, commctrl/TabCtrl_SetCurFocus, controls.TabCtrl_SetCurFocus, controls._win32_TabCtrl_SetCurFocus
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
 - TabCtrl_SetCurFocus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TabCtrl_SetCurFocus macro


## -description


Sets the focus to a specified tab in a tab control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/tcm-setcurfocus">TCM_SETCURFOCUS</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tab control. 


### -param i

Type: <b>int</b>

Zero-based index of the tab that gets the focus. 


## -remarks



If the tab control has the <a href="https://docs.microsoft.com/windows/desktop/Controls/tab-control-styles">TCS_BUTTONS</a> style (button mode), the tab with the focus may be different from the selected tab. For example, when a tab is selected, the user can press the arrow keys to set the focus to a different tab without changing the selected tab. In button mode, the <b>TabCtrl_SetCurFocus</b> macro sets the input focus to the button associated with the specified tab, but it does not change the selected tab. 

If the tab control does not have the <a href="https://docs.microsoft.com/windows/desktop/Controls/tab-control-styles">TCS_BUTTONS</a> style, changing the focus also changes the selected tab. In this case, the tab control sends the <a href="https://docs.microsoft.com/windows/desktop/Controls/tcn-selchanging">TCN_SELCHANGING</a> and <a href="https://docs.microsoft.com/windows/desktop/Controls/tcn-selchange">TCN_SELCHANGE</a> notification codes to its parent window. 




## -see-also




<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/Controls/tcm-getcurfocus">TCM_GETCURFOCUS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-tabctrl_getcurfocus">TabCtrl_GetCurFocus</a>
 

 

