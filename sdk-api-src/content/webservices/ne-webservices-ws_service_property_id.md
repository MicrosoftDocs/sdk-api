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

# WS_SERVICE_PROPERTY_ID enumeration


## -description


The optional parameters for configuring the service host.
            This enumeration is used within the <a href="https://msdn.microsoft.com/d25cab25-2227-4afe-ae45-93a229d7f78b">WS_SERVICE_PROPERTY</a> structure when calling <a href="https://msdn.microsoft.com/412a262a-1706-4101-b154-1804408a5b9f">WsCreateServiceHost</a> or by itself when calling <a href="https://msdn.microsoft.com/3793cb79-37b9-4d94-9932-9eb3b259b60e">WsGetServiceHostProperty</a>.


## -enum-fields




### -field WS_SERVICE_PROPERTY_HOST_USER_STATE

A void pointer
                    used with <a href="https://msdn.microsoft.com/412a262a-1706-4101-b154-1804408a5b9f">WsCreateServiceHost</a>. This property 
                    is made available to different callbacks and service operations as part of the  <a href="https://msdn.microsoft.com/5c9b5906-15f0-4339-a4ad-39977d28ce5b">WS_OPERATION_CONTEXT</a> structure


### -field WS_SERVICE_PROPERTY_FAULT_DISCLOSURE

A <a href="https://msdn.microsoft.com/1dca9074-b329-4293-8a44-d0ced00ae59e">WS_FAULT_DISCLOSURE</a> value used with <a href="https://msdn.microsoft.com/412a262a-1706-4101-b154-1804408a5b9f">WsCreateServiceHost</a>.
                    This property is used to specify the disclosure level of the error object when its converted into a fault. The default is <b>WS_MINIMAL_FAULT_DISCLOSURE</b>.
                


### -field WS_SERVICE_PROPERTY_FAULT_LANGID


                                        A LANGID used with <a href="https://msdn.microsoft.com/3793cb79-37b9-4d94-9932-9eb3b259b60e">WsGetServiceHostProperty</a> to create a fault. If none is specified, the default user locale will be used.



### -field WS_SERVICE_PROPERTY_HOST_STATE


                    A <a href="https://msdn.microsoft.com/99745db7-6e9c-49fd-a97a-4430a80064bb">WS_SERVICE_HOST_STATE</a> value  used with <a href="https://msdn.microsoft.com/3793cb79-37b9-4d94-9932-9eb3b259b60e">WsGetServiceHostProperty</a> that specifies the current state of the service host.
                


                    The returned value is a snapshot of the current state, so it is
                    possible that the state may have changed before the caller has
                    had a chance to examine the value.
                


### -field WS_SERVICE_PROPERTY_METADATA

A <a href="https://msdn.microsoft.com/f695867d-989d-41a9-ab6e-612a6ef4fb14">WS_SERVICE_METADATA</a> structure used with <a href="https://msdn.microsoft.com/412a262a-1706-4101-b154-1804408a5b9f">WsCreateServiceHost</a> that contains the collection of metadata documents used for WS-MetadataExchange by the <a href="https://msdn.microsoft.com/1186e3ae-87d0-4d0b-a7cc-cce63dc091e2">WS_SERVICE_HOST</a>.


The service name and namespace are used to create a service element inside the WSDL document. The document is identified by means of the service namespace provided as part of <a href="https://msdn.microsoft.com/f695867d-989d-41a9-ab6e-612a6ef4fb14">WS_SERVICE_METADATA</a> structure.

 
Note that if a service section is already defined in any of the provided WSDL documents, a service element will not be added on behalf of the application by the runtime. 



### -field WS_SERVICE_PROPERTY_CLOSE_TIMEOUT

A <b>ULONG</b> used with <a href="https://msdn.microsoft.com/412a262a-1706-4101-b154-1804408a5b9f">WsCreateServiceHost</a> that specifies the maximum amount of time a service model will wait after <a href="https://msdn.microsoft.com/46abbcba-72ba-4328-858d-367218f45df3">WsCloseServiceHost</a> is called. Once the timeout expires service host will abort itself. 
The default is 5 seconds specified in milliseconds as 5000.


