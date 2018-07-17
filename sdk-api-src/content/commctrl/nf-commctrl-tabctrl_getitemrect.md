---
UID: NF:commctrl.TabCtrl_GetItemRect
title: TabCtrl_GetItemRect macro
author: windows-sdk-content
description: Retrieves the bounding rectangle for a tab in a tab control. You can use this macro or send the TCM_GETITEMRECT message explicitly.
old-location: controls\TabCtrl_GetItemRect.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_getitemrect.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: TabCtrl_GetItemRect, TabCtrl_GetItemRect macro [Windows Controls], _win32_TabCtrl_GetItemRect, _win32_TabCtrl_GetItemRect_cpp, commctrl/TabCtrl_GetItemRect, controls.TabCtrl_GetItemRect, controls._win32_TabCtrl_GetItemRect
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
 - TabCtrl_GetItemRect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TabCtrl_GetItemRect macro


## -description


Retrieves the bounding rectangle for a tab in a tab control. You can use this macro or send the <a href="https://msdn.microsoft.com/library/Bb760594(v=VS.85).aspx">TCM_GETITEMRECT</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tab control. 


### -param i

TBD


### -param prc

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

Pointer to a structure that receives the bounding rectangle of the tab, in viewport coordinates. 


#### - iItem

Type: <b>int</b>

Index of the tab. 

