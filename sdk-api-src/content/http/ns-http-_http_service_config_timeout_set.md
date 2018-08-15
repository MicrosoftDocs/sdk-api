---
UID: NS:http._HTTP_SERVICE_CONFIG_TIMEOUT_SET
title: "_HTTP_SERVICE_CONFIG_TIMEOUT_SET"
author: windows-sdk-content
description: Used to set the HTTP Server API wide timeout value.
old-location: http\http_service_config_timeout_set.htm
old-project: http
ms.assetid: 928cb09d-9f63-4334-b034-ee27e950ce0a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PHTTP_SERVICE_CONFIG_TIMEOUT_SET, *PHTTP_SERVICE_CONFIG_TIMEOUT_SET structure [HTTP], HTTP_SERVICE_CONFIG_TIMEOUT_SET, HTTP_SERVICE_CONFIG_TIMEOUT_SET structure [HTTP], _HTTP_SERVICE_CONFIG_TIMEOUT_SET, http.http_service_config_timeout_set, http/*PHTTP_SERVICE_CONFIG_TIMEOUT_SET, http/HTTP_SERVICE_CONFIG_TIMEOUT_SET"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: http.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: HTTP_SERVICE_CONFIG_TIMEOUT_SET, *PHTTP_SERVICE_CONFIG_TIMEOUT_SET
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_SERVICE_CONFIG_TIMEOUT_SET
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _HTTP_SERVICE_CONFIG_TIMEOUT_SET structure


## -description


The <b>HTTP_SERVICE_CONFIG_TIMEOUT_SET</b> structure is used to set the HTTP Server API wide timeout value.


## -struct-fields




### -field KeyDesc

A member of the <a href="https://msdn.microsoft.com/e591a6b8-e63f-40c3-bd48-e14cb9f89453">HTTP_SERVICE_CONFIG_TIMEOUT_KEY</a> enumeration identifying the timer that is set.


### -field ParamDesc

The value, in seconds, for the timer. The value must be greater than zero.


## -remarks



An instance of the <b>HTTP_SERVICE_CONFIG_TIMEOUT_SET</b> structure is used to pass data in to the 
<a href="https://msdn.microsoft.com/b0a6d442-2ff4-4e00-8301-696fb0864d8c">HTTPSetServiceConfiguration</a> function through the <i>pConfigInformation</i> parameter or to retrieve data from the 
<a href="https://msdn.microsoft.com/bbd2c3c4-d2d0-4590-9b5c-6916b91600cd">HTTPQueryServiceConfiguration</a> function through the <i>pOutputConfigInformation</i> parameter when the <i>ConfigId</i> parameter of either function is equal to <b>HttpServiceConfigTimeout</b>.

Querying the existing value of an HTTP Server API wide timeout does not require administrative privileges. Setting the value, however, does require administrative privileges.

When the HTTP Server API wide timeout value is set with <a href="https://msdn.microsoft.com/b0a6d442-2ff4-4e00-8301-696fb0864d8c">HTTPSetServiceConfiguration</a>, the setting persists when the HTTP service is stopped and restarted.  The timeout value is applied to all the HTTP Server API applications on the machine.

The HTTP Server API timeout value is deleted by calling <a href="https://msdn.microsoft.com/0ae94936-4c6a-4c9f-adb8-5e3af75cf486">HTTPDeleteServiceConfiguration</a> with the <i>ConfigId</i> parameter set to <b>HttpServiceConfigTimeout</b> and the <i>pConfigInformation</i>  parameter pointing to the <b>HTTP_SERVICE_CONFIG_TIMEOUT_SET</b> structure. When a timer value is deleted, the persistent setting goes away, and HTTP Server API uses its hardcoded defaults. 




## -see-also




<a href="https://msdn.microsoft.com/5a8e28e9-f85b-4550-929e-53f38eca6a8c">HTTP Server API Version 2.0 Structures</a>



<a href="https://msdn.microsoft.com/0ae94936-4c6a-4c9f-adb8-5e3af75cf486">HTTPDeleteServiceConfiguration</a>



<a href="https://msdn.microsoft.com/bbd2c3c4-d2d0-4590-9b5c-6916b91600cd">HTTPQueryServiceConfiguration</a>



<a href="https://msdn.microsoft.com/b0a6d442-2ff4-4e00-8301-696fb0864d8c">HTTPSetServiceConfiguration</a>
 

 

