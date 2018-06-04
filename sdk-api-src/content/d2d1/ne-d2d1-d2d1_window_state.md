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

# D2D1_WINDOW_STATE enumeration


## -description


Describes whether a window is occluded.


## -enum-fields




### -field D2D1_WINDOW_STATE_NONE

The window is not occluded.


### -field D2D1_WINDOW_STATE_OCCLUDED

The window is occluded.


### -field D2D1_WINDOW_STATE_FORCE_DWORD




## -remarks



If the window was occluded the last time  <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">EndDraw</a> was called, the next time the render target calls <a href="https://msdn.microsoft.com/f40d46dc-04ec-4d11-bc3e-96043b16dcb3">CheckWindowState</a>, it  returns <b>D2D1_WINDOW_STATE_OCCLUDED</b> regardless of the current window state. If you want to use <b>CheckWindowState</b> to check the current window state, call <b>CheckWindowState</b> after every <b>EndDraw</b> call and ignore its return value. This will ensure that your next call to <b>CheckWindowState</b> state  returns the actual window state.




## -see-also




<a href="https://msdn.microsoft.com/f40d46dc-04ec-4d11-bc3e-96043b16dcb3">CheckWindowState</a>
 

 

