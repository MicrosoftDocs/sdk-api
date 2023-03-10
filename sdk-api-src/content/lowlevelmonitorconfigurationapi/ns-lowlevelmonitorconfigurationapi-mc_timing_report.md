---
UID: NS:lowlevelmonitorconfigurationapi._MC_TIMING_REPORT
title: MC_TIMING_REPORT (lowlevelmonitorconfigurationapi.h)
description: Contains information from a monitor's timing report.
helpviewer_keywords: ["*LPMC_TIMING_REPORT","LPMC_TIMING_REPORT","LPMC_TIMING_REPORT structure pointer [Monitor Configuration]","MC_TIMING_REPORT","MC_TIMING_REPORT structure [Monitor Configuration]","lowlevelmonitorconfigurationapi/LPMC_TIMING_REPORT","lowlevelmonitorconfigurationapi/MC_TIMING_REPORT","monitor.mc_timing_report"]
old-location: monitor\mc_timing_report.htm
tech.root: Monitor
ms.assetid: dfad2277-4f0d-4a92-a332-2c6c2bbac138
ms.date: 12/05/2018
ms.keywords: '*LPMC_TIMING_REPORT, LPMC_TIMING_REPORT, LPMC_TIMING_REPORT structure pointer [Monitor Configuration], MC_TIMING_REPORT, MC_TIMING_REPORT structure [Monitor Configuration], lowlevelmonitorconfigurationapi/LPMC_TIMING_REPORT, lowlevelmonitorconfigurationapi/MC_TIMING_REPORT, monitor.mc_timing_report'
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
targetos: Windows
req.typenames: MC_TIMING_REPORT, *LPMC_TIMING_REPORT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MC_TIMING_REPORT
 - lowlevelmonitorconfigurationapi/_MC_TIMING_REPORT
 - LPMC_TIMING_REPORT
 - lowlevelmonitorconfigurationapi/LPMC_TIMING_REPORT
 - MC_TIMING_REPORT
 - lowlevelmonitorconfigurationapi/MC_TIMING_REPORT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - LowLevelMonitorConfigurationAPI.h
api_name:
 - MC_TIMING_REPORT
---

# MC_TIMING_REPORT structure


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

<a href="/windows/desktop/api/lowlevelmonitorconfigurationapi/nf-lowlevelmonitorconfigurationapi-gettimingreport">GetTimingReport</a>



<a href="/windows/desktop/Monitor/monitor-configuration-structures">Monitor Configuration Structures</a>