---
UID: NF:traceloggingprovider.TRACELOGGING_DEFINE_PROVIDER
title: TRACELOGGING_DEFINE_PROVIDER macro (traceloggingprovider.h)
description: Allocates storage for a TraceLogging provider and creates a handle to the provider.
helpviewer_keywords: ["TRACELOGGING_DEFINE_PROVIDER","TRACELOGGING_DEFINE_PROVIDER macro","tracelogging.TRACELOGGING_DEFINE_PROVIDER","tracelogging.traceloggingprovider","traceloggingprovider/TRACELOGGING_DEFINE_PROVIDER"]
old-location: tracelogging\TRACELOGGING_DEFINE_PROVIDER.htm
tech.root: tracelogging
ms.assetid: 4515652D-86B0-4274-8523-27292F5F6815
ms.date: 03/21/2022
ms.keywords: TRACELOGGING_DEFINE_PROVIDER, TRACELOGGING_DEFINE_PROVIDER macro, tracelogging.TRACELOGGING_DEFINE_PROVIDER, tracelogging.traceloggingprovider, traceloggingprovider/TRACELOGGING_DEFINE_PROVIDER
req.header: traceloggingprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2012 R2
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TRACELOGGING_DEFINE_PROVIDER
 - traceloggingprovider/TRACELOGGING_DEFINE_PROVIDER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - traceloggingprovider.h
api_name:
 - TRACELOGGING_DEFINE_PROVIDER
---

# TRACELOGGING_DEFINE_PROVIDER macro


## -description

Allocates storage for a TraceLogging provider and creates a handle to the provider.

## -parameters

### -param handleVariable [in]

A handle to a TraceLogging provider (TraceLoggingHProvider) created using <a href="/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider">TRACELOGGING_DECLARE_PROVIDER</a>.

### -param providerName [in]

The name of the TraceLogging provider. This must be a string literal--do not use a variable.

### -param providerId [in]

The GUID for the provider.

This can be any GUID (for example, one generated using the `guidgen` SDK tool or https://uuidgen.org). However, Microsoft has established a convention for generating the GUID using a hash of the provider name. This provides several benefits: it's easier to remember just the name,  and it works with tools such as tracelog, traceview, EventSource, and WPR.

You can obtain the provider Id in PowerShell as follows:
```powershell
[System.Diagnostics.Tracing.EventSource]::new("MyProvider").Guid
```

Results in:
```

Guid
----
b3864c38-4273-58c5-545b-8b3608343471
```

#### - options [in, optional]

The GUID of the provider group that this provider is a member of.

## -remarks

Before using this macro, you need to declare your TraceLogging provider using <a href="/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregisterex">TRACELOGGING_DECLARE_PROVIDER</a>. Once the provider is created, it is in the unregistered state. Before it can respond to any write calls, you need to register the provider using  <a href="/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister">TraceLoggingRegister</a>.


Use the <a href="/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup">TraceLoggingOptionGroup</a> macro to  specify the GUID of the provider group that the provider belongs to. A provider can be a member of no
more than one group. The semantics of group membership are determined by
the ETW controllers that subscribe a session to a group.

If your provider is a part of a group, add the <i>options</i> parameter.


#### Examples


```cpp
TRACELOGGING_DEFINE_PROVIDER(
    g_hMyProvider,
    "MyProvider",
    (0xb3864c38, 0x4273, 0x58c5, 0x54, 0x5b, 0x8b, 0x36, 0x08, 0x34, 0x34, 0x71));
```

```cpp
TRACELOGGING_DEFINE_PROVIDER(
    g_hMyProvider,
    "MyProvider",
    (0xb3864c38, 0x4273, 0x58c5, 0x54, 0x5b, 0x8b, 0x36, 0x08, 0x34, 0x34, 0x71),
    TraceLoggingOptionGroup(0xfaaf2f61, 0x9b26, 0x4591, 0x9b, 0xb1, 0xb9, 0xb8, 0xba, 0xe2, 0xd3, 0x4c));
```
