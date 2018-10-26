---
UID: NF:commctrl.Pager_SetBkColor
title: Pager_SetBkColor macro
author: windows-sdk-content
description: Sets the current background color for the pager control. You can use this macro or send the PGM_SETBKCOLOR message explicitly.
old-location: controls\Pager_SetBkColor.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\pager\macros\pager_setbkcolor.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: Pager_SetBkColor, Pager_SetBkColor macro [Windows Controls], _win32_Pager_SetBkColor, _win32_Pager_SetBkColor_cpp, commctrl/Pager_SetBkColor, controls.Pager_SetBkColor, controls._win32_Pager_SetBkColor
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
 - Pager_SetBkColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Pager_SetBkColor macro


## -description


Sets the current background color for the pager control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb760878(v=VS.85).aspx">PGM_SETBKCOLOR</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

Handle to the pager control. 


### -param clr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">COLORREF</a></b>

<b>COLORREF</b> value that contains the new background color of the pager control. 


## -remarks



By default, the pager control will use the system button face color as the background color. This is the same color that can be retrieved by calling <a href="https://msdn.microsoft.com/en-us/library/Dd144927(v=VS.85).aspx">GetSysColorBrush</a> with COLOR_BTNFACE. 



