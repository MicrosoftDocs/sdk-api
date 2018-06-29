---
UID: NF:commctrl.TabCtrl_SetItemExtra
title: TabCtrl_SetItemExtra macro
author: windows-sdk-content
description: Sets the number of bytes per tab reserved for application-defined data in a tab control. You can use this macro or send the TCM_SETITEMEXTRA message explicitly.
old-location: controls\TabCtrl_SetItemExtra.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_setitemextra.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: TabCtrl_SetItemExtra, TabCtrl_SetItemExtra macro [Windows Controls], _win32_TabCtrl_SetItemExtra, _win32_TabCtrl_SetItemExtra_cpp, commctrl/TabCtrl_SetItemExtra, controls.TabCtrl_SetItemExtra, controls._win32_TabCtrl_SetItemExtra
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
 - TabCtrl_SetItemExtra
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TabCtrl_SetItemExtra macro


## -description


Sets the number of bytes per tab reserved for application-defined data in a tab control. You can use this macro or send the <a href="https://msdn.microsoft.com/library/Bb760633(v=VS.85).aspx">TCM_SETITEMEXTRA</a> message explicitly. 


## -parameters




### -param hwndTC

TBD


### -param cb

Type: <b>int</b>

Number of extra bytes.


#### - hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tab control. 


## -remarks



By default, the number of extra bytes is four. An application that changes the number of extra bytes cannot use the <a href="https://msdn.microsoft.com/library/Bb760554(v=VS.85).aspx">TCITEM</a> structure to retrieve and set the application-defined data for a tab. Instead, you must define a new structure that consists of the <a href="https://msdn.microsoft.com/library/Bb760556(v=VS.85).aspx">TCITEMHEADER</a> structure followed by application-defined members. 

An application should only change the number of extra bytes when a tab control does not contain any tabs. 



