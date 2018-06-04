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

# IBDA_SignalProperties::GetSignalSource


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetSignalSource</b> method retrieves the signal source for the current tuning request.


## -parameters




### -param pulSignalSource [in, out]

Receives a value identifying the signal source. The value is an arbitrary identifier set by the network provider. If two tuners share the same signal source, they should have the same identifier.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method returns whatever value was last set by calling <a href="https://msdn.microsoft.com/81cd43b1-97a7-4663-984e-2c20a8315c7e">IBDA_SignalProperties::PutSignalSource</a>.

<div class="alert"><b>Note</b>  The <i>pulSignalSource</i> parameter is marked in the IDL file as [in, out] but is used as an [out] parameter. To preserve binary compatibility with previous versions, it has not been changed.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/fe88b628-7959-4d2f-981f-7de9126146f6">IBDA_SignalProperties Interface</a>



<a href="https://msdn.microsoft.com/81cd43b1-97a7-4663-984e-2c20a8315c7e">PutSignalSource</a>
 

 

