---
UID: NF:winddi.EngQueryPerformanceFrequency
title: EngQueryPerformanceFrequency function (winddi.h)
description: The EngQueryPerformanceFrequency function queries the frequency of the performance counter.
helpviewer_keywords: ["EngQueryPerformanceFrequency","EngQueryPerformanceFrequency function [Display Devices]","display.engqueryperformancefrequency","gdifncs_46139586-61a2-4418-9400-ac9bbce12167.xml","winddi/EngQueryPerformanceFrequency"]
old-location: display\engqueryperformancefrequency.htm
tech.root: display
ms.assetid: d4194278-eb49-43e4-b4bf-576e65d9e5ad
ms.date: 12/05/2018
ms.keywords: EngQueryPerformanceFrequency, EngQueryPerformanceFrequency function [Display Devices], display.engqueryperformancefrequency, gdifncs_46139586-61a2-4418-9400-ac9bbce12167.xml, winddi/EngQueryPerformanceFrequency
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngQueryPerformanceFrequency
 - winddi/EngQueryPerformanceFrequency
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-base-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngQueryPerformanceFrequency
---

# EngQueryPerformanceFrequency function


## -description

The <b>EngQueryPerformanceFrequency</b> function queries the frequency of the performance counter.

## -parameters

### -param pFrequency [out]

Pointer to a location that receives the performance counter frequency.

## -returns

None

## -remarks

The resolution of the timer is 1/<i>x</i>, where <i>x</i> is the value returned in the location to which <i>pFrequency</i> points. For example, if the value returned in <i>pFrequency</i> is 2 million, each tick is 1/2 millionth of a second. Each 1/<i>x</i> millionth increment of the count corresponds to one second of elapsed time.

A driver should call this routine sparingly. Frequent calls to <b>EngQueryPerformanceFrequency</b> can degrade the I/O performance for the calling driver and for the system as a whole.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engqueryperformancecounter">EngQueryPerformanceCounter</a>