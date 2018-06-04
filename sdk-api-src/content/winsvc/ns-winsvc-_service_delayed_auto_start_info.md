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

# _SERVICE_DELAYED_AUTO_START_INFO structure


## -description


Contains the delayed auto-start setting of an auto-start service.


## -struct-fields




### -field fDelayedAutostart

If this member is <b>TRUE</b>, the service is started after other auto-start services are started plus a short delay. Otherwise, the service is started during system boot.

This setting is ignored unless the service is an auto-start service.


## -remarks



Any service can be marked as a delayed auto-start service; however, this setting has no effect unless the service is an auto-start service. The change takes effect the next time the system is started.

The service control manager (SCM) supports delayed auto-start services to improve system performance at boot time without affecting the user experience. The SCM makes a list of delayed auto-start services during boot and starts them one at a time after the delay has passed, honoring dependencies. There is no specific time guarantee as to when the service will be started. To minimize the impact on the user, the <a href="https://msdn.microsoft.com/d7f3235e-91bd-4107-a30c-4a8f9a6c731e">ServiceMain</a> thread for the service is started with THREAD_PRIORITY_LOWEST. Threads that are started by the <i>ServiceMain</i> thread should also be run at a low priority. After the service has reported that it has entered the SERVICE_RUNNING state, the priority of the <i>ServiceMain</i> thread is raised to THREAD_PRIORITY_NORMAL.

A delayed auto-start service cannot be a member of a load ordering group. It can depend on another auto-start service. An auto-start service can depend on a delayed auto-start service, but this is not generally desirable as the SCM must start the dependent delayed auto-start service at boot.

If a delayed auto-start service is demand-started using the <a href="https://msdn.microsoft.com/f185a878-e1c3-4fe5-8ec9-c5296d27f985">StartService</a> function shortly after boot, the system starts the service on demand instead of delaying its start further. If this situation is likely to occur on a regular basis, the service should not be marked as a delayed auto-start service.

If a client calls a delayed auto-start service before it is loaded, the call fails. Therefore, clients should be prepared to either retry the call or demand start the service.




## -see-also




<a href="https://msdn.microsoft.com/6e5b79ed-52e1-460e-b076-01afbd08775c">ChangeServiceConfig2</a>



<a href="https://msdn.microsoft.com/cb090e59-aeff-4420-bb7c-912a4911006f">QueryServiceConfig2</a>
 

 

