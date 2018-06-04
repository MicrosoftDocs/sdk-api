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

# IRadialControllerConfigurationInterop::GetForWindow


## -description


Retrieves a <a href="https://msdn.microsoft.com/f988ea33-43bf-4b0e-86bc-8ee56f41ed90">RadialControllerConfiguration</a> object bound to the active application.


## -parameters




### -param hwnd [in]

Handle to the window of the active application.


### -param riid [in]

The GUID of the <a href="https://msdn.microsoft.com/f988ea33-43bf-4b0e-86bc-8ee56f41ed90">RadialControllerConfiguration</a> object.


### -param ppv [out]

Address of a pointer to a <a href="https://msdn.microsoft.com/f988ea33-43bf-4b0e-86bc-8ee56f41ed90">RadialControllerConfiguration</a> object.


## -returns



If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<b>Developer and UX guidance</b>



<a href="https://msdn.microsoft.com/eb8672c1-a7e6-45f5-a61f-3bee67f5ff5e">IRadialControllerConfigurationInterop</a>



<b>Samples</b>



<a href="https://go.microsoft.com/fwlink/?linkid=832322">Surface Dial interactions</a>



<a href="https://go.microsoft.com/fwlink/?linkid=832713">Universal Windows Platform samples (C# and C++)</a>



<a href="https://aka.ms/radialcontrollerclassicsample">Windows classic desktop sample</a>
 

 

