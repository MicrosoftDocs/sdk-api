---
UID: NF:commctrl.Pager_GetDropTarget
title: Pager_GetDropTarget macro
author: windows-sdk-content
description: Retrieves a pager control's IDropTarget interface pointer. You can use this macro or send the PGM_GETDROPTARGET message explicitly.
old-location: controls\Pager_GetDropTarget.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\pager\macros\pager_getdroptarget.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
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
 - Pager_GetDropTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Pager_GetDropTarget macro


## -description


Retrieves a pager control's <a href="https://msdn.microsoft.com/en-us/library/ms679679(v=VS.85).aspx">IDropTarget</a> interface pointer. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb760872(v=VS.85).aspx">PGM_GETDROPTARGET</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

Handle to the pager control. 


### -param ppdt

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms679679(v=VS.85).aspx">IDropTarget</a>**</b>

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms679679(v=VS.85).aspx">IDropTarget</a> pointer that receives the interface pointer. It is the caller's responsibility to call 
					<a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">Release</a> on this pointer when it is no longer needed. 

