---
UID: NF:dcomp.IDCompositionDeviceDebug.DisableDebugCounters
title: IDCompositionDeviceDebug::DisableDebugCounters
author: windows-sdk-content
description: Disables display of performance debugging counters.
old-location: directcomp\idcompositiondevicedebug_disabledebugcounters.htm
tech.root: directcomp
ms.assetid: 7B1E35D4-8CB3-4AAC-91D9-E1191A6DC169
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DisableDebugCounters, DisableDebugCounters method [DirectComposition], DisableDebugCounters method [DirectComposition],IDCompositionDeviceDebug interface, IDCompositionDeviceDebug interface [DirectComposition],DisableDebugCounters method, IDCompositionDeviceDebug.DisableDebugCounters, IDCompositionDeviceDebug::DisableDebugCounters, dcomp/IDCompositionDeviceDebug::DisableDebugCounters, directcomp.idcompositiondevicedebug_disabledebugcounters
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDCompositionDeviceDebug.DisableDebugCounters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionDeviceDebug::DisableDebugCounters


## -description


Disables display of performance debugging counters.


## -parameters






## -returns



If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



Microsoft DirectComposition keeps a count of how many DirectComposition devices have performance counters enabled, for the entire desktop session. If the count is non-zero, the performance counters are displayed. Therefore, disabling the counters may not make them go away if another device is also requesting display of the counters.




## -see-also




<a href="https://msdn.microsoft.com/B8D17570-9729-45DB-99E1-A2EBBDAA5996">IDCompositionDeviceDebug</a>



<a href="https://msdn.microsoft.com/AA0E913F-D89F-4AF1-91DE-B57D0C016DB7">IDCompositionDeviceDebug::EnableDebugCounters</a>
 

 

