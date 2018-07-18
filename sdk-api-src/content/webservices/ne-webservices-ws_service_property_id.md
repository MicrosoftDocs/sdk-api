---
UID: NE:webservices.WS_SERVICE_PROPERTY_ID
title: WS_SERVICE_PROPERTY_ID
author: windows-sdk-content
description: The optional parameters for configuring the service host. This enumeration is used within the WS_SERVICE_PROPERTY structure when calling WsCreateServiceHost or by itself when calling WsGetServiceHostProperty.
old-location: wsw\ws_service_property_id.htm
old-project: wsw
ms.assetid: 305fe7ad-e4a2-499a-b34b-e5b7cde53e22
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: WS_SERVICE_PROPERTY_CLOSE_TIMEOUT, WS_SERVICE_PROPERTY_FAULT_DISCLOSURE, WS_SERVICE_PROPERTY_FAULT_LANGID, WS_SERVICE_PROPERTY_HOST_STATE, WS_SERVICE_PROPERTY_HOST_USER_STATE, WS_SERVICE_PROPERTY_ID, WS_SERVICE_PROPERTY_ID enumeration [Web Services for Windows], WS_SERVICE_PROPERTY_METADATA, webservices/WS_SERVICE_PROPERTY_CLOSE_TIMEOUT, webservices/WS_SERVICE_PROPERTY_FAULT_DISCLOSURE, webservices/WS_SERVICE_PROPERTY_FAULT_LANGID, webservices/WS_SERVICE_PROPERTY_HOST_STATE, webservices/WS_SERVICE_PROPERTY_HOST_USER_STATE, webservices/WS_SERVICE_PROPERTY_ID, webservices/WS_SERVICE_PROPERTY_METADATA, wsw.ws_service_property_id
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: WS_SERVICE_PROPERTY_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_SERVICE_PROPERTY_ID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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


