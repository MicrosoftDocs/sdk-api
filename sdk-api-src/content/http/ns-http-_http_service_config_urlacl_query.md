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

# _HTTP_SERVICE_CONFIG_URLACL_QUERY structure


## -description


The 
<b>HTTP_SERVICE_CONFIG_URLACL_QUERY</b> structure is used to specify a particular reservation record to query in the URL namespace reservation store. It is passed to the 
<a href="https://msdn.microsoft.com/bbd2c3c4-d2d0-4590-9b5c-6916b91600cd">HttpQueryServiceConfiguration</a> function using the <i>pInputConfigInfo</i> parameter when the <i>ConfigId</i> parameter is equal to <b>HttpServiceConfigUrlAclInfo</b>.


## -struct-fields




### -field QueryDesc

One of the following values from the <a href="https://msdn.microsoft.com/63b2503f-7e71-4c62-8e9c-ad0f5103a9e8">HTTP_SERVICE_CONFIG_QUERY_TYPE</a> enumeration. 







#### HttpServiceConfigQueryExact

Returns a single record.



#### HttpServiceConfigQueryNext

Returns a sequence of records in a sequence of calls, controlled by the <i>dwToken</i> parameter.


### -field KeyDesc

If the <i>QueryDesc</i> parameter is equal to <b>HttpServiceConfigQueryExact</b>, then <i>KeyDesc</i> should contain an 
<a href="https://msdn.microsoft.com/ab739046-c25c-43bd-8c1f-da3aab374a05">HTTP_SERVICE_CONFIG_URLACL_KEY</a> structure that identifies the reservation record queried. 




If the <i>QueryDesc</i> parameter is equal to <b>HttpServiceConfigQueryNext</b>, <i>KeyDesc</i> is ignored.


### -field dwToken

If the <i>QueryDesc</i> parameter is equal to <b>HttpServiceConfigQueryNext</b>, then <i>dwToken</i> must be equal to zero on the first call to the 
<a href="https://msdn.microsoft.com/bbd2c3c4-d2d0-4590-9b5c-6916b91600cd">HttpQueryServiceConfiguration</a> function, one on the second call, two on the third call, and so forth until all reservation records are returned, at which point 
<b>HttpQueryServiceConfiguration</b> returns ERROR_NO_MORE_ITEMS. 




If the <i>QueryDesc</i> parameter is equal to <b>HttpServiceConfigQueryExact</b>, then <i>dwToken</i> is ignored.


## -see-also




<a href="https://msdn.microsoft.com/63b2503f-7e71-4c62-8e9c-ad0f5103a9e8">HTTP_SERVICE_CONFIG_QUERY_TYPE</a>



<a href="https://msdn.microsoft.com/ab739046-c25c-43bd-8c1f-da3aab374a05">HTTP_SERVICE_CONFIG_URLACL_KEY</a>



<a href="https://msdn.microsoft.com/92fc3f65-0153-4075-a61b-48a63c8e0ffe">HTTP_SERVICE_CONFIG_URLACL_SET</a>



<a href="https://msdn.microsoft.com/bbd2c3c4-d2d0-4590-9b5c-6916b91600cd">HttpQueryServiceConfiguration</a>
 

 

