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

# IDDrawExclModeVideoCallback::OnUpdateSize


## -description



The <code>OnUpdateSize</code> method informs the application that the size of the video rectangle is about to change.




## -parameters




### -param dwWidth [in]

The new width, in pixels, of the video stream.


### -param dwHeight [in]

The new height, in pixels, of the video stream.


### -param dwARWidth [in]

The new horizontal value of the aspect ratio.


### -param dwARHeight [in]

The new vertical value of the aspect ratio.


## -returns



Returns an HRESULT value.




## -remarks



This method is called when the size of the rectangle in the video stream changes, for example from 704x480 to 640x480.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7f22d4cd-93e0-4d7d-b8f3-932488d2c672">IDDrawExclModeVideoCallback Interface</a>
 

 

