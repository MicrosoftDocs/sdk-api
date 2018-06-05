---
UID: NF:traceloggingprovider.TraceLoggingProviderEnabled
title: TraceLoggingProviderEnabled function
author: windows-sdk-content
description: Indicates whether any sessions have subscribed to the provider.
old-location: tracelogging\traceloggingproviderenabled.htm
old-project: tracelogging
ms.assetid: 3ECA1A19-CFDD-4B14-AF88-0180C9B65F00
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: TraceLoggingProviderEnabled, TraceLoggingProviderEnabled function, tracelogging.traceloggingproviderenabled, traceloggingprovider/TraceLoggingProviderEnabled
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
-	TraceLoggingProviderEnabled
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: N/A
req.irql: 
req.product: Windows XP with SP1 and later
---

# TraceLoggingProviderEnabled function


## -description


Indicates whether any sessions have subscribed to the provider.


## -parameters




### -param hProvider [in]

The handle to the provider to check.


### -param eventLevel [in]

The event level that you want to check. An event level of 0 indicates any events.


### -param eventKeyword [in]

The keyword that you want to check. A keyword of 0 indicates no specific keywords.


## -returns



Returns <b>TRUE</b> if any session has subscribed to the handler matching the event criteria; <b>FALSE</b> otherwise.



