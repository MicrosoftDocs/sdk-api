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
 

 

