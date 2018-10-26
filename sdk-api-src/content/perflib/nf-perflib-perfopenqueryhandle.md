---
UID: NF:perflib.PerfOpenQueryHandle
title: PerfOpenQueryHandle function
author: windows-sdk-content
description: Creates a handle that references a query on the specified system. A query is a list of counter specifications.
old-location: perf\perfopenqueryhandle.htm
tech.root: perfctrs
ms.assetid: 5105F617-9443-451D-B802-C6A241769E65
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: PerfOpenQueryHandle, PerfOpenQueryHandle function [Perf], perf.perfopenqueryhandle, perflib/PerfOpenQueryHandle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: perflib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: AdvAPI32.lib
req.dll: AdvAPI32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - AdvAPI32.dll
api_name:
 - PerfOpenQueryHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PerfOpenQueryHandle function


## -description


Creates a handle that references a query on the specified system. A query is a
list of counter specifications.


## -parameters




### -param szMachine [in, optional]

The name of the machine for which you want to get the query handle.


### -param phQuery [out]

The handle to the query. Call <a href="https://msdn.microsoft.com/94D08CF1-D47C-4A1B-A0CE-8C318CDF9FE0">PerfCloseQueryHandle</a> to close ths handle when you no longer need it.


## -returns



If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. 




## -remarks



Use <a href="https://msdn.microsoft.com/FC66E794-EF13-47BB-A704-735924363310">PerfAddCounters</a> and <a href="https://msdn.microsoft.com/330CA041-41CA-4C48-B88B-C48A0143505E">PerfDeleteCounters</a> to
add or remove counter specifications to the list. Use <a href="https://msdn.microsoft.com/42CAB98C-4525-499D-BA11-731A666E112D">PerfQueryCounterInfo</a> to
get the counter specifications currently in the list and to determine the
indexes at which the data for each counter will be returned by 
<a href="https://msdn.microsoft.com/EBCF00E0-6C40-40E5-9F3D-9AE5F9AB74AC">PerfQueryCounterData</a>. Use <b>PerfQueryCounterData</b> to retrieve the values of the
counters that match the counter specifications.





## -see-also




<a href="https://msdn.microsoft.com/FC66E794-EF13-47BB-A704-735924363310">PerfAddCounters</a>



<a href="https://msdn.microsoft.com/94D08CF1-D47C-4A1B-A0CE-8C318CDF9FE0">PerfCloseQueryHandle</a>



<a href="https://msdn.microsoft.com/330CA041-41CA-4C48-B88B-C48A0143505E">PerfDeleteCounters</a>



<a href="https://msdn.microsoft.com/EBCF00E0-6C40-40E5-9F3D-9AE5F9AB74AC">PerfQueryCounterData</a>



<a href="https://msdn.microsoft.com/42CAB98C-4525-499D-BA11-731A666E112D">PerfQueryCounterInfo</a>
 

 

