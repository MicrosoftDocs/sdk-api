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

# IMSVidTuner::get_TuningSpace


## -description


The <b>get_TuningSpace</b> method retrieves the current tuning space.


## -parameters




### -param plTS






#### - pplTS [out]

Pointer to a variable that receives an <a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace</a> interface pointer.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The returned <a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace</a> interface has an outstanding reference count. The caller must release the interface.




## -see-also




<a href="https://msdn.microsoft.com/b11f3ac4-c351-4017-9801-98d8edec7449">IMSVidTuner Interface</a>



<a href="https://msdn.microsoft.com/b1da0078-0c5e-439e-9419-670e9e0f812c">IMSVidTuner::put_TuningSpace</a>



<a href="https://msdn.microsoft.com/a0f36580-522f-48d6-989d-11e8d175ffdb">The Microsoft Unified Tuning Model</a>
 

 

