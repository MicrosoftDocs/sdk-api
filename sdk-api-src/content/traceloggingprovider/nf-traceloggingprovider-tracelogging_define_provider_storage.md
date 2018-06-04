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

# TRACELOGGING_DEFINE_PROVIDER_STORAGE macro


## -description


Allocates storage for a TraceLogging provider. This macro should only be used for advanced scenarios.


## -parameters




### -param storageVariable [in]

A handle to the data storage allocated for the TraceLogging provider.


### -param providerName [in]

The name of the TraceLogging provider. This must be a string literal and cannot be a variable.


### -param providerId [in]

The GUID for the provider.


#### - options [in, optional]

The GUID of the provider group that your provider is a member of.


## -remarks



Use this macro  to allocate storage but not define a handle for the TraceLogging provider. This is useful for scenarios where you need to have greater control over the way that your app manages registration for global handles.

Use the <a href="https://msdn.microsoft.com/5D794C46-95B2-4111-AFB8-CE488B4D1A42">TraceLoggingOptionGroup</a> macro to  specify the GUID of the provider group that the provider belongs to. A provider can be a member of no
more than one group. The semantics of group membership are determined by
the ETW controllers that subscribe a session to a group.

TRACELOGGING_DEFINE_PROVIDER_STORAGE will declare a static variable with the data needed for a provider. You can then create a handle by taking the address of this variable. Example usage:


<pre class="syntax">TRACELOGGING_DEFINE_PROVIDER_STORAGE(s_myProvider, "MyProvider", ( … GUID … );
const TraceLoggingHProvider g_hMyProvider = &amp;s_myProvider;</pre>




