---
UID: NE:http._HTTP_SERVICE_CONFIG_QUERY_TYPE
title: "_HTTP_SERVICE_CONFIG_QUERY_TYPE"
author: windows-sdk-content
description: The HTTP_SERVICE_CONFIG_QUERY_TYPE enumeration type defines various types of queries to make. It is used in the HTTP_SERVICE_CONFIG_SSL_QUERY, HTTP_SERVICE_CONFIG_SSL_CCS_QUERY, and HTTP_SERVICE_CONFIG_URLACL_QUERY structures.
old-location: http\http_service_config_query_type.htm
tech.root: http
ms.assetid: 63b2503f-7e71-4c62-8e9c-ad0f5103a9e8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PHTTP_SERVICE_CONFIG_QUERY_TYPE, HTTP_SERVICE_CONFIG_QUERY_TYPE, HTTP_SERVICE_CONFIG_QUERY_TYPE enumeration [HTTP], HttpServiceConfigQueryExact, HttpServiceConfigQueryMax, HttpServiceConfigQueryNext, PHTTP_SERVICE_CONFIG_QUERY_TYPE, PHTTP_SERVICE_CONFIG_QUERY_TYPE enumeration pointer [HTTP], _HTTP_SERVICE_CONFIG_QUERY_TYPE, _http_http_service_config_query_type, http.http_service_config_query_type, http/HTTP_SERVICE_CONFIG_QUERY_TYPE, http/HttpServiceConfigQueryExact, http/HttpServiceConfigQueryMax, http/HttpServiceConfigQueryNext, http/PHTTP_SERVICE_CONFIG_QUERY_TYPE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
 - HTTP_SERVICE_CONFIG_QUERY_TYPE
product: Windows
targetos: Windows
req.typenames: HTTP_SERVICE_CONFIG_QUERY_TYPE, *PHTTP_SERVICE_CONFIG_QUERY_TYPE
req.redist: 
---

# _HTTP_SERVICE_CONFIG_QUERY_TYPE enumeration


## -description


The 
<b>HTTP_SERVICE_CONFIG_QUERY_TYPE</b> enumeration type defines various types of queries to make. It is used in the 
<a href="https://msdn.microsoft.com/733b451a-d35b-4b83-ba49-0529309cd99b">HTTP_SERVICE_CONFIG_SSL_QUERY</a>, <a href="https://msdn.microsoft.com/E7578D74-E8BE-472D-A01B-51BBA511F561">HTTP_SERVICE_CONFIG_SSL_CCS_QUERY</a>, and 
<a href="https://msdn.microsoft.com/298edd6c-c036-4e45-88f3-84917c8a76ea">HTTP_SERVICE_CONFIG_URLACL_QUERY</a> structures.


## -enum-fields




### -field HttpServiceConfigQueryExact

The query returns a single record that matches the specified key value.


### -field HttpServiceConfigQueryNext

The query iterates through the store and returns all records in sequence, using an index value that the calling process increments between query calls.


### -field HttpServiceConfigQueryMax

Terminates the enumeration; is not used to define a query type.


## -see-also




<a href="https://msdn.microsoft.com/E7578D74-E8BE-472D-A01B-51BBA511F561">HTTP_SERVICE_CONFIG_SSL_CCS_QUERY</a>



<a href="https://msdn.microsoft.com/733b451a-d35b-4b83-ba49-0529309cd99b">HTTP_SERVICE_CONFIG_SSL_QUERY</a>



<a href="https://msdn.microsoft.com/298edd6c-c036-4e45-88f3-84917c8a76ea">HTTP_SERVICE_CONFIG_URLACL_QUERY</a>
 

 

