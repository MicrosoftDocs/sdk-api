---
UID: NS:http._HTTP_SERVICE_CONFIG_URLACL_SET
title: "_HTTP_SERVICE_CONFIG_URLACL_SET"
author: windows-sdk-content
description: Used to add a new record to the URL reservation store or retrieve an existing record from it.
old-location: http\http_service_config_urlacl_set.htm
old-project: http
ms.assetid: 92fc3f65-0153-4075-a61b-48a63c8e0ffe
ms.author: windowssdkdev
ms.date: 04/13/2018
ms.keywords: "*PHTTP_SERVICE_CONFIG_URLACL_SET, HTTP_SERVICE_CONFIG_URLACL_SET, HTTP_SERVICE_CONFIG_URLACL_SET structure [HTTP], PHTTP_SERVICE_CONFIG_URLACL_SET, PHTTP_SERVICE_CONFIG_URLACL_SET structure pointer [HTTP], _HTTP_SERVICE_CONFIG_URLACL_SET, _http_http_service_config_urlacl_set, http.http_service_config_urlacl_set, http/HTTP_SERVICE_CONFIG_URLACL_SET, http/PHTTP_SERVICE_CONFIG_URLACL_SET"
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
tech.root: 
req.typenames: HTTP_SERVICE_CONFIG_URLACL_SET, *PHTTP_SERVICE_CONFIG_URLACL_SET
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_SERVICE_CONFIG_URLACL_SET
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

