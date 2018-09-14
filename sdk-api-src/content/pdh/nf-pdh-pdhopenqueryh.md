---
UID: NF:pdh.PdhOpenQueryH
title: PdhOpenQueryH function
author: windows-sdk-content
description: Creates a new query that is used to manage the collection of performance data. This function is identical to the PdhOpenQuery function, except that it supports the use of handles to data sources.
old-location: perf\pdhopenqueryh.htm
tech.root: PerfCtrs
ms.assetid: 068c55da-d7e0-4111-91c8-a2bbd676f99d
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: PdhOpenQueryH, PdhOpenQueryH function [Perf], _win32_pdhopenqueryh, base.pdhopenqueryh, pdh/PdhOpenQueryH, perf.pdhopenqueryh
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Pdh.dll
api_name:
 - PdhOpenQueryH
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PdhOpenQueryH function


## -description


Creates a new query that is used to manage the collection of performance data.
			

This function is identical to 
the <a href="https://msdn.microsoft.com/ec4e5353-c7f5-4957-b7f4-39df508846a0">PdhOpenQuery</a> function, except that it supports the use of handles to data sources.


## -parameters




### -param hDataSource [in]

Handle to a data source returned by the 
<a href="https://msdn.microsoft.com/eaed9b28-eb09-4123-9317-5d3d50e2d77a">PdhBindInputDataSource</a> function.


### -param dwUserData [in]

User-defined value to associate with this query. To retrieve the user data later, call 
the <a href="https://msdn.microsoft.com/12e1a194-5418-4c2a-9853-ef2d2c666893">PdhGetCounterInfo</a> function and access the <b>dwQueryUserData</b> member of <a href="https://msdn.microsoft.com/c9ede50e-85de-4a68-b539-54285c2599cb">PDH_COUNTER_INFO</a>.


### -param phQuery [out]

Handle to the query. You use this handle in subsequent calls.


## -returns



If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> or a 
<a href="https://msdn.microsoft.com/ea67d798-81db-44ad-b0fb-24e0c3be7388">PDH error code</a>. 




## -see-also




<a href="https://msdn.microsoft.com/eaed9b28-eb09-4123-9317-5d3d50e2d77a">PdhBindInputDataSource</a>
 

 

