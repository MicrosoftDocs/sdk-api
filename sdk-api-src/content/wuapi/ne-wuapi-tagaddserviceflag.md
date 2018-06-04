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

# tagAddServiceFlag enumeration


## -description


Defines the possible ways in which the <a href="https://msdn.microsoft.com/26b75edc-eb43-4ee0-8040-da8b3252cf21">IUpdateServiceManager2</a> interface can process service registration requests.


## -enum-fields




### -field asfAllowPendingRegistration

Allows the update agent to process the service registration at a later time, when it next performs an online scan for updates.


### -field asfAllowOnlineRegistration

Allows the update agent to process the service registration immediately if network connectivity is available.


### -field asfRegisterServiceWithAU

Registers the service with Automatic Updates when the service is added.


## -remarks



For info about how  <a href="https://msdn.microsoft.com/1584b92f-ba21-4b03-a1b4-540313eb7893">IUpdateServiceManager2::AddService2</a> behaves when you specify different combinations of <b>AddServiceFlag</b> values in the <i>flags</i> parameter, see the Remarks section of <b>IUpdateServiceManager2::AddService2</b>.




## -see-also




<a href="https://msdn.microsoft.com/1584b92f-ba21-4b03-a1b4-540313eb7893">IUpdateServiceManager2::AddService2</a>
 

 

