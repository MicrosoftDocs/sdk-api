---
UID: NF:perflib.PerfSetCounterSetInfo
title: PerfSetCounterSetInfo function
author: windows-sdk-content
description: Specifies the layout of a particular counter set.
old-location: perf\perfsetcountersetinfo.htm
old-project: PerfCtrs
ms.assetid: b4295503-5588-4898-816c-939a5920fc77
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PerfSetCounterSetInfo, PerfSetCounterSetInfo function [Perf], base.perfsetcountersetinfo, perf.perfsetcountersetinfo, perflib/PerfSetCounterSetInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: perflib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PerfRegInfoType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Core-perfcounters-l1-1-0.dll
 - KernelBase.dll
api_name:
 - PerfSetCounterSetInfo
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PerfSetCounterSetInfo function


## -description


Specifies the layout of a particular counter set.


## -parameters




### -param ProviderHandle

TBD


### -param Template

TBD


### -param TemplateSize

TBD




#### - dwTemplateSize [in]

Size, in bytes, of the <i>pTemplate</i> buffer.


#### - hProvider [in]

The handle of the provider. Use the handle variable that the <a href="https://msdn.microsoft.com/3939f6a1-0a94-429d-a71e-b37f045fea13">CTRPP</a> tool generated for you. For the name of the variable, see the <b>symbol</b> attribute of the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406455">provider</a> element.

<b>Windows Vista:  </b>The <a href="https://msdn.microsoft.com/b417b19b-adbc-40e3-aca1-c2cd94a79232">PerfStartProvider</a> function returns the handle.


#### - pTemplate [in]

Buffer that contains the counter set information. For details, see <a href="https://msdn.microsoft.com/bf48dcdb-6fdd-4093-9006-a53690c3ed86">PERF_COUNTERSET_INFO</a>.


## -returns




						If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. 




## -remarks



The <a href="https://msdn.microsoft.com/edcf8df3-0f6d-4849-b41d-270509499b8e">CounterInitialize</a> function calls this function; do not call this function directly.

<b>Windows Vista:  </b>The <b>PerfAutoInitialize</b> function calls this function.



