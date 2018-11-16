---
UID: NF:commctrl.TabCtrl_SetItemExtra
title: TabCtrl_SetItemExtra macro
author: windows-sdk-content
description: Sets the number of bytes per tab reserved for application-defined data in a tab control. You can use this macro or send the TCM_SETITEMEXTRA message explicitly.
old-location: controls\TabCtrl_SetItemExtra.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_setitemextra.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: TabCtrl_SetItemExtra, TabCtrl_SetItemExtra macro [Windows Controls], _win32_TabCtrl_SetItemExtra, _win32_TabCtrl_SetItemExtra_cpp, commctrl/TabCtrl_SetItemExtra, controls.TabCtrl_SetItemExtra, controls._win32_TabCtrl_SetItemExtra
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
 - TabCtrl_SetItemExtra
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- commctrl.h
: 
- TabCtrl_SetItemExtra
: 
---

# TabCtrl_SetItemExtra macro


## -description


Sets the number of bytes per tab reserved for application-defined data in a tab control. You can use this macro or send the <a href="https://msdn.microsoft.com/8315f1fd-8eca-48bd-bb4a-71b09e8aa2c4">TCM_SETITEMEXTRA</a> message explicitly. 


## -parameters




### -param hwndTC

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tab control. 


### -param cb

Type: <b>int</b>

Number of extra bytes.


## -remarks



By default, the number of extra bytes is four. An application that changes the number of extra bytes cannot use the <a href="https://msdn.microsoft.com/e08c4528-5874-492c-97be-dfdf5f5636a9">TCITEM</a> structure to retrieve and set the application-defined data for a tab. Instead, you must define a new structure that consists of the <a href="https://msdn.microsoft.com/018a0de7-fc05-4b56-817b-1af36261fff2">TCITEMHEADER</a> structure followed by application-defined members. 

An application should only change the number of extra bytes when a tab control does not contain any tabs. 



