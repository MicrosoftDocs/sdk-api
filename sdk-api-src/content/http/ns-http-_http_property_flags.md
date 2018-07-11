---
UID: NS:http._HTTP_PROPERTY_FLAGS
title: "_HTTP_PROPERTY_FLAGS"
author: windows-sdk-content
description: Used by the property configuration structures to enable or disable a property on a configuration object when setting property configurations.
old-location: http\http_property_flags.htm
old-project: http
ms.assetid: cafa3b04-ac8b-4269-bfa9-fe8e9ab65936
ms.author: windowssdkdev
ms.date: 04/13/2018
ms.keywords: "*PHTTP_PROPERTY_FLAGS, *PHTTP_PROPERTY_FLAGS structure [HTTP], HTTP_PROPERTY_FLAGS, HTTP_PROPERTY_FLAGS structure [HTTP], _HTTP_PROPERTY_FLAGS, http.http_property_flags, http/*PHTTP_PROPERTY_FLAGS, http/HTTP_PROPERTY_FLAGS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: http.h
req.include-header: 
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
req.typenames: HTTP_PROPERTY_FLAGS, *PHTTP_PROPERTY_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_PROPERTY_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _HTTP_PROPERTY_FLAGS structure


## -description


The <b>HTTP_PROPERTY_FLAGS</b> structure is used by the property configuration structures to enable or disable a property on a configuration object when setting property configurations.

When the configuration structure is used to query property configurations, this structure specifies whether the property is present on the configuration object.


## -struct-fields




### -field Present

 




#### - Present:1

The <b>Present</b> flag enables or disables a property, or determines whether the property is present on the configuration object.

A value of zero indicates the property is not present; a positive value indicates the property is present.


## -remarks



The property configuration structures are used in calls to <a href="https://msdn.microsoft.com/56111cc0-94c8-47dc-a3bb-ffc5dae772fe">HttpSetRequestQueueProperty</a>, <a href="https://msdn.microsoft.com/d655832c-68a1-42d1-ac91-964884bf2dac">HttpSetServerSessionProperty</a>, and <a href="https://msdn.microsoft.com/e0826a25-1c50-4757-9355-69eb4946e8dd">HttpSetUrlGroupProperty</a> to set properties on the corresponding configuration objects. The configuration structures are also used in calls to <a href="https://msdn.microsoft.com/a3b1e85e-f152-4038-a56a-3d5985757c45">HttpQueryRequestQueueProperty</a>, <a href="https://msdn.microsoft.com/653b286b-dc86-4896-8f03-1628b7178680">HttpQueryServerSessionProperty</a>, and <a href="https://msdn.microsoft.com/f3e8fde0-5a78-46aa-8c6c-cea957d12356">HttpQueryUrlGroupProperty</a>,  to query properties on the corresponding configuration object. When properties are set on the URL Group, server session, or request queue, this structure enables or disables the property. When properties are queried for the URL Group, server session, or request queue, this structure is used by the application to determine if the property is present. For more information, see the list of property configuration structures in the See Also section below.




## -see-also




<a href="https://msdn.microsoft.com/5a8e28e9-f85b-4550-929e-53f38eca6a8c">HTTP Server API Version 2.0 Structures</a>



<a href="https://msdn.microsoft.com/34c85ecf-1eb4-4f0d-a081-4b9feeb8dd15">HTTP_BANDWIDTH_LIMIT_INFO</a>



<a href="https://msdn.microsoft.com/551a928a-84c6-479b-a500-de69dc8857cd">HTTP_BINDING_INFO</a>



<a href="https://msdn.microsoft.com/6d2c1eeb-d248-4ca5-80b3-5c9f69ce8b9b">HTTP_CONNECTION_LIMIT_INFO</a>



<a href="https://msdn.microsoft.com/12e12f83-c36a-4b4e-8890-50566cf00c2b">HTTP_LOGGING_INFO</a>



<a href="https://msdn.microsoft.com/4f408115-c073-4e9f-b316-8ad3f03acf53">HTTP_SERVER_AUTHENTICATION_INFO</a>



<a href="https://msdn.microsoft.com/736ae89b-a4fb-4962-ae68-9aaccd869c88">HTTP_STATE_INFO</a>



<a href="https://msdn.microsoft.com/900f4b4d-c34d-4994-b8eb-b3f15e54f29a">HTTP_TIMEOUT_LIMIT_INFO</a>
 

 

