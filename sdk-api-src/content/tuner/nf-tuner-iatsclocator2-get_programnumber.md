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

# IATSCLocator2::get_ProgramNumber


## -description



The <b>get_ProgramNumber</b> method retrieves the program number.




## -parameters




### -param ProgramNumber [out]

Pointer to a variable that receives the program number.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/dbb830bf-db46-4981-8a96-ae33b1de3883">IATSCLocator2 Interface</a>



<a href="https://msdn.microsoft.com/af4eeac6-4eee-41d7-a35d-439e4143f046">put_ProgramNumber</a>
 

 

