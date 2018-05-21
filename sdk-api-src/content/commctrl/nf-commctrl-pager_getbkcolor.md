---
UID: NF:commctrl.Pager_GetBkColor
title: Pager_GetBkColor macro
author: windows-driver-content
description: Retrieves the current background color for the pager control. You can use this macro or send the PGM_GETBKCOLOR message explicitly.
old-location: controls\Pager_GetBkColor.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\pager\macros\pager_getbkcolor.htm
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: Pager_GetBkColor, Pager_GetBkColor macro [Windows Controls], _win32_Pager_GetBkColor, _win32_Pager_GetBkColor_cpp, commctrl/Pager_GetBkColor, controls.Pager_GetBkColor, controls._win32_Pager_GetBkColor
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
-	Pager_GetBkColor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# Pager_GetBkColor macro


## -description


Retrieves the current background color for the pager control. You can use this macro or send the <a href="https://msdn.microsoft.com/c39ad721-fe39-44e9-8305-67444acc5d65">PGM_GETBKCOLOR</a> message explicitly. 


## -parameters




### -param hwnd

TBD






#### - hwndPager

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the pager control. 


## -remarks



By default, the pager control will use the system button face color as the background color. This is the same color that can be retrieved by calling <a href="https://msdn.microsoft.com/07a1d8e3-eae8-40ab-9d0f-4efa9fac0117">GetSysColorBrush</a> with COLOR_BTNFACE. 



