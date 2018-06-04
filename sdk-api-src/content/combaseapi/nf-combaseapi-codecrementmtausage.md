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

# CoDecrementMTAUsage function


## -description


Releases the increment made by a previous call to the <a href="https://msdn.microsoft.com/EFE6E66A-96A3-4B51-92DD-1CE84B1F0185">CoIncrementMTAUsage</a> function.


## -parameters




### -param Cookie [in]

A <b>PVOID</b> variable that was set by a previous call to the <a href="https://msdn.microsoft.com/EFE6E66A-96A3-4B51-92DD-1CE84B1F0185">CoIncrementMTAUsage</a> function.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<i>Cookie</i> must be a valid value returned by a successful previous call to the  <a href="https://msdn.microsoft.com/EFE6E66A-96A3-4B51-92DD-1CE84B1F0185">CoIncrementMTAUsage</a> function. If the overall count of MTA usage reaches 0, including both through this API and through the <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> and <a href="https://msdn.microsoft.com/9411cbed-fa3b-46f7-b677-6ada53324edc">CoUninitialize</a> functions, the system frees resources related to MTA support.

You can call <a href="https://msdn.microsoft.com/EFE6E66A-96A3-4B51-92DD-1CE84B1F0185">CoIncrementMTAUsage</a> from one thread and <b>CoDecrementMTAUsage</b> from another as long as a cookie previously returned by <b>CoIncrementMTAUsage</b> is passed to <b>CoDecrementMTAUsage</b>. 

Don't call <b>CoDecrementMTAUsage</b> during process shutdown or inside dllmain. You can call <b>CoDecrementMTAUsage</b> before the call to start the shutdown process.




## -see-also




<a href="https://msdn.microsoft.com/EFE6E66A-96A3-4B51-92DD-1CE84B1F0185">CoIncrementMTAUsage</a>
 

 

