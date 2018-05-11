---
UID: NF:winddi.EngQueryPerformanceCounter
title: EngQueryPerformanceCounter function
author: windows-driver-content
description: The EngQueryPerformanceCounter function queries the performance counter.
old-location: display\engqueryperformancecounter.htm
old-project: display
ms.assetid: 6f351bd7-586e-4fd0-ad20-779b18eaa4dc
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: EngQueryPerformanceCounter, EngQueryPerformanceCounter function [Display Devices], display.engqueryperformancecounter, gdifncs_8a5d6431-cd14-42cd-bcd4-2d27342bc08a.xml, winddi/EngQueryPerformanceCounter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Win32k.sys
api_name:
-	EngQueryPerformanceCounter
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
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




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564996">EngQueryPerformanceFrequency</a>
 

 

