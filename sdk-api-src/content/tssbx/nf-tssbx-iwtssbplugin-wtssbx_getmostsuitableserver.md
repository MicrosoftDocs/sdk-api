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

# IWTSSBPlugin::WTSSBX_GetMostSuitableServer


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/f6959b8c-a8a8-438b-8b6d-31bf0e782bac">IWTSSBPlugin</a> interface is 
    not supported  after Windows Server 2008 R2. Starting with Windows Server 2012 please use the 
    <a href="https://msdn.microsoft.com/db3d3ee7-9e53-4bac-9711-4e85f1016db9">ITsSbPlugin</a> interface.]

Returns the ID of the server to which Terminal Services Session Broker (TS Session Broker) should direct the incoming connection. The  redirection logic of  the plug-in determines the preferred server.


## -parameters




### -param UserName [in]

A pointer to a Unicode string that contains the user name of the incoming connection.


### -param DomainName [in]

A pointer to a Unicode string that contains the domain name that is associated with the  incoming connection.


### -param ApplicationType [in]

A pointer to a Unicode string that contains the name of the program that Remote Desktop Services runs after it creates the session.


### -param FarmName [in]

A pointer to a Unicode string that contains the name of the farm in TS Session Broker that the user is connecting to.


### -param pMachineId [in, out]

A pointer to the ID of the server to which TS Session Broker will redirect the incoming connection.  This value is initially set to the  ID of the server provided by the load balancing logic of TS Session Broker.


## -returns



Returns <b>S_OK</b> if successful.




## -remarks



Use <b>WTSSBX_GetMostSuitableServer</b>  to override the default load balancing logic of TS Session Broker. TS Session Broker calls this method after it runs its own load balancing logic. The <i>pMachineId</i>  parameter is initially set to the ID of the server provided by the load balancing logic of TS Session Broker. When you implement this method, your redirection logic can return this <i>pMachineId</i> or another one as appropriate.

Whenever a server joins a farm in TS Session Broker, TS Session Broker calls the <a href="https://msdn.microsoft.com/226ca68e-6c3d-4160-a569-ca0b92cb9316">WTSSBX_MachineChangeNotification</a> method to notify the plug-in and provide a MachineId to identify the new server. When TS Session Broker calls <b>WTSSBX_GetMostSuitableServer</b>, the plug-in should return one of the IDs that TS Session Broker provided to the plug-in.  The plug-in should not return the ID of a server that is not in the farm.

Your implementation of <b>WTSSBX_GetMostSuitableServer</b> must return <b>S_OK</b> immediately if successful.




## -see-also




<a href="https://msdn.microsoft.com/db3d3ee7-9e53-4bac-9711-4e85f1016db9">ITsSbPlugin</a>



<a href="https://msdn.microsoft.com/f6959b8c-a8a8-438b-8b6d-31bf0e782bac">IWTSSBPlugin</a>
 

 

