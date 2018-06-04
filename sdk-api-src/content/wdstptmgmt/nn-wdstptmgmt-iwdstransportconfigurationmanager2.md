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

# IWdsTransportConfigurationManager2 interface


## -description


This interface inherits from the <a href="https://msdn.microsoft.com/b86f9bc7-ddee-4d18-b5cb-28d28fa7ae7e">IWdsTransportConfigurationManager</a> interface and extends it with configuration settings, such as multicast session policy, that are available beginning with Windows Server 2008 R2. 

A client application can obtain an interface pointer to an instance of the <b>IWdsTransportConfigurationManager2</b> interface by first getting an interface pointer to the <a href="https://msdn.microsoft.com/b86f9bc7-ddee-4d18-b5cb-28d28fa7ae7e">IWdsTransportConfigurationManager</a> interface  and then using the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface Method</a>. 


## -see-also




<a href="https://msdn.microsoft.com/b86f9bc7-ddee-4d18-b5cb-28d28fa7ae7e">IWdsTransportConfigurationManager</a>
 

 

