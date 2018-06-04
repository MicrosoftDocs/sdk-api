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

# IWTSSBPlugin::Initialize


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/f6959b8c-a8a8-438b-8b6d-31bf0e782bac">IWTSSBPlugin</a> interface is 
    not supported  after Windows Server 2008 R2. Starting with Windows Server 2012 please use the 
    <a href="https://msdn.microsoft.com/db3d3ee7-9e53-4bac-9711-4e85f1016db9">ITsSbPlugin</a> interface.]

Initializes the plug-in and returns a value that indicates the redirection capabilities of the 
    plug-in. Terminal Services Session Broker (TS Session Broker) calls this method 
    immediately after it instantiates the plug-in class.


## -parameters




### -param PluginCapabilities [out]

A pointer to a value that indicates the redirection capabilities of the plug-in.



#### 0

The plug-in redirects only within a farm in TS Session Broker. If this value is returned, TS Session Broker does not call the <a href="https://msdn.microsoft.com/989cd7bc-932f-4a33-91c8-e66fac7195ad">WTSSBX_GetUserExternalSession</a> method on the plug-in.



#### 1

The plug-in redirects within a farm in TS Session Broker, and the plug-in implements <a href="https://msdn.microsoft.com/989cd7bc-932f-4a33-91c8-e66fac7195ad">WTSSBX_GetUserExternalSession</a> to redirect outside the farm.


## -returns



Returns <b>S_OK</b> if successful.




## -remarks



TS Session Broker calls <b>Initialize</b> immediately after it instantiates the COM class. The plug-in should return information about its redirection capabilities  by using the <b>Initialize</b> method.

Your implementation of <b>Initialize</b> must return <b>S_OK</b> immediately if successful.




## -see-also




<a href="https://msdn.microsoft.com/db3d3ee7-9e53-4bac-9711-4e85f1016db9">ITsSbPlugin</a>



<a href="https://msdn.microsoft.com/f6959b8c-a8a8-438b-8b6d-31bf0e782bac">IWTSSBPlugin</a>
 

 

