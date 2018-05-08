---
UID: NF:commctrl.ListView_FindItem
title: ListView_FindItem macro
author: windows-driver-content
description: Searches for a list-view item with the specified characteristics. You can use this macro or send the LVM_FINDITEM message explicitly.
old-location: controls\ListView_FindItem.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_finditem.htm
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: ListView_FindItem, ListView_FindItem macro [Windows Controls], _win32_ListView_FindItem, _win32_ListView_FindItem_cpp, commctrl/ListView_FindItem, controls.ListView_FindItem, controls._win32_ListView_FindItem
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
-	ListView_FindItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_FindItem macro


## -description


Searches for a list-view item with the specified characteristics. You can use this macro or send the <a href="https://msdn.microsoft.com/3b18c8ad-97e6-4f4d-bf89-afb95f925ed1">LVM_FINDITEM</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param iStart

Type: <b>int</b>

The index of the item after which to begin the search, or -1 to start from the beginning. 


### -param plvfi

Type: <b>const LPLVFINDINFO</b>

A pointer to an <a href="https://msdn.microsoft.com/6d78c0ec-9735-407d-a20b-efb7dc3b0fba">LVFINDINFO</a> structure that contains information about what to search for. 

