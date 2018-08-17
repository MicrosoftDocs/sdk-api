---
UID: NF:winddi.EngQueryPerformanceFrequency
title: EngQueryPerformanceFrequency function
author: windows-sdk-content
description: The EngQueryPerformanceFrequency function queries the frequency of the performance counter.
old-location: display\engqueryperformancefrequency.htm
old-project: display
ms.assetid: d4194278-eb49-43e4-b4bf-576e65d9e5ad
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: EngQueryPerformanceFrequency, EngQueryPerformanceFrequency function [Display Devices], display.engqueryperformancefrequency, gdifncs_46139586-61a2-4418-9400-ac9bbce12167.xml, winddi/EngQueryPerformanceFrequency
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.redist: 
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngQueryPerformanceFrequency
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
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




<a href="https://msdn.microsoft.com/6f351bd7-586e-4fd0-ad20-779b18eaa4dc">EngQueryPerformanceCounter</a>
 

 

