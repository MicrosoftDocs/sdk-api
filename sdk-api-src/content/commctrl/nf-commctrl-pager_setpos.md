---
UID: NF:commctrl.Pager_SetPos
title: Pager_SetPos macro
author: windows-sdk-content
description: Sets the scroll position for the pager control. You can use this macro or send the PGM_SETPOS message explicitly.
old-location: controls\Pager_SetPos.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\pager\macros\pager_setpos.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: Pager_SetPos, Pager_SetPos macro [Windows Controls], _win32_Pager_SetPos, _win32_Pager_SetPos_cpp, commctrl/Pager_SetPos, controls.Pager_SetPos, controls._win32_Pager_SetPos
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
tech.root: 
req.typenames: STGOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - Pager_SetPos
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# Pager_SetPos macro


## -description


Sets the scroll position for the pager control. You can use this macro or send the <a href="https://msdn.microsoft.com/b882ea2d-9dab-4d36-9201-29522141f779">PGM_SETPOS</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param iPos

Type: <b>int</b>

Value of type <b>int</b> that contains the new scroll position, in pixels. 


#### - hwndPager

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the pager control. 

