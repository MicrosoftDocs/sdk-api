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

# IAMExtendedSeeking::GetMarkerTime


## -description



The <b>GetMarkerTime</b> method retrieves the presentation time associated with the specified marker.




## -parameters




### -param MarkerNum [in]

Specifies the marker number.


### -param pMarkerTime [out]

Pointer to a variable that receives the marker time.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9e0e49af-61ef-408c-8c26-bb29ab26a1f5">IAMExtendedSeeking Interface</a>



<a href="https://msdn.microsoft.com/899cc32e-3a9f-4be0-97a9-2ddd323bf9ce">IAMExtendedSeeking::GetMarkerName</a>
 

 

