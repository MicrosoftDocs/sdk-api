---
UID: NF:commctrl.Pager_SetChild
title: Pager_SetChild macro
author: windows-sdk-content
description: Sets the contained window for the pager control.
old-location: controls\Pager_SetChild.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\pager\macros\pager_setchild.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: Pager_SetChild, Pager_SetChild macro [Windows Controls], _win32_Pager_SetChild, _win32_Pager_SetChild_cpp, commctrl/Pager_SetChild, controls.Pager_SetChild, controls._win32_Pager_SetChild
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
 - Pager_SetChild
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Pager_SetChild macro


## -description


Sets the contained window for the pager control. This macro will not change the parent of the contained window; it only assigns a window handle to the pager control for scrolling. In most cases, the contained window will be a child window. If this is the case, the contained window should be a child of the pager control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb760884(v=VS.85).aspx">PGM_SETCHILD</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

Handle to the pager control. 


### -param hwndChild

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

Handle to the window to be contained. 

