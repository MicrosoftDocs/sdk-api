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

# ACMFORMATCHOOSEHOOKPROC callback function


## -description



The <b>acmFormatChooseHookProc</b> function specifies a user-defined function that hooks the <a href="https://msdn.microsoft.com/9be8311a-f6ad-4007-a254-841ee99ff3b6">acmFormatChoose</a> dialog box. The <b>acmFormatChooseHookProc</b> name is a placeholder for an application-defined name.




## -parameters




### -param hwnd

Window handle for the dialog box.


### -param uMsg

Window message.


### -param wParam

Message parameter.


### -param lParam

Message parameter.


## -remarks



If the hook function processes one of the WM_CTLCOLOR messages, this function must return a handle of the brush that should be used to paint the control background.

A hook function can optionally process the MM_ACM_FORMATCHOOSE message.

You should use this function the same way as you use the Common Dialog hook functions for customizing common dialog boxes.




## -see-also




<a href="https://msdn.microsoft.com/da207a50-9c67-4cf3-920b-5878637060db">Audio Compression Functions</a>



<a href="https://msdn.microsoft.com/2f9a4540-86c0-40e6-b4da-24a9d31b56bf">Audio Compression Manager</a>
 

 

