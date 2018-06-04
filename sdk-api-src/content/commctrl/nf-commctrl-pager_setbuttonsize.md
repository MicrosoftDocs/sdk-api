---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# Pager_SetButtonSize macro


## -description


Sets the current button size for the pager control. You can use this macro or send the <a href="https://msdn.microsoft.com/b31960f8-87c2-4209-8213-df75ac883e11">PGM_SETBUTTONSIZE</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param iSize

TBD






#### - hwndPager

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the pager control. 


#### - iButtonSize

Type: <b>int</b>

Value of type <b>int</b> that contains the new button size, in pixels. 


## -remarks



If the pager control has the <a href="Pager_Control_Styles.htm">PGS_HORZ</a> style, the button size determines the width of the pager buttons. If the pager control has the <a href="Pager_Control_Styles.htm">PGS_VERT</a> style, the button size determines the height of the pager buttons. By default, the pager control sets its button size to three-fourths of the width of the scroll bar. 




## -see-also




<a href="https://msdn.microsoft.com/836654ac-8bae-4f3d-967d-2ac10e97b86f">Pager_GetButtonSize</a>
 

 

