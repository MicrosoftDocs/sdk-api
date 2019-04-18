---
UID: NF:perflib.PerfCloseQueryHandle
title: PerfCloseQueryHandle function (perflib.h)
author: windows-sdk-content
description: Closes a query handle that you opened by calling PerfOpenQueryHandle.
old-location: perf\perfclosequeryhandle.htm
tech.root: perfctrs
ms.assetid: 94D08CF1-D47C-4A1B-A0CE-8C318CDF9FE0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PerfCloseQueryHandle, PerfCloseQueryHandle function [Perf], perf.perfclosequeryhandle, perflib/PerfCloseQueryHandle
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
 - PerfCloseQueryHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PerfCloseQueryHandle function


## -description


Closes a query handle that you opened by calling <a href="https://msdn.microsoft.com/5105F617-9443-451D-B802-C6A241769E65">PerfOpenQueryHandle</a>.


## -parameters




### -param hQuery [in]

A handle to the query that you want to close


## -returns



If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. 




## -see-also




<a href="https://msdn.microsoft.com/5105F617-9443-451D-B802-C6A241769E65">PerfOpenQueryHandle</a>
 

 

