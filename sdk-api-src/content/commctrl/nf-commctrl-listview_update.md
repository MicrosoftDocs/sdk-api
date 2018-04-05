---
UID: NF:commctrl.ListView_Update
title: ListView_Update macro
author: windows-driver-content
description: Updates a list-view item. If the list-view control has the LVS_AUTOARRANGE style, this macro causes the list-view control to be arranged. You can use this macro or send the LVM_UPDATE message explicitly.
old-location: controls\ListView_Update.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_update.htm
ms.author: windowsdriverdev
ms.date: 3/31/2018
ms.keywords: ListView_Update, ListView_Update macro [Windows Controls], _win32_ListView_Update, _win32_ListView_Update_cpp, commctrl/ListView_Update, controls.ListView_Update, controls._win32_ListView_Update
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
-	ListView_Update
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_Update macro


## -description


Updates a list-view item. If the list-view control has the <a href="List_view_window_styles.htm">LVS_AUTOARRANGE</a> style, this macro causes the list-view control to be arranged. You can use this macro or send the <a href="https://msdn.microsoft.com/81b332e9-4bea-481e-a7c5-613371103550">LVM_UPDATE</a> message explicitly. 


## -parameters




### -param hwndLV

TBD


### -param i

TBD






#### - hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


#### - iItem

Type: <b>int</b>

The index of the item to update. 

