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

# capCreateCaptureWindowW function


## -description



The <b>capCreateCaptureWindow</b> function creates a capture window.




## -parameters




### -param lpszWindowName


            Null-terminated string containing the name used for the capture window.
          


### -param dwStyle


            Window styles used for the capture window. Window styles are described with the <a href="winui._win32_CreateWindowEx">CreateWindowEx</a> function.
          


### -param x


            The x-coordinate of the upper left corner of the capture window.
          


### -param y


            The y-coordinate of the upper left corner of the capture window.
          


### -param nWidth


            Width of the capture window.
          


### -param nHeight


            Height of the capture window.
          


### -param hwndParent

TBD


### -param nID


            Window identifier.
          


#### - hWnd


            Handle to the parent window.
          


## -returns




            Returns a handle of the capture window if successful or <b>NULL</b> otherwise.
          




## -see-also




<a href="https://msdn.microsoft.com/a727ce14-9b12-4f21-bab4-fa2eb245dce7">Creating a Capture Window</a>



<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/0fe87fa7-9f07-48f7-958b-da385d9ddaf0">Video Capture Functions</a>
 

 

