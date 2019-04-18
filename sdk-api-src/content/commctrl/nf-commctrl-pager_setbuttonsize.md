---
UID: NF:commctrl.Pager_SetButtonSize
title: Pager_SetButtonSize macro (commctrl.h)
author: windows-sdk-content
description: Sets the current button size for the pager control. You can use this macro or send the PGM_SETBUTTONSIZE message explicitly.
old-location: controls\Pager_SetButtonSize.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\pager\macros\pager_setbuttonsize.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Pager_SetButtonSize, Pager_SetButtonSize macro [Windows Controls], _win32_Pager_SetButtonSize, _win32_Pager_SetButtonSize_cpp, commctrl/Pager_SetButtonSize, controls.Pager_SetButtonSize, controls._win32_Pager_SetButtonSize
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
 - Pager_SetButtonSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Pager_SetButtonSize macro


## -description


Sets the current button size for the pager control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb760882(v=VS.85).aspx">PGM_SETBUTTONSIZE</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the pager control. 


### -param iSize

Type: <b>int</b>

Value of type <b>int</b> that contains the new button size, in pixels. 


## -remarks



If the pager control has the <a href="https://msdn.microsoft.com/en-us/library/Bb760859(v=VS.85).aspx">PGS_HORZ</a> style, the button size determines the width of the pager buttons. If the pager control has the <a href="https://msdn.microsoft.com/en-us/library/Bb760859(v=VS.85).aspx">PGS_VERT</a> style, the button size determines the height of the pager buttons. By default, the pager control sets its button size to three-fourths of the width of the scroll bar. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb760894(v=VS.85).aspx">Pager_GetButtonSize</a>
 

 

