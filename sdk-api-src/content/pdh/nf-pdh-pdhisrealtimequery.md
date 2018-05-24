---
UID: NF:pdh.PdhIsRealTimeQuery
title: PdhIsRealTimeQuery function
author: windows-driver-content
description: Determines if the specified query is a real-time query.
old-location: perf\pdhisrealtimequery.htm
old-project: PerfCtrs
ms.assetid: 4f6b2d8d-3a0f-4346-8b8e-a7aea11fbc40
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: PdhIsRealTimeQuery, PdhIsRealTimeQuery function [Perf], _win32_pdhisrealtimequery, base.pdhisrealtimequery, pdh/PdhIsRealTimeQuery, perf.pdhisrealtimequery
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
req.typenames: CHANNEL_PDU_HEADER, *PCHANNEL_PDU_HEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Pdh.dll
api_name:
-	PdhIsRealTimeQuery
product: Windows
targetos: Windows
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PdhIsRealTimeQuery function


## -description



			Determines if the specified query is a real-time query.
		


## -parameters




### -param hQuery [in]

Handle to the query. The 
<a href="https://msdn.microsoft.com/ec4e5353-c7f5-4957-b7f4-39df508846a0">PdhOpenQuery</a> function returns this handle.


## -returns




						If the query is a real-time query, the return value is <b>TRUE</b>.
						

If the query is not a real-time query, the return value is <b>FALSE</b>.




## -remarks



The term <i>real-time</i> as used in the description of this function does not imply the standard meaning of the term <i>real-time</i>. Instead, it describes the collection of performance data from a source providing current information (for example, the registry or a WMI provider) rather than from a log file.




## -see-also




<a href="https://msdn.microsoft.com/ec4e5353-c7f5-4957-b7f4-39df508846a0">PdhOpenQuery</a>



<a href="https://msdn.microsoft.com/211d4504-e1f9-48a0-8ddd-613f2f183c59">PdhSelectDataSource</a>
 

 

