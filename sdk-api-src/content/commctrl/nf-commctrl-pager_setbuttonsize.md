---
UID: NF:commctrl.Pager_SetButtonSize
title: Pager_SetButtonSize macro
author: windows-sdk-content
description: Sets the current button size for the pager control. You can use this macro or send the PGM_SETBUTTONSIZE message explicitly.
old-location: controls\Pager_SetButtonSize.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\pager\macros\pager_setbuttonsize.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Pager_SetButtonSize, Pager_SetButtonSize macro [Windows Controls], _win32_Pager_SetButtonSize, _win32_Pager_SetButtonSize_cpp, commctrl/Pager_SetButtonSize, controls.Pager_SetButtonSize, controls._win32_Pager_SetButtonSize
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
 - Pager_SetButtonSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Pager_SetButtonSize macro


## -description


Sets the current button size for the pager control. You can use this macro or send the <a href="https://msdn.microsoft.com/b31960f8-87c2-4209-8213-df75ac883e11">PGM_SETBUTTONSIZE</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the pager control. 


### -param iSize

Type: <b>int</b>

Value of type <b>int</b> that contains the new button size, in pixels. 


## -remarks



If the pager control has the <a href="Pager_Control_Styles.htm">PGS_HORZ</a> style, the button size determines the width of the pager buttons. If the pager control has the <a href="Pager_Control_Styles.htm">PGS_VERT</a> style, the button size determines the height of the pager buttons. By default, the pager control sets its button size to three-fourths of the width of the scroll bar. 




## -see-also




<a href="https://msdn.microsoft.com/836654ac-8bae-4f3d-967d-2ac10e97b86f">Pager_GetButtonSize</a>
 

 

