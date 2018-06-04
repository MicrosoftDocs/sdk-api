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

# CoWaitForMultipleObjects function


## -description


A replacement for <a href="https://msdn.microsoft.com/3eeecd34-aa94-4a48-8b41-167a71b52860">CoWaitForMultipleHandles</a>. This replacement API hides the options for <b>CoWaitForMultipleHandles</b> that are not supported in ASTA.


## -parameters




### -param dwFlags [in]


<a href="https://msdn.microsoft.com/5FE605A9-DE92-4CD9-9390-6C9F5189A7CB">CWMO_FLAGS</a> flag controlling whether call/window message reentrancy is enabled from this wait. By default, neither COM calls nor window messages are dispatched from <b>CoWaitForMultipleObjects</b> in ASTA.


### -param dwTimeout [in]

The timeout in milliseconds of the wait.


### -param cHandles [in]

The length of the <i>pHandles</i> array. Must be &lt;= 56.


### -param pHandles [in]

An array of handles to waitable kernel objects.


### -param lpdwindex

TBD




#### - lpdwIndex [out]

Receives the index of the handle that satisfied the wait.


## -returns



Same return values as <a href="https://msdn.microsoft.com/3eeecd34-aa94-4a48-8b41-167a71b52860">CoWaitForMultipleHandles</a>, except the ASTA-specific CO_E_NOTSUPPORTED cases instead return E_INVALIDARG from all apartment types.



