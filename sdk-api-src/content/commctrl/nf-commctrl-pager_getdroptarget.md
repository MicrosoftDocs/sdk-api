---
UID: NF:commctrl.Pager_GetDropTarget
title: Pager_GetDropTarget macro
author: windows-driver-content
description: Retrieves a pager control's IDropTarget interface pointer. You can use this macro or send the PGM_GETDROPTARGET message explicitly.
old-location: controls\Pager_GetDropTarget.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\pager\macros\pager_getdroptarget.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: Pager_GetDropTarget, Pager_GetDropTarget macro [Windows Controls], _win32_Pager_GetDropTarget, _win32_Pager_GetDropTarget_cpp, commctrl/Pager_GetDropTarget, controls.Pager_GetDropTarget, controls._win32_Pager_GetDropTarget
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
-	Pager_GetDropTarget
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# Pager_GetDropTarget macro


## -description


Retrieves a pager control's <a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a> interface pointer. You can use this macro or send the <a href="https://msdn.microsoft.com/6b548c30-2d32-4372-90e4-346a27dda218">PGM_GETDROPTARGET</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param ppdt

TBD






#### - hwndPager

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the pager control. 


#### - ppDropTarget

Type: <b><a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a>**</b>

Pointer to an <a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a> pointer that receives the interface pointer. It is the caller's responsibility to call 
					<a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> on this pointer when it is no longer needed. 

