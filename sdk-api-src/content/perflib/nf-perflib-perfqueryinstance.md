---
UID: NF:perflib.PerfQueryInstance
title: PerfQueryInstance function
author: windows-driver-content
description: Retrieves a pointer to the specified counter set instance. Providers use this function.
old-location: perf\perfqueryinstance.htm
old-project: PerfCtrs
ms.assetid: 844f3f9e-8de2-4995-b13c-befe0da8a1ab
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: PerfQueryInstance, PerfQueryInstance function [Perf], base.perfqueryinstance, perf.perfqueryinstance, perflib/PerfQueryInstance
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PerfRegInfoType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
-	API-MS-Win-Core-perfcounters-l1-1-0.dll
-	KernelBase.dll
api_name:
-	PerfQueryInstance
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PerfQueryInstance function


## -description


Retrieves a pointer to the specified counter set instance. Providers use this function.


## -parameters




### -param ProviderHandle

TBD


### -param CounterSetGuid [in]

GUID that uniquely identifies the counter set that you want to query. This is the same GUID specified in the <b>guid</b> attribute of the <a href="https://msdn.microsoft.com/">counterSet</a> element. Use the GUID variable that the <a href="https://msdn.microsoft.com/3939f6a1-0a94-429d-a71e-b37f045fea13">CTRPP</a> tool generated for you. For the name of the variable, see the <b>symbol</b> attribute of the <b>counterSet</b> element.

<b>Windows Vista:  </b>The GUID variable is not available.


### -param Name

TBD


### -param Id

TBD




#### - dwInstance [in]

Unique identifier of the counter set instance that you want to retrieve.


#### - hProvider [in]

The handle of the provider. Use the handle variable that the <a href="https://msdn.microsoft.com/3939f6a1-0a94-429d-a71e-b37f045fea13">CTRPP</a> tool generated for you. For the name of the variable, see the <b>symbol</b> attribute of the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406455">provider</a> element.

<b>Windows Vista:  </b>The <a href="https://msdn.microsoft.com/b417b19b-adbc-40e3-aca1-c2cd94a79232">PerfStartProvider</a> function returns the handle.


#### - szInstance [in]

<b>Null</b>-terminated Unicode string that contains the name of counter set instance that you want to retrieve.


## -returns



A <a href="https://msdn.microsoft.com/709d5339-cedd-4b03-9d8e-c125eb3bcac0">PERF_COUNTERSET_INSTANCE</a> structure that contains the counter set instance or <b>NULL</b> if the instance does not exist.

This function returns <b>NULL</b> if an error occurred. To determine the error that occurred, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



Use the same instance name and identifier that you used when calling <a href="https://msdn.microsoft.com/73be8588-2c87-4c27-933d-62b8605ed9a3">PerfCreateInstance</a> to retrieve a specific instance of the counter set.

Providers should  cache the pointer to the instance when they create the instance instead of calling this function to retrieve the pointer. 




## -see-also




<a href="https://msdn.microsoft.com/73be8588-2c87-4c27-933d-62b8605ed9a3">PerfCreateInstance</a>
 

 

