---
UID: NF:commctrl.ListView_SetItemPosition
title: ListView_SetItemPosition macro
author: windows-driver-content
description: Moves an item to a specified position in a list-view control (in icon or small icon view). You can use this macro or send the LVM_SETITEMPOSITION message explicitly.
old-location: controls\ListView_SetItemPosition.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setitemposition.htm
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: ListView_SetItemPosition, ListView_SetItemPosition macro [Windows Controls], _win32_ListView_SetItemPosition, _win32_ListView_SetItemPosition_cpp, commctrl/ListView_SetItemPosition, controls.ListView_SetItemPosition, controls._win32_ListView_SetItemPosition
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
-	ListView_SetItemPosition
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_SetItemPosition macro


## -description


Moves an item to a specified position in a list-view control (in icon or small icon view). You can use this macro or send the <a href="https://msdn.microsoft.com/dfb35af4-e6c3-40fc-9d7c-cf0d68a3ea01">LVM_SETITEMPOSITION</a> message explicitly. 


## -parameters




### -param hwndLV

TBD


### -param i

Type: <b>int</b>

The index of the list-view item. 


### -param x

Type: <b>int</b>

The new x-position of the item's upper-left corner, in view coordinates. 


### -param y

Type: <b>int</b>

The new y-position of the item's upper-left corner, in view coordinates. 


#### - hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


## -remarks



If the list-view control has the <a href="List_view_window_styles.htm">LVS_AUTOARRANGE</a> style, the list-view control is arranged after the position of the item is set. 

On Windows Vista, calling this macro on a list-view control with the <a href="List_view_window_styles.htm">LVS_AUTOARRANGE</a> style does nothing, and the return value is <b>FALSE</b>.



