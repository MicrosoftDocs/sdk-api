---
UID: NF:commctrl.ListView_GetItemPosition
title: ListView_GetItemPosition macro
author: windows-sdk-content
description: Gets the position of a list-view item. You can use this macro or explicitly send the LVM_GETITEMPOSITION message.
old-location: controls\ListView_GetItemPosition.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getitemposition.htm
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: ListView_GetItemPosition, ListView_GetItemPosition macro [Windows Controls], _win32_ListView_GetItemPosition, _win32_ListView_GetItemPosition_cpp, commctrl/ListView_GetItemPosition, controls.ListView_GetItemPosition, controls._win32_ListView_GetItemPosition
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
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	ListView_GetItemPosition
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_GetItemPosition macro


## -description


Gets the position of a list-view item. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/e5841089-c34e-498e-b94c-45c845bfc747">LVM_GETITEMPOSITION</a> message. 


## -parameters




### -param hwndLV

TBD


### -param i

Type: <b>int</b>

The index of the list-view item. 


### -param ppt

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure that receives the position of the item's upper-left corner, in view coordinates. 


#### - hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 

