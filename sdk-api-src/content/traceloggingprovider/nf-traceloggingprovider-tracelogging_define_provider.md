---
UID: NF:traceloggingprovider.TRACELOGGING_DEFINE_PROVIDER
title: TRACELOGGING_DEFINE_PROVIDER macro
author: windows-sdk-content
description: Allocates storage for a TraceLogging provider and creates a handle to the provider.
old-location: tracelogging\TRACELOGGING_DEFINE_PROVIDER.htm
tech.root: tracelogging
ms.assetid: 4515652D-86B0-4274-8523-27292F5F6815
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: TRACELOGGING_DEFINE_PROVIDER, TRACELOGGING_DEFINE_PROVIDER macro, tracelogging.TRACELOGGING_DEFINE_PROVIDER, tracelogging.traceloggingprovider, traceloggingprovider/TRACELOGGING_DEFINE_PROVIDER
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
 - TRACELOGGING_DEFINE_PROVIDER
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TRACELOGGING_DEFINE_PROVIDER macro


## -description


Allocates storage for a TraceLogging provider and creates a handle to the provider.


## -parameters




### -param handleVariable [in]

A handle to a TraceLogging provider (TraceLoggingHProvider) created using <a href="https://msdn.microsoft.com/E9C0B622-77A5-498F-BB28-C6C181271276">TRACELOGGING_DECLARE_PROVIDER</a>.


### -param providerName [in]

The name of the TraceLogging provider. This must be a string literal--do not use a variable.


### -param providerId [in]

The GUID for the provider.


#### - options [in, optional]

The GUID of the provider group that this provider is a member of.


## -remarks



Before using this macro, you need to declare your TraceLogging provider using <a href="https://msdn.microsoft.com/E9C0B622-77A5-498F-BB28-C6C181271276">TRACELOGGING_DECLARE_PROVIDER</a>. Once the provider is created, it is in the unregistered state. Before it can respond to any write calls, you need to register the provider using  <a href="https://msdn.microsoft.com/en-us/library/Dn904610(v=VS.85).aspx">TraceLoggingRegister</a>.

Use the <a href="https://msdn.microsoft.com/5D794C46-95B2-4111-AFB8-CE488B4D1A42">TraceLoggingOptionGroup</a> macro to  specify the GUID of the provider group that the provider belongs to. A provider can be a member of no
more than one group. The semantics of group membership are determined by
the ETW controllers that subscribe a session to a group.

If your provider is a part of a group, add the <i>options</i> parameter.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>TRACELOGGING_DEFINE_PROVIDER(
    g_hMyProvider,
    "MyProvider",
    (0xb3864c38, 0x4273, 0x58c5, 0x54, 0x5b, 0x8b, 0x36, 0x08, 0x34, 0x34, 0x71));</pre>
</td>
</tr>
</table></span><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>TRACELOGGING_DEFINE_PROVIDER(
    g_hMyProvider,
    "MyProvider",
    (0xb3864c38, 0x4273, 0x58c5, 0x54, 0x5b, 0x8b, 0x36, 0x08, 0x34, 0x34, 0x71),
    TraceLoggingOptionGroup(0xfaaf2f61, 0x9b26, 0x4591, 0x9b, 0xb1, 0xb9, 0xb8, 0xba, 0xe2, 0xd3, 0x4c));</pre>
</td>
</tr>
</table></span></div>


