---
UID: NF:commctrl.ListView_GetNumberOfWorkAreas
title: ListView_GetNumberOfWorkAreas macro
author: windows-driver-content
description: Gets the number of working areas in a list-view control. You can use this macro or send the LVM_GETNUMBEROFWORKAREAS message explicitly.
old-location: controls\ListView_GetNumberOfWorkAreas.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getnumberofworkareas.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ListView_GetNumberOfWorkAreas, ListView_GetNumberOfWorkAreas macro [Windows Controls], _win32_ListView_GetNumberOfWorkAreas, _win32_ListView_GetNumberOfWorkAreas_cpp, commctrl/ListView_GetNumberOfWorkAreas, controls.ListView_GetNumberOfWorkAreas, controls._win32_ListView_GetNumberOfWorkAreas
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
-	ListView_GetNumberOfWorkAreas
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_GetNumberOfWorkAreas macro


## -description


Gets the number of working areas in a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/ce0bcccd-62a2-45a4-959e-9959c9ca0c46">LVM_GETNUMBEROFWORKAREAS</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param pnWorkAreas

TBD






#### - hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


#### - lpuWorkAreas

Type: <b>LPUINT</b>

A pointer to a UINT value that receives the number of working areas in the list-view control. If zero is placed in this variable, then no working areas are currently set. This value cannot be <b>NULL</b>. 


## -see-also




<a href="https://msdn.microsoft.com/6953cdfc-8c59-4c6d-8998-f828cea3a315">Using List-View Controls</a>
 

 

