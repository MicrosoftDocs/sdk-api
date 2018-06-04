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



