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

# ACMFILTERCHOOSEHOOKPROC callback function


## -description



The <b>acmFilterChooseHookProc</b> function specifies a user-defined function that hooks the <a href="https://msdn.microsoft.com/9d8f659f-46f7-4399-a538-24c887c0fbee">acmFilterChoose</a> dialog box.




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



To customize the dialog box selections, a hook function can optionally process the MM_ACM_FILTERCHOOSE message.

You should use this function the same way as you use the Common Dialog hook functions for customizing common dialog boxes.




## -see-also




<a href="https://msdn.microsoft.com/da207a50-9c67-4cf3-920b-5878637060db">Audio Compression Functions</a>



<a href="https://msdn.microsoft.com/2f9a4540-86c0-40e6-b4da-24a9d31b56bf">Audio Compression Manager</a>
 

 

