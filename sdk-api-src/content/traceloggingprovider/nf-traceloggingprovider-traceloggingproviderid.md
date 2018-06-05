---
UID: NF:traceloggingprovider.TraceLoggingProviderId
title: TraceLoggingProviderId function
author: windows-sdk-content
description: Returns the provider ID that was specified in TRACELOGGING_DEFINE_PROVIDER.
old-location: tracelogging\traceloggingproviderid.htm
old-project: tracelogging
ms.assetid: 16C79B3D-ACFF-40E3-B418-2DC44F010A74
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: TraceLoggingProviderId, TraceLoggingProviderId function, tracelogging.traceloggingproviderid, traceloggingprovider/TraceLoggingProviderId
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: TPMVSCMGR_ERROR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	N/A
api_name:
-	TraceLoggingProviderId
product: Windows
targetos: Windows
req.lib: Advap32.lib
req.dll: N/A
req.irql: 
req.product: Windows XP with SP1 and later
---

# TraceLoggingProviderId function


## -description


Returns the provider ID that was specified in <a href="https://msdn.microsoft.com/4515652D-86B0-4274-8523-27292F5F6815">TRACELOGGING_DEFINE_PROVIDER</a>.


## -parameters




### -param hProvider

TBD




#### - hProviderId [in]

The handle of the TraceLogging provider.


## -returns



The GUID of the provider ID specified in <a href="https://msdn.microsoft.com/4515652D-86B0-4274-8523-27292F5F6815">TRACELOGGING_DEFINE_PROVIDER</a>.



