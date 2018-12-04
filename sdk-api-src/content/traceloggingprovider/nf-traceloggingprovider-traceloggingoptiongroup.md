---
UID: NF:traceloggingprovider.TraceLoggingOptionGroup
title: TraceLoggingOptionGroup macro
author: windows-sdk-content
description: Wrapper macro for use in TRACELOGGING_DEFINE_PROVIDER to declare the GUID of the provider group that the provider is a member of.
old-location: tracelogging\traceloggingoptiongroup.htm
tech.root: tracelogging
ms.assetid: 5D794C46-95B2-4111-AFB8-CE488B4D1A42
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: TraceLoggingOptionGroup, TraceLoggingOptionGroup macro, tracelogging.traceloggingoptiongroup, traceloggingprovider/TraceLoggingOptionGroup
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - traceloggingprovider.h
api_name:
 - TraceLoggingOptionGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TraceLoggingOptionGroup macro


## -description


Wrapper macro for use in <a href="https://msdn.microsoft.com/4515652D-86B0-4274-8523-27292F5F6815">TRACELOGGING_DEFINE_PROVIDER</a> to declare the
GUID of the provider group that the provider is a member of.


## -parameters




### -param g1 [in]

The first 4 bytes of the GUID.


### -param g2 [in]

The next 2 bytes of the GUID.


### -param g3 [in]

The next 2 bytes of the GUID.


### -param g4 [in]

The next byte of the GUID.


### -param g5 [in]

The next byte of the GUID.


### -param g6 [in]

The next byte of the GUID.


### -param g7 [in]

The next byte of the GUID.


### -param g8 [in]

The next byte of the GUID.


### -param g9 [in]

The next byte of the GUID.


### -param g10 [in]

The next byte of the GUID.


### -param g11 [in]

The next byte of the GUID.


## -remarks



A provider can be a member of no
more than one group. The semantics of group membership are determined by
ETW controllers that subscribe a session to a group.

The following code sample shows how to construct the  GUID:


<pre class="syntax">TraceLoggingOptionGroup(0x3970f9cf, 0x2c0c, 0x4f11, 0xb1, 0xcc, 0xe3, 0xa1, 0xe9, 0x95, 0x88, 0x33);</pre>




