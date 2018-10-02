---
UID: NS:http._HTTP_SERVICE_CONFIG_URLACL_QUERY
title: "_HTTP_SERVICE_CONFIG_URLACL_QUERY"
author: windows-sdk-content
description: Used to specify a particular reservation record to query in the URL namespace reservation store.
old-location: http\http_service_config_urlacl_query.htm
tech.root: Http
ms.assetid: 298edd6c-c036-4e45-88f3-84917c8a76ea
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PHTTP_SERVICE_CONFIG_URLACL_QUERY, HTTP_SERVICE_CONFIG_URLACL_QUERY, HTTP_SERVICE_CONFIG_URLACL_QUERY structure [HTTP], PHTTP_SERVICE_CONFIG_URLACL_QUERY, PHTTP_SERVICE_CONFIG_URLACL_QUERY structure pointer [HTTP], _HTTP_SERVICE_CONFIG_URLACL_QUERY, _http_http_service_config_urlacl_query, http.http_service_config_urlacl_query, http/HTTP_SERVICE_CONFIG_URLACL_QUERY, http/PHTTP_SERVICE_CONFIG_URLACL_QUERY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_SERVICE_CONFIG_URLACL_QUERY
product: Windows
targetos: Windows
req.typenames: HTTP_SERVICE_CONFIG_URLACL_QUERY, *PHTTP_SERVICE_CONFIG_URLACL_QUERY
req.redist: 
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
 

 

