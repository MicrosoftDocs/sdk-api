---
UID: NF:commctrl.TabCtrl_SetImageList
title: TabCtrl_SetImageList macro
author: windows-sdk-content
description: Assigns an image list to a tab control. You can use this macro or send the TCM_SETIMAGELIST message explicitly.
old-location: controls\TabCtrl_SetImageList.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_setimagelist.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: TabCtrl_SetImageList, TabCtrl_SetImageList macro [Windows Controls], _win32_TabCtrl_SetImageList, _win32_TabCtrl_SetImageList_cpp, commctrl/TabCtrl_SetImageList, controls.TabCtrl_SetImageList, controls._win32_TabCtrl_SetImageList
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
 - TabCtrl_SetImageList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TabCtrl_SetImageList macro


## -description


Assigns an image list to a tab control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb760629(v=VS.85).aspx">TCM_SETIMAGELIST</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

Handle to the tab control. 


### -param himl

Type: <b>HIMAGELIST</b>

Handle to the image list to assign to the tab control. 

