---
UID: NF:commctrl.Pager_SetBorder
title: Pager_SetBorder macro
author: windows-sdk-content
description: Sets the current border size for the pager control. You can use this macro or send the PGM_SETBORDER message explicitly.
old-location: controls\Pager_SetBorder.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\pager\macros\pager_setborder.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: Pager_SetBorder, Pager_SetBorder macro [Windows Controls], _win32_Pager_SetBorder, _win32_Pager_SetBorder_cpp, commctrl/Pager_SetBorder, controls.Pager_SetBorder, controls._win32_Pager_SetBorder
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
 - Pager_SetBorder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Pager_SetBorder macro


## -description


Sets the current border size for the pager control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb760880(v=VS.85).aspx">PGM_SETBORDER</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

Handle to the pager control. 


### -param iBorder

Type: <b>int</b>

New size of the border, in pixels. This value should not be larger than the pager button or less than zero. If <i>iBorder</i> is too large, the border will be drawn the same size as the button. If 
<i>iBorder</i> is negative, the border size will be set to zero. 

