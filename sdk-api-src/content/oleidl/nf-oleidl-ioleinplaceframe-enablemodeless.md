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

# IOleInPlaceFrame::EnableModeless


## -description


Enables or disables a frame's modeless dialog boxes.


## -parameters




### -param fEnable [in]

Specifies whether the modeless dialog box windows are to be enabled (<b>TRUE</b>) or disabled (<b>FALSE</b>).


## -returns



This method returns S_OK if the dialog box was either enabled or disabled successfully, depending on the value for <i>fEnable</i>.




## -see-also




<a href="https://msdn.microsoft.com/2fc45490-b3fe-48fd-a41c-2b7f35b09edc">IOleInPlaceActiveObject::EnableModeless</a>



<a href="https://msdn.microsoft.com/c530aff7-fd83-413d-8945-0c9d1bfb51ba">IOleInPlaceFrame</a>
 

 

