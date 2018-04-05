---
UID: NF:commctrl.TabCtrl_DeleteItem
title: TabCtrl_DeleteItem macro
author: windows-driver-content
description: Removes an item from a tab control. You can use this macro or send the TCM_DELETEITEM message explicitly.
old-location: controls\TabCtrl_DeleteItem.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_deleteitem.htm
ms.author: windowsdriverdev
ms.date: 3/31/2018
ms.keywords: TabCtrl_DeleteItem, TabCtrl_DeleteItem macro [Windows Controls], _win32_TabCtrl_DeleteItem, _win32_TabCtrl_DeleteItem_cpp, commctrl/TabCtrl_DeleteItem, controls.TabCtrl_DeleteItem, controls._win32_TabCtrl_DeleteItem
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
req.typenames: CATEGORYINFO, *LPCATEGORYINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	TabCtrl_DeleteItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TabCtrl_DeleteItem macro


## -description


Removes an item from a tab control. You can use this macro or send the <a href="https://msdn.microsoft.com/54bfa446-580a-4ea7-b5e9-9429f4ee1c2b">TCM_DELETEITEM</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tab control. 


### -param i

TBD






#### - iItem

Type: <b>int</b>

Index of the item to delete. 

