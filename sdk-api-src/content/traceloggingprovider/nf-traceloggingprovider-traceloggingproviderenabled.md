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



