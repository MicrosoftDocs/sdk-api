---
UID: NF:dcomp.IDCompositionDeviceDebug.EnableDebugCounters
title: IDCompositionDeviceDebug::EnableDebugCounters
author: windows-sdk-content
description: Enables display of performance debugging counters.
old-location: directcomp\idcompositiondevicedebug_enabledebugcounters.htm
tech.root: directcomp
ms.assetid: AA0E913F-D89F-4AF1-91DE-B57D0C016DB7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EnableDebugCounters, EnableDebugCounters method [DirectComposition], EnableDebugCounters method [DirectComposition],IDCompositionDeviceDebug interface, IDCompositionDeviceDebug interface [DirectComposition],EnableDebugCounters method, IDCompositionDeviceDebug.EnableDebugCounters, IDCompositionDeviceDebug::EnableDebugCounters, dcomp/IDCompositionDeviceDebug::EnableDebugCounters, directcomp.idcompositiondevicedebug_enabledebugcounters
ms.topic: method
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionDeviceDebug.EnableDebugCounters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionDeviceDebug::EnableDebugCounters


## -description


Enables display of performance debugging counters.


## -parameters






## -returns



If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



Performance counters are displayed on the top-right corner of the screen. From left to right, Microsoft DirectComposition displays the following information:



<ul>
<li>The composition engine frame rate, in frames per second, averaged over the last 60 composition frames</li>
<li>The overall CPU usage of the composition thread, in milliseconds
</li>
</ul>
The DirectComposition composition engine operates on the entire desktop all at once, so the performance counters measure the total cost of desktop composition, not just the cost of any one particular application. If the application occupies the entire screen, however, it is reasonable to assume that all of the composition cost is due to that one application.





## -see-also




<a href="https://msdn.microsoft.com/B8D17570-9729-45DB-99E1-A2EBBDAA5996">IDCompositionDeviceDebug</a>



<a href="https://msdn.microsoft.com/7B1E35D4-8CB3-4AAC-91D9-E1191A6DC169">IDCompositionDeviceDebug::DisableDebugCounters</a>



<a href="https://msdn.microsoft.com/0AF98EEB-3EA7-44E3-8F2F-182D9F6BCCA4">IDCompositionVisualDebug</a>
 

 

