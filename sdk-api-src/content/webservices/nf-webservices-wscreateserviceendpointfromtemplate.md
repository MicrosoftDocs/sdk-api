---
UID: NF:webservices.WsCreateServiceEndpointFromTemplate
title: WsCreateServiceEndpointFromTemplate function
author: windows-sdk-content
description: Helper routine for creating a service endpoint (WS_SERVICE_ENDPOINT) from policy templates.
old-location: wsw\wscreateserviceendpointfromtemplate.htm
tech.root: wsw
ms.assetid: 433194eb-ac42-4b6a-a1c0-7260a7aabeeb
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: WsCreateServiceEndpointFromTemplate, WsCreateServiceEndpointFromTemplate function [Web Services for Windows], webservices/WsCreateServiceEndpointFromTemplate, wsw.wscreateserviceendpointfromtemplate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsCreateServiceEndpointFromTemplate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsCreateServiceEndpointFromTemplate function


## -description



Helper routine for creating a service endpoint (<a href="https://msdn.microsoft.com/6b15fc3f-5e4b-4eb3-b337-0170b0ca746f">WS_SERVICE_ENDPOINT</a>) from policy templates.
      




## -parameters




### -param channelType [in]

A <a href="https://msdn.microsoft.com/7e1092f9-10e8-485c-a286-770e1c74d8ca">WS_CHANNEL_TYPE</a> enumeration value representing the type of channel hosted by the endpoint.
        


### -param properties [in]

An array of <a href="https://msdn.microsoft.com/4342d1d2-3126-401b-8019-c7dd243d4ac4">WS_SERVICE_ENDPOINT_PROPERTY</a>  structures containing  properties for the service endpoint. (Application should fill in channel properties in the template structure.)




### -param propertyCount [in]

The number of properties in the <i>properties</i> array.
                


### -param addressUrl [in, optional]

The URL address on which the endpoint is  to listen.
        


### -param contract [in]

A <a href="https://msdn.microsoft.com/77bd8c1e-0596-44d7-be99-356d052ee6c1">WS_SERVICE_CONTRACT</a> structure representing the contract of the endpoint.
        


### -param authorizationCallback [in]

A <a href="https://msdn.microsoft.com/0fa127ea-a715-4f21-8b49-3c2705c2bf5d">WS_SERVICE_SECURITY_CALLBACK</a> authorization callback for the service endpoint.
        


### -param heap [in]

The <a href="https://msdn.microsoft.com/3a25284a-8f15-42d4-a292-ece28a08fb69">heap</a> from which memory for the  service endpoint is allocated on successful return.
        


### -param templateType [in]

A <a href="https://msdn.microsoft.com/831001f4-619d-4128-a645-85077701c28c">WS_BINDING_TEMPLATE_TYPE</a> enumeration value representing the type of templates being used to create the service endpoint.
        


### -param templateValue [in]

Optional template structure to be created and filled in by application.
          The template must be consistent with the input template type (passed in the <i>templateType</i>  parameter). When the <i>templateValue</i> parameter is <b>NULL</b>,
          it is equivalent to the corresponding template structure initialized to zero.
        


### -param templateSize [in]

The size, in bytes, of the input templateValue structure.
        


### -param templateDescription [in]

The description of template structure (passed in the <i>templateValue</i> parameter). Needs to match templateType.
        


### -param templateDescriptionSize [in]

The size of the template description.
        


### -param serviceEndpoint [out]

On   success, a pointer that receives the address of the  <a href="https://msdn.microsoft.com/6b15fc3f-5e4b-4eb3-b337-0170b0ca746f">WS_SERVICE_ENDPOINT</a> structure representing the new service endpoint.
                
                


### -param error [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> structure  that receives additional error information if the function fails.
                
                


## -returns



If the function succeeds, it returns NO_ERROR; otherwise, it returns an HRESULT error code.




## -remarks



<b>WsCreateServiceEndpointFromTemplate</b> creates the <a href="https://msdn.microsoft.com/6b15fc3f-5e4b-4eb3-b337-0170b0ca746f">WS_SERVICE_ENDPOINT</a> structure from the specified input policy templates and additional user input.
      



