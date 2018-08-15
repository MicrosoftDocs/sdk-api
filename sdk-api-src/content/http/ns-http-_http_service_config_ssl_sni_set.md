---
UID: NS:http._HTTP_SERVICE_CONFIG_SSL_SNI_SET
title: "_HTTP_SERVICE_CONFIG_SSL_SNI_SET"
author: windows-sdk-content
description: Used to add a new Secure Sockets Layer (SSL) Server Name Indication (SNI) certificate record to the SSL SNI store or retrieve an existing record from it.
old-location: http\http_service_config_ssl_sni_set.htm
old-project: http
ms.assetid: 382838B9-C15E-459F-AC40-ECA15EFC18B8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PHTTP_SERVICE_CONFIG_SSL_SNI_SET, HTTP_SERVICE_CONFIG_SSL_SNI_SET, HTTP_SERVICE_CONFIG_SSL_SNI_SET structure [HTTP], PHTTP_SERVICE_CONFIG_SSL_SNI_SET, PHTTP_SERVICE_CONFIG_SSL_SNI_SET structure pointer [HTTP], _HTTP_SERVICE_CONFIG_SSL_SNI_SET, http.http_service_config_ssl_sni_set, http/HTTP_SERVICE_CONFIG_SSL_SNI_SET, http/PHTTP_SERVICE_CONFIG_SSL_SNI_SET"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: http.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: HTTP_SERVICE_CONFIG_SSL_SNI_SET, *PHTTP_SERVICE_CONFIG_SSL_SNI_SET
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_SERVICE_CONFIG_SSL_SNI_SET
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _HTTP_SERVICE_CONFIG_SSL_SNI_SET structure


## -description


The 
<b>HTTP_SERVICE_CONFIG_SSL_SNI_SET</b> structure is used to add a new Secure Sockets Layer (SSL) Server Name Indication (SNI) certificate record to the SSL SNI store or retrieve an existing record from it. It is passed to the 
<a href="https://msdn.microsoft.com/b0a6d442-2ff4-4e00-8301-696fb0864d8c">HttpSetServiceConfiguration</a> function through the <i>pConfigInformation</i> parameter or to retrieve data from the 
<a href="https://msdn.microsoft.com/bbd2c3c4-d2d0-4590-9b5c-6916b91600cd">HttpQueryServiceConfiguration</a> function through the <i>pOutputConfigInformation</i> parameter when the <i>ConfigId</i> parameter of either function is set to <b>HttpServiceConfigSslSniCertInfo</b>.


## -struct-fields




### -field KeyDesc

An <a href="https://msdn.microsoft.com/0EABB454-B4B9-4912-8E81-7930164B12F2">HTTP_SERVICE_CONFIG_SSL_SNI_KEY</a> structure that identifies the SSL SNI certificate record.


### -field ParamDesc

An <a href="https://msdn.microsoft.com/2bb3bfe0-9bac-4eb5-80b1-c883503a30b3">HTTP_SERVICE_CONFIG_SSL_PARAM</a> structure that holds the contents of the specified SSL SNI certificate record.


## -see-also




<a href="https://msdn.microsoft.com/0EABB454-B4B9-4912-8E81-7930164B12F2">HTTP_SERVICE_CONFIG_SSL_SNI_KEY</a>



<a href="https://msdn.microsoft.com/9C45B1B1-5572-4153-BBA4-0E8A52F650CA">HTTP_SERVICE_CONFIG_SSL_SNI_QUERY</a>



<a href="https://msdn.microsoft.com/0ae94936-4c6a-4c9f-adb8-5e3af75cf486">HttpDeleteServiceConfiguration</a>



<a href="https://msdn.microsoft.com/bbd2c3c4-d2d0-4590-9b5c-6916b91600cd">HttpQueryServiceConfiguration</a>



<a href="https://msdn.microsoft.com/b0a6d442-2ff4-4e00-8301-696fb0864d8c">HttpSetServiceConfiguration</a>
 

 

