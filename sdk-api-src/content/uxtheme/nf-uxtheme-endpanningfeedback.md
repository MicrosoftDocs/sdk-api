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

# EndPanningFeedback function


## -description


Terminates any existing animation that was in process or set up by <a href="https://msdn.microsoft.com/b1da3ed7-68bd-4bf7-a951-ee85368ea1d3">BeginPanningFeedback</a> and <a href="https://msdn.microsoft.com/227631b3-33e8-4ade-a7ff-51b70aed9ec6">UpdatePanningFeedback</a>. 


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The handle to the target window that will receive feedback.


### -param fAnimateBack [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Flag that indicates whether the displaced window should return to the original position using animation. If <b>FALSE</b>, the method restore the moved window using a direct jump.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> if successful.




## -remarks



This function can only be called after a <a href="https://msdn.microsoft.com/b1da3ed7-68bd-4bf7-a951-ee85368ea1d3">BeginPanningFeedback</a> call.



