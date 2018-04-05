---
UID: NS:http._HTTP_SERVICE_CONFIG_SSL_SET
title: "_HTTP_SERVICE_CONFIG_SSL_SET"
author: windows-driver-content
description: Used to add a new record to the SSL store or retrieve an existing record from it.
old-location: http\http_service_config_ssl_set.htm
old-project: Http
ms.assetid: 23adda0b-907d-4804-9c12-e549af4f18c4
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: "*PHTTP_SERVICE_CONFIG_SSL_SET, HTTP_SERVICE_CONFIG_SSL_SET, HTTP_SERVICE_CONFIG_SSL_SET structure [HTTP], PHTTP_SERVICE_CONFIG_SSL_SET, PHTTP_SERVICE_CONFIG_SSL_SET structure pointer [HTTP], _HTTP_SERVICE_CONFIG_SSL_SET, _http_http_service_config_ssl_set, http.http_service_config_ssl_set, http/HTTP_SERVICE_CONFIG_SSL_SET, http/PHTTP_SERVICE_CONFIG_SSL_SET"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: HTTP_SERVICE_CONFIG_SSL_SET, *PHTTP_SERVICE_CONFIG_SSL_SET
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Http.h
api_name:
-	HTTP_SERVICE_CONFIG_SSL_SET
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _HTTP_SERVICE_CONFIG_SSL_SET structure


## -description


The 
<b>HTTP_SERVICE_CONFIG_SSL_SET</b> structure is used to add a new record to the SSL store or retrieve an existing record from it. An instance of the structure is used to pass data in to the 
<a href="https://msdn.microsoft.com/b0a6d442-2ff4-4e00-8301-696fb0864d8c">HTTPSetServiceConfiguration</a> function through the <i>pConfigInformation</i> parameter or to retrieve data from the 
<a href="https://msdn.microsoft.com/bbd2c3c4-d2d0-4590-9b5c-6916b91600cd">HTTPQueryServiceConfiguration</a> function through the <i>pOutputConfigInformation</i> parameter when the <i>ConfigId</i> parameter of either function is equal to <b>HTTPServiceConfigSSLCertInfo</b>.


## -struct-fields




### -field KeyDesc

An 
<a href="https://msdn.microsoft.com/67231fa5-69eb-4353-8c3c-326ec9095554">HTTP_SERVICE_CONFIG_SSL_KEY</a> structure that identifies the SSL certificate record.


### -field ParamDesc

An 
<a href="https://msdn.microsoft.com/2bb3bfe0-9bac-4eb5-80b1-c883503a30b3">HTTP_SERVICE_CONFIG_SSL_PARAM</a> structure that holds the contents of the specified SSL certificate record.


## -see-also




<a href="https://msdn.microsoft.com/bbd2c3c4-d2d0-4590-9b5c-6916b91600cd">HTTPQueryServiceConfiguration</a>



<a href="https://msdn.microsoft.com/b0a6d442-2ff4-4e00-8301-696fb0864d8c">HTTPSetServiceConfiguration</a>



<a href="https://msdn.microsoft.com/67231fa5-69eb-4353-8c3c-326ec9095554">HTTP_SERVICE_CONFIG_SSL_KEY</a>



<a href="https://msdn.microsoft.com/2bb3bfe0-9bac-4eb5-80b1-c883503a30b3">HTTP_SERVICE_CONFIG_SSL_PARAM</a>
 

 

