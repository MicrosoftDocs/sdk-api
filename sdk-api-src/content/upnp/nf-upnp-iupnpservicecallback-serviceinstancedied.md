---
UID: NF:upnp.IUPnPServiceCallback.ServiceInstanceDied
title: IUPnPServiceCallback::ServiceInstanceDied
author: windows-sdk-content
description: The ServiceInstanceDied method is invoked when a service is no longer sending events.
old-location: upnp\iupnpservicecallback_serviceinstancedied.htm
tech.root: upnp
ms.assetid: 13b6d2b1-f95d-4b07-bd69-2793158ee27b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUPnPServiceCallback interface [UPnP APIs],ServiceInstanceDied method, IUPnPServiceCallback.ServiceInstanceDied, IUPnPServiceCallback::ServiceInstanceDied, ServiceInstanceDied, ServiceInstanceDied method [UPnP APIs], ServiceInstanceDied method [UPnP APIs],IUPnPServiceCallback interface, _upnp_iupnpservicecallback_serviceinstancedied, upnp.iupnpservicecallback_serviceinstancedied, upnp/IUPnPServiceCallback::ServiceInstanceDied
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Upnp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPServiceCallback.ServiceInstanceDied
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUPnPServiceCallback::ServiceInstanceDied


## -description


The 
<b>ServiceInstanceDied</b> method is invoked when a service is no longer sending events.


## -parameters




### -param pus [in]

Reference to an 
<a href="https://msdn.microsoft.com/48b20b03-62a4-4dcd-8eda-f1bfef1eef38">IUPnPService</a> object that specifies the service about which the UPnP framework is sending the notification.


## -returns



The application should return S_OK.




## -remarks



The UPnP framework invokes this method either when a service has notified the UPnP framework that it is no longer sending events or when the UPnP framework has failed to maintain its connection to a service.




## -see-also




<a href="https://msdn.microsoft.com/48b20b03-62a4-4dcd-8eda-f1bfef1eef38">IUPnPService</a>



<a href="https://msdn.microsoft.com/f5797907-ae65-48e6-adf8-b717bfb5101f">IUPnPService::AddCallback</a>



<a href="https://msdn.microsoft.com/44515be4-891b-4f3d-a2c2-1699e468e708">IUPnPServiceCallback</a>
 

 

