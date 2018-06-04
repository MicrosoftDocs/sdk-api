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

# _HTTP_SERVICE_CONFIG_URLACL_SET structure


## -description


The 
<b>HTTP_SERVICE_CONFIG_URLACL_SET</b> structure is used to add a new record to the URL reservation store or retrieve an existing record from it. An instance of the structure is used to pass data in through the <i>pConfigInformation</i> parameter of the 
<a href="https://msdn.microsoft.com/b0a6d442-2ff4-4e00-8301-696fb0864d8c">HTTPSetServiceConfiguration</a> function, or to retrieve data through the <i>pOutputConfigInformation</i> parameter of the 
<a href="https://msdn.microsoft.com/bbd2c3c4-d2d0-4590-9b5c-6916b91600cd">HTTPQueryServiceConfiguration</a> function when the <i>ConfigId</i> parameter of either function is equal to <b>HTTPServiceConfigUrlAclInfo</b>.


## -struct-fields




### -field KeyDesc

An 
<a href="https://msdn.microsoft.com/ab739046-c25c-43bd-8c1f-da3aab374a05">HTTP_SERVICE_CONFIG_URLACL_KEY</a> structure that identifies the URL reservation record.


### -field ParamDesc

An 
<a href="https://msdn.microsoft.com/5fd50d77-cd2b-47d7-baa3-ed1d7fc934a7">HTTP_SERVICE_CONFIG_URLACL_PARAM</a> structure that holds the contents of the specified URL reservation record.


## -see-also




<a href="https://msdn.microsoft.com/bbd2c3c4-d2d0-4590-9b5c-6916b91600cd">HTTPQueryServiceConfiguration</a>



<a href="https://msdn.microsoft.com/b0a6d442-2ff4-4e00-8301-696fb0864d8c">HTTPSetServiceConfiguration</a>



<a href="https://msdn.microsoft.com/ab739046-c25c-43bd-8c1f-da3aab374a05">HTTP_SERVICE_CONFIG_URLACL_KEY</a>



<a href="https://msdn.microsoft.com/5fd50d77-cd2b-47d7-baa3-ed1d7fc934a7">HTTP_SERVICE_CONFIG_URLACL_PARAM</a>
 

 

