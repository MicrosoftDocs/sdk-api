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

# IWdsTransportConfigurationManager::NotifyWdsTransportServices


## -description


Sends a notification to WDS transport services. The notification value is translated to the appropriate WDS transport service controls, and then these controls are sent to the appropriate services.




## -parameters




### -param ServiceNotification [in]

A value of the <a href="https://msdn.microsoft.com/d239241d-efe9-409b-8425-c71382b27c05">WDSTRANSPORT_SERVICE_NOTIFICATION</a> enumeration that specifies the type of service notification to be sent.


## -returns



Standard HRESULT error values are used: S_OK for success; others for failure.




## -see-also




<a href="https://msdn.microsoft.com/b86f9bc7-ddee-4d18-b5cb-28d28fa7ae7e">IWdsTransportConfigurationManager</a>



<a href="https://msdn.microsoft.com/d239241d-efe9-409b-8425-c71382b27c05">WDSTRANSPORT_SERVICE_NOTIFICATION</a>
 

 

