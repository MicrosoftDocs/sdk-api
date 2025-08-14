---
UID: NF:perflib.PerfDeleteInstance
title: PerfDeleteInstance function (perflib.h)
description: Deletes an instance of the counter set created by the PerfCreateInstance function.
helpviewer_keywords: ["PerfDeleteInstance","PerfDeleteInstance function [Perf]","base.perfdeleteinstance","perf.perfdeleteinstance","perflib/PerfDeleteInstance"]
old-location: perf\perfdeleteinstance.htm
tech.root: perf
ms.assetid: 8266e58c-c0a3-42dd-9f06-0d04dccfcf7c
ms.date: 12/05/2018
ms.keywords: PerfDeleteInstance, PerfDeleteInstance function [Perf], base.perfdeleteinstance, perf.perfdeleteinstance, perflib/PerfDeleteInstance
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PerfDeleteInstance
 - perflib/PerfDeleteInstance
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-perfcounters-l1-2-0.dll
 - Advapi32.dll
 - API-MS-Win-Core-perfcounters-l1-1-0.dll
 - KernelBase.dll
api_name:
 - PerfDeleteInstance
---

# PerfDeleteInstance function


## -description

Deletes an instance of the counter set  created by the <a href="/windows/desktop/api/perflib/nf-perflib-perfcreateinstance">PerfCreateInstance</a> function.   Providers use this function.

## -parameters

### -param Provider [in]

The handle of the provider. Use the handle variable that the <a href="/windows/desktop/PerfCtrs/ctrpp">CTRPP</a> tool generated for you. For the name of the variable, see the <b>symbol</b> attribute of the <a href="/previous-versions/aa373164(v=vs.85)">provider</a> element.

<b>Windows Vista:  </b>The <a href="/windows/desktop/api/perflib/nf-perflib-perfstartprovider">PerfStartProvider</a> function returns the handle.

### -param InstanceBlock [in]

A <a href="/windows/desktop/api/perflib/ns-perflib-perf_counterset_instance">PERF_COUNTERSET_INSTANCE</a> structure that contains the instance of the counter set to delete.

## -returns

If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

If the provider process terminates abnormally, all allocated instances will be released.

The provider determines when it deletes an instance. If the counter data is more static, the provider can delete an instance at cleanup time. For example, the number of processors on a computer would be considered static, so a provider that provides counter data for processors could delete an instance for each processor on the computer at cleanup time. For counters that are more dynamic, such as disk or process counters, the providers would delete the instances in response to a USB device being removed or a process being terminated.

## -see-also

<a href="/windows/desktop/api/perflib/nf-perflib-perfcreateinstance">PerfCreateInstance</a>



<a href="/windows/desktop/api/perflib/nf-perflib-perfqueryinstance">PerfQueryInstance</a>