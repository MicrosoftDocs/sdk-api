---
UID: NF:commctrl.TabCtrl_AdjustRect
title: TabCtrl_AdjustRect macro
author: windows-sdk-content
description: Calculates a tab control's display area given a window rectangle, or calculates the window rectangle that would correspond to a specified display area. You can use this macro or send the TCM_ADJUSTRECT message explicitly.
old-location: controls\TabCtrl_AdjustRect.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_adjustrect.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: TabCtrl_AdjustRect, TabCtrl_AdjustRect macro [Windows Controls], _win32_TabCtrl_AdjustRect, _win32_TabCtrl_AdjustRect_cpp, commctrl/TabCtrl_AdjustRect, controls.TabCtrl_AdjustRect, controls._win32_TabCtrl_AdjustRect
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
 - TabCtrl_AdjustRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TabCtrl_AdjustRect macro


## -description


Calculates a tab control's display area given a window rectangle, or calculates the window rectangle that would correspond to a specified display area. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb760573(v=VS.85).aspx">TCM_ADJUSTRECT</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tab control. 


### -param bLarger

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Operation to perform. If this parameter is <b>TRUE</b>, 
					<i>prc</i> specifies a display rectangle and receives the corresponding window rectangle. If this parameter is <b>FALSE</b>, 
					<i>prc</i> specifies a window rectangle and receives the corresponding display area. 


### -param prc

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that specifies the given rectangle and receives the calculated rectangle. 


## -remarks



This message applies only to tab controls that are at the top. It does not apply to tab controls that are on the sides or bottom.



