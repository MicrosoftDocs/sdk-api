---
UID: NF:commctrl.ListView_GetViewRect
title: ListView_GetViewRect macro
author: windows-driver-content
description: Gets the bounding rectangle of all items in the list-view control. The list view must be in icon or small icon view. You can use this macro or send the LVM_GETVIEWRECT message explicitly.
old-location: controls\ListView_GetViewRect.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getviewrect.htm
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: ListView_GetViewRect, ListView_GetViewRect macro [Windows Controls], _win32_ListView_GetViewRect, _win32_ListView_GetViewRect_cpp, commctrl/ListView_GetViewRect, controls.ListView_GetViewRect, controls._win32_ListView_GetViewRect
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
-	ListView_GetViewRect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_GetViewRect macro


## -description


Gets the bounding rectangle of all items in the list-view control. The list view must be in icon or small icon view. You can use this macro or send the <a href="https://msdn.microsoft.com/69b96f86-8b7e-42c1-ad73-f9b2732ab9f9">LVM_GETVIEWRECT</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param prc

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that receives the bounding rectangle. All coordinates are relative to the visible area of the list-view control. 

