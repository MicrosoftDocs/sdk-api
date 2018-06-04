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

# IInitializeSpy::PostInitialize


## -description


Performs initialization steps required after calling the <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> function.


## -parameters




### -param hrCoInit [in]

The value returned by <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a>.


### -param dwCoInit [in]

The apartment type passed to <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a>, specified as a member of the <a href="https://msdn.microsoft.com/0ac4a809-05f8-46d7-8e79-9d4e88b487f4">COINIT</a> enumeration.


### -param dwNewThreadAptRefs [in]

The number of times <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> has been called on this thread.


## -returns



This method returns the value that it intends the <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> call to return to its caller. For more information, see the Remarks section.




## -remarks



The return value from <b>PostInitialize</b> is intended to be the returned <b>HRESULT</b> from the call to <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a>. This is always the case for a single active registration on this thread.

For cases where there are multiple registrations active on this thread, the returned <b>HRESULT</b> is arrived at by chaining of the various <b>PostInitialize</b> methods as follows: The COM determined <b>HRESULT</b> will be passed as the <i>hrCoInit</i> parameter to the first <b>PostInitialize</b> method called. The <b>HRESULT</b> from that <b>PostInitialize</b> call will be passed as the <i>hrCoInit</i> parameter to the next <b>PostInitialize</b> call. This chaining continues leading to the <b>HRESULT</b> from the last <b>PostInitialize</b> call being returned as the <b>HRESULT</b> from the call to <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a>.





## -see-also




<a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a>



<a href="https://msdn.microsoft.com/9cf1a3fa-dbc6-4760-a9e9-ef237737acfb">IInitializeSpy</a>
 

 

