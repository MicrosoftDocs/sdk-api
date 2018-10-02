---
UID: NS:lowlevelmonitorconfigurationapi._MC_TIMING_REPORT
title: "_MC_TIMING_REPORT"
author: windows-sdk-content
description: Contains information from a monitor's timing report.
old-location: monitor\mc_timing_report.htm
tech.root: Monitor
ms.assetid: dfad2277-4f0d-4a92-a332-2c6c2bbac138
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPMC_TIMING_REPORT, LPMC_TIMING_REPORT, LPMC_TIMING_REPORT structure pointer [Monitor Configuration], MC_TIMING_REPORT, MC_TIMING_REPORT structure [Monitor Configuration], _MC_TIMING_REPORT, lowlevelmonitorconfigurationapi/LPMC_TIMING_REPORT, lowlevelmonitorconfigurationapi/MC_TIMING_REPORT, monitor.mc_timing_report"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: lowlevelmonitorconfigurationapi.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - LowLevelMonitorConfigurationAPI.h
api_name:
 - MC_TIMING_REPORT
product: Windows
targetos: Windows
req.typenames: MC_TIMING_REPORT, *LPMC_TIMING_REPORT
req.redist: 
---

# _MC_TIMING_REPORT structure


## -description


Contains information from a monitor's timing report.


## -struct-fields




### -field dwHorizontalFrequencyInHZ

The monitor's horizontal synchronization frequency in Hz.
          


### -field dwVerticalFrequencyInHZ

The monitor's vertical synchronization frequency in Hz.
          


### -field bTimingStatusByte

Timing status byte. For more information about this value, see the Display Data Channel Command Interface (DDC/CI) standard.
          


## -see-also




<a href="https://msdn.microsoft.com/17b5a7e4-936f-451f-b586-032f94a99be5">GetTimingReport</a>



<a href="https://msdn.microsoft.com/4aca3a00-d2c6-42a6-9143-72e42c1d33bb">Monitor Configuration Structures</a>
 

 

