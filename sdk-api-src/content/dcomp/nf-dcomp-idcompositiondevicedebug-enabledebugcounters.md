---
UID: NF:dcomp.IDCompositionDeviceDebug.EnableDebugCounters
title: IDCompositionDeviceDebug::EnableDebugCounters (dcomp.h)
description: Enables display of performance debugging counters.
helpviewer_keywords: ["EnableDebugCounters","EnableDebugCounters method [DirectComposition]","EnableDebugCounters method [DirectComposition]","IDCompositionDeviceDebug interface","IDCompositionDeviceDebug interface [DirectComposition]","EnableDebugCounters method","IDCompositionDeviceDebug.EnableDebugCounters","IDCompositionDeviceDebug::EnableDebugCounters","dcomp/IDCompositionDeviceDebug::EnableDebugCounters","directcomp.idcompositiondevicedebug_enabledebugcounters"]
old-location: directcomp\idcompositiondevicedebug_enabledebugcounters.htm
tech.root: directcomp
ms.assetid: AA0E913F-D89F-4AF1-91DE-B57D0C016DB7
ms.date: 12/05/2018
ms.keywords: EnableDebugCounters, EnableDebugCounters method [DirectComposition], EnableDebugCounters method [DirectComposition],IDCompositionDeviceDebug interface, IDCompositionDeviceDebug interface [DirectComposition],EnableDebugCounters method, IDCompositionDeviceDebug.EnableDebugCounters, IDCompositionDeviceDebug::EnableDebugCounters, dcomp/IDCompositionDeviceDebug::EnableDebugCounters, directcomp.idcompositiondevicedebug_enabledebugcounters
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDCompositionDeviceDebug::EnableDebugCounters
 - dcomp/IDCompositionDeviceDebug::EnableDebugCounters
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionDeviceDebug.EnableDebugCounters
---

# IDCompositionDeviceDebug::EnableDebugCounters


## -description

Enables display of performance debugging counters.



## -returns

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

Performance counters are displayed on the top-right corner of the screen. From left to right, Microsoft DirectComposition displays the following information:



<ul>
<li>The composition engine frame rate, in frames per second, averaged over the last 60 composition frames</li>
<li>The overall CPU usage of the composition thread, in milliseconds
</li>
</ul>
The DirectComposition composition engine operates on the entire desktop all at once, so the performance counters measure the total cost of desktop composition, not just the cost of any one particular application. If the application occupies the entire screen, however, it is reasonable to assume that all of the composition cost is due to that one application.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevicedebug">IDCompositionDeviceDebug</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevicedebug-disabledebugcounters">IDCompositionDeviceDebug::DisableDebugCounters</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisualdebug">IDCompositionVisualDebug</a>
