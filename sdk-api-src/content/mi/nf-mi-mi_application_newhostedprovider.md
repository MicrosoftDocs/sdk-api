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

# MI_Application_NewHostedProvider function


## -description


Registers a hosted provider with the WMI engine on the local machine.


## -parameters




### -param application [in]

A pointer to the handle returned from the 
      <a href="https://msdn.microsoft.com/32696A33-820D-4D01-AF71-DDA1F34EFBE0">MI_Application_Initialize</a> 
      function.


### -param namespaceName [in]

A pointer to the namespace where the provider is registered. For example, 
      L"root/cimv2".


### -param providerName [in]

A pointer to the provider name that is registered with the WMI engine for this hosted provider.


### -param mi_Main [in]

Main entry point to an MI provider.


### -param extendedError [out, optional]

A pointer to a pointer to an optional parameter to receive extended error information in the event the API 
      fails. If a pointer is passed in, then an error instance may be returned. If an error instance is returned, 
      then, when you have finished using it, delete it by using the 
      <a href="https://msdn.microsoft.com/6370e464-b262-4c91-a3c8-889911df7965">MI_Instance_Delete</a> function.


### -param hostedProvider [out]

A pointer to a returned hosted provider handle. When you have finished using the handle, close it by 
      calling the <a href="https://msdn.microsoft.com/b0cae173-a552-4c5a-8181-ba20143d846b">MI_HostedProvider_Close</a> 
      function during shutdown or when the provider no longer needs to receive operation requests.


## -returns



This function returns MI_INLINE MI_Result.




## -remarks



A hosted provider is one that resides in a client application rather than in the WMI service's host process. 
    The client controls the lifetime of these providers. Hosted providers are registered differently than regular 
    providers. This different registration indicates that the WMI service be hosted by the client. When you have 
    finished using the provider, the application should shut it down by calling the 
    <a href="https://msdn.microsoft.com/b0cae173-a552-4c5a-8181-ba20143d846b">MI_HostedProvider_Close</a> function.



