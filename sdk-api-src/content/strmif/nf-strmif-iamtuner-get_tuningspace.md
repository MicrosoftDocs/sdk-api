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

# IAMTuner::get_TuningSpace


## -description



The <code>get_TuningSpace</code> method retrieves the tuning space.




## -parameters




### -param plTuningSpace [out]

Pointer to a variable that receives the current tuning space.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



The application defines the value retrieved by this method; it is set through a call to <a href="https://msdn.microsoft.com/fd0c0bc5-2c46-4c5a-8f93-9021f37a6e6a">IAMTuner::put_TuningSpace</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/997d39c5-a1a5-4d2d-8704-9846f149712c">IAMTuner Interface</a>
 

 

