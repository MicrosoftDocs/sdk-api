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
 

 

