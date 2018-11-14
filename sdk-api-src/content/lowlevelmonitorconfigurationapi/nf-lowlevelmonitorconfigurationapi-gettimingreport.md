---
UID: NF:lowlevelmonitorconfigurationapi.GetTimingReport
title: GetTimingReport function
author: windows-sdk-content
description: Retrieves a monitor's horizontal and vertical synchronization frequencies.
old-location: monitor\gettimingreport.htm
tech.root: Monitor
ms.assetid: 17b5a7e4-936f-451f-b586-032f94a99be5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetTimingReport, GetTimingReport function [Monitor Configuration], lowlevelmonitorconfigurationapi/GetTimingReport, monitor.gettimingreport
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Dxva2.lib
req.dll: Dxva2.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dxva2.dll
api_name:
 - GetTimingReport
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetTimingReport
: 
---

# GetTimingReport function


## -description


Retrieves a monitor's horizontal and vertical synchronization frequencies.


## -parameters




### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="https://msdn.microsoft.com/f2ac8a6a-3be9-4155-ad13-c256b96da792">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://msdn.microsoft.com/1e0e9749-8ee4-42d5-ab7b-182222b6c429">GetPhysicalMonitorsFromIDirect3DDevice9</a>.
          


### -param pmtrMonitorTimingReport [out]

Pointer to an <a href="https://msdn.microsoft.com/dfad2277-4f0d-4a92-a332-2c6c2bbac138">MC_TIMING_REPORT</a> structure that receives the timing information.
          


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.
          




## -remarks



This function corresponds to the "Get Timing Report &amp; Timing Message" command from the Display Data Channel Command Interface (DDC/CI) standard. For more information about the timing information, refer to the DDC/CI standard.
      

This function takes about 50 milliseconds to return.
      




## -see-also




<a href="https://msdn.microsoft.com/e9a00792-f471-47a4-93d7-25400e27f13f">Monitor Configuration Functions</a>
 

 

