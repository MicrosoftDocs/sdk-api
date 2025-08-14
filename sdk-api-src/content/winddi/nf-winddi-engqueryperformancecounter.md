---
UID: NF:winddi.EngQueryPerformanceCounter
title: EngQueryPerformanceCounter function (winddi.h)
description: The EngQueryPerformanceCounter function queries the performance counter.
helpviewer_keywords: ["EngQueryPerformanceCounter","EngQueryPerformanceCounter function [Display Devices]","display.engqueryperformancecounter","gdifncs_8a5d6431-cd14-42cd-bcd4-2d27342bc08a.xml","winddi/EngQueryPerformanceCounter"]
old-location: display\engqueryperformancecounter.htm
tech.root: display
ms.assetid: 6f351bd7-586e-4fd0-ad20-779b18eaa4dc
ms.date: 12/05/2018
ms.keywords: EngQueryPerformanceCounter, EngQueryPerformanceCounter function [Display Devices], display.engqueryperformancecounter, gdifncs_8a5d6431-cd14-42cd-bcd4-2d27342bc08a.xml, winddi/EngQueryPerformanceCounter
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
 - EngQueryPerformanceCounter
 - winddi/EngQueryPerformanceCounter
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
 - EngQueryPerformanceCounter
---

# EngQueryPerformanceCounter function


## -description

The <b>EngQueryPerformanceCounter</b> function queries the performance counter.

## -parameters

### -param pPerformanceCount [out]

Pointer to a location that receives the performance counter value, in hertz.

## -returns

None

## -remarks

<b>EngQueryPerformanceCounter</b> always returns a 64-bit integer that represents the number of ticks per second. The count begins accumulating when the system is booted.

A driver should call this routine sparingly. Frequent calls to <b>EngQueryPerformanceCounter</b> can degrade the I/O performance for the calling driver and for the system as a whole.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engqueryperformancefrequency">EngQueryPerformanceFrequency</a>