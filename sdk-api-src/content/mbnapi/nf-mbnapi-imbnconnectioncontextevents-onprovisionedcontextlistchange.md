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

# IMbnConnectionContextEvents::OnProvisionedContextListChange


## -description


Notification method called by the Mobile Broadband service to indicate that a provisioned context stored in the device is available or updated.


## -parameters




### -param newInterface [in]

An <a href="https://msdn.microsoft.com/a9bc52dc-47f9-4b20-b98d-0287464a89e5">IMbnConnectionContext</a> interface that represents the device for which the context is available or updated.


## -returns



This method must return <b>S_OK</b>.




## -remarks



An application can use the passed <a href="https://msdn.microsoft.com/a9bc52dc-47f9-4b20-b98d-0287464a89e5">IMbnConnectionContext</a> interface to get the list of provisioned contexts for the device.  

<b>OnProvisionedContextListChange</b> is not called as the result of an update to an existing provisioned context from an application call of the <a href="https://msdn.microsoft.com/738a3037-01a9-465a-a67d-979a29968b68">SetProvisionedContext</a> method of <a href="https://msdn.microsoft.com/a9bc52dc-47f9-4b20-b98d-0287464a89e5">IMbnConnectionContext</a>.




## -see-also




<a href="https://msdn.microsoft.com/1f73260b-04db-410a-ade0-a835805b2b0a">IMbnConnectionContextEvents</a>
 

 

