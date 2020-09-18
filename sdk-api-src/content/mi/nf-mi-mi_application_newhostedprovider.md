---
UID: NF:mi.MI_Application_NewHostedProvider
title: MI_Application_NewHostedProvider function (mi.h)
description: Registers a hosted provider with the WMI engine on the local machine.
helpviewer_keywords: ["MI_Application_NewHostedProvider","MI_Application_NewHostedProvider function [Windows Management Infrastructure (MI)]","mi/MI_Application_NewHostedProvider","wmi_v2.mi_application_newhostedprovider"]
old-location: wmi_v2\mi_application_newhostedprovider.htm
tech.root: wmi_v2
ms.assetid: 4f39ffca-4ae3-4ce5-9460-c7ac27c06a50
ms.date: 12/05/2018
ms.keywords: MI_Application_NewHostedProvider, MI_Application_NewHostedProvider function [Windows Management Infrastructure (MI)], mi/MI_Application_NewHostedProvider, wmi_v2.mi_application_newhostedprovider
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_Application_NewHostedProvider
 - mi/MI_Application_NewHostedProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_Application_NewHostedProvider
---

# MI_Application_NewHostedProvider function


## -description

Registers a hosted provider with the WMI engine on the local machine.

## -parameters

### -param application [in]

A pointer to the handle returned from the 
      <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_initializev1">MI_Application_Initialize</a> 
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
      <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_delete">MI_Instance_Delete</a> function.

### -param hostedProvider [out]

A pointer to a returned hosted provider handle. When you have finished using the handle, close it by 
      calling the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_hostedprovider_close">MI_HostedProvider_Close</a> 
      function during shutdown or when the provider no longer needs to receive operation requests.

## -returns

This function returns MI_INLINE MI_Result.

## -remarks

A hosted provider is one that resides in a client application rather than in the WMI service's host process. 
    The client controls the lifetime of these providers. Hosted providers are registered differently than regular 
    providers. This different registration indicates that the WMI service be hosted by the client. When you have 
    finished using the provider, the application should shut it down by calling the 
    <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_hostedprovider_close">MI_HostedProvider_Close</a> function.