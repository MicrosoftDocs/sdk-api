---
UID: NF:commctrl.Pager_RecalcSize
title: Pager_RecalcSize macro
author: windows-sdk-content
description: Forces the pager control to recalculate the size of the contained window. Using this macro will result in a PGN_CALCSIZE notification being sent. You can use this macro or send the PGM_RECALCSIZE message explicitly.
old-location: controls\Pager_RecalcSize.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\pager\macros\pager_recalcsize.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: Pager_RecalcSize, Pager_RecalcSize macro [Windows Controls], _win32_Pager_RecalcSize, _win32_Pager_RecalcSize_cpp, commctrl/Pager_RecalcSize, controls.Pager_RecalcSize, controls._win32_Pager_RecalcSize
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
 - Pager_RecalcSize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# Pager_RecalcSize macro


## -description


Forces the pager control to recalculate the size of the contained window. Using this macro will result in a <a href="https://msdn.microsoft.com/a15f4191-2f26-4139-bdaf-bab219449b78">PGN_CALCSIZE</a> notification being sent. You can use this macro or send the <a href="https://msdn.microsoft.com/51b75ce8-2b41-4f1a-830e-b25e7d77dccb">PGM_RECALCSIZE</a> message explicitly. 


## -parameters




### -param hwnd

TBD






#### - hwndPager

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the pager control. 

