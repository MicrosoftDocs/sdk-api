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

# ISdoServiceControl::ResetService


## -description


The <b>ResetService</b> method resets the 
  service administered by the SDO API. Resetting the service causes the service to refresh its data.


## -parameters






## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -remarks



The data refresh begins 5 seconds after the last call to 
  <b>ISdoServiceControl::ResetService</b>. The 
  amount of time it takes for the refresh to complete depends on the number of objects in the SDO configuration 
  database.




## -see-also




<a href="https://msdn.microsoft.com/265f034a-78be-4792-958e-80ad7a71d1a7">ISdoMachineGetServiceSDO</a>



<a href="https://msdn.microsoft.com/c901ac9a-524a-498d-8b72-9afb26cf2c58">ISdoServiceControl</a>
 

 

