---
UID: NF:commctrl.ListView_SetHotItem
title: ListView_SetHotItem macro
author: windows-driver-content
description: Sets the hot item in a list-view control. You can use this macro or send the LVM_SETHOTITEM message explicitly.
old-location: controls\ListView_SetHotItem.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_sethotitem.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ListView_SetHotItem, ListView_SetHotItem macro [Windows Controls], _win32_ListView_SetHotItem, _win32_ListView_SetHotItem_cpp, commctrl/ListView_SetHotItem, controls.ListView_SetHotItem, controls._win32_ListView_SetHotItem
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
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	ListView_SetHotItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_SetHotItem macro


## -description


Sets the hot item in a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/0aa2b15d-4983-4234-9863-f1fdee09f913">LVM_SETHOTITEM</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param i

TBD






#### - hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a list-view control. 


#### - iIndex

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

The zero-based index of the item to be set as the hot item. 

