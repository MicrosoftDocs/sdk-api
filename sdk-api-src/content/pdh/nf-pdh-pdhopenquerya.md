---
UID: NF:pdh.PdhOpenQueryA
title: PdhOpenQueryA function
author: windows-sdk-content
description: Creates a new query that is used to manage the collection of performance data. To use handles to data sources, use the PdhOpenQueryH function.
old-location: perf\pdhopenquery.htm
tech.root: perfctrs
ms.assetid: ec4e5353-c7f5-4957-b7f4-39df508846a0
ms.author: windowssdkdev
ms.date: 08/08/2018
ms.keywords: PdhOpenQuery, PdhOpenQuery function [Perf], PdhOpenQueryA, PdhOpenQueryW, _win32_pdhopenquery, base.pdhopenquery, pdh/PdhOpenQuery, pdh/PdhOpenQueryA, pdh/PdhOpenQueryW, perf.pdhopenquery
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
req.unicode-ansi: PdhOpenQueryW (Unicode) and PdhOpenQueryA (ANSI)
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
 - PdhOpenQuery
 - PdhOpenQueryA
 - PdhOpenQueryW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PdhOpenQueryA function


## -description


Creates a new query that is used to manage the collection of performance data.
			

To use handles to data sources, use the 
<a href="https://msdn.microsoft.com/068c55da-d7e0-4111-91c8-a2bbd676f99d">PdhOpenQueryH</a> function.


## -parameters




### -param szDataSource [in]

<b>Null</b>-terminated string that specifies the name of the log file from which to retrieve performance data. If <b>NULL</b>, performance data is collected from a real-time data source. 



					


### -param dwUserData [in]

User-defined value to associate with this query. To retrieve the user data later, call 
<a href="https://msdn.microsoft.com/12e1a194-5418-4c2a-9853-ef2d2c666893">PdhGetCounterInfo</a> and access the <b>dwQueryUserData</b> member of <a href="https://msdn.microsoft.com/c9ede50e-85de-4a68-b539-54285c2599cb">PDH_COUNTER_INFO</a>.


### -param phQuery [out]

Handle to the query. You use this handle in subsequent calls.


## -returns



If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> or a 
<a href="https://msdn.microsoft.com/ea67d798-81db-44ad-b0fb-24e0c3be7388">PDH error code</a>. 




## -see-also




<a href="https://msdn.microsoft.com/af0fb9f4-3999-48fa-88d7-aa59b5caed75">PdhCloseQuery</a>



<a href="https://msdn.microsoft.com/12e1a194-5418-4c2a-9853-ef2d2c666893">PdhGetCounterInfo</a>



<a href="https://msdn.microsoft.com/4f6b2d8d-3a0f-4346-8b8e-a7aea11fbc40">PdhIsRealTimeQuery</a>



<a href="https://msdn.microsoft.com/068c55da-d7e0-4111-91c8-a2bbd676f99d">PdhOpenQueryH</a>



<a href="https://msdn.microsoft.com/5a46ac26-c1a1-40c1-a328-688e0b394e18">PdhSetDefaultRealTimeDataSource</a>
 

 

