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

# IMbnPinManagerEvents::OnPinListAvailable


## -description


Notification method called by the Mobile Broadband service to indicate that the list of device PINs is available.


## -parameters




### -param pinManager [in]

Pointer to an <a href="https://msdn.microsoft.com/b5cfabc7-81f8-4ea0-b6f4-5de011320f0b">IMbnPinManager</a> interface that represents the Mobile Broadband device for which the PIN list is available.


## -returns



This method must return <b>S_OK</b>.




## -remarks



This method is called by the Mobile Broadband service to notify an application when the list of supported PIN types is available or if a PIN list retrieval operation resulted in an error. The calling application can issue the <a href="https://msdn.microsoft.com/732906dd-7d1e-49a1-a3cc-60075eed9c7c">GetPinList</a> method of the passed <a href="https://msdn.microsoft.com/b5cfabc7-81f8-4ea0-b6f4-5de011320f0b">IMbnPinManager</a> to get the available list of supported PINs or error code returned in the operation.




## -see-also




<a href="https://msdn.microsoft.com/2942bd4d-5bdb-45eb-a008-352bf44eec80">IMbnPinManagerEvents</a>
 

 

