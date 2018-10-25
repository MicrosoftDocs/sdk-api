---
UID: NF:pdh.PdhBrowseCountersHW
title: PdhBrowseCountersHW function
author: windows-sdk-content
description: Displays a Browse Counters dialog box that the user can use to select one or more counters that they want to add to the query. This function is identical to the PdhBrowseCounters function, except that it supports the use of handles to data sources.
old-location: perf\pdhbrowsecountersh.htm
tech.root: perfctrs
ms.assetid: ab835bf8-1adc-463f-99c3-654a328af98a
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: PdhBrowseCountersH, PdhBrowseCountersH function [Perf], PdhBrowseCountersHA, PdhBrowseCountersHW, _win32_pdhbrowsecountersh, base.pdhbrowsecountersh, pdh/PdhBrowseCountersH, pdh/PdhBrowseCountersHA, pdh/PdhBrowseCountersHW, perf.pdhbrowsecountersh
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PdhBrowseCountersHW (Unicode) and PdhBrowseCountersHA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Pdh.dll
api_name:
 - PdhBrowseCountersH
 - PdhBrowseCountersHA
 - PdhBrowseCountersHW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PdhBrowseCountersHW function


## -description


Displays a <b>Browse Counters</b> dialog box that the user can use to select one or more counters that they want to add to the query. 
			

This function is identical to 
the <a href="https://msdn.microsoft.com/4e9e4b20-a573-4f6d-97e8-63bcc675032b">PdhBrowseCounters</a> function, except that it supports the use of handles to data sources.


## -parameters




### -param pBrowseDlgData [in]

A 
<a href="https://msdn.microsoft.com/db30ff94-3238-45a0-a78e-8b3cd00ec79c">PDH_BROWSE_DLG_CONFIG_H</a> structure that specifies the behavior of the dialog box.


## -returns



If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> or a 
<a href="https://msdn.microsoft.com/ea67d798-81db-44ad-b0fb-24e0c3be7388">PDH error code</a>.




## -remarks



Note that the dialog
   box can return PDH_DIALOG_CANCELLED if <b>bSingleCounterPerDialog</b>is <b>FALSE</b> and the user clicks the <b>Close</b> button, so your error handling would have to account for this.




## -see-also




<a href="https://msdn.microsoft.com/db30ff94-3238-45a0-a78e-8b3cd00ec79c">PDH_BROWSE_DLG_CONFIG_H</a>



<a href="https://msdn.microsoft.com/eaed9b28-eb09-4123-9317-5d3d50e2d77a">PdhBindInputDataSource</a>



<a href="https://msdn.microsoft.com/7e8dc113-76a7-4a7a-bbad-1a4387831501">PdhEnumMachinesH</a>



<a href="https://msdn.microsoft.com/2cea7d0a-cea2-4fee-a087-37663de254e9">PdhEnumObjectItemsH</a>



<a href="https://msdn.microsoft.com/8f68a7a8-cc56-4f7f-a86f-4b439738808d">PdhEnumObjectsH</a>



<a href="https://msdn.microsoft.com/d7d13beb-02ab-4204-808e-d395197f09e1">PdhExpandWildCardPathH</a>



<a href="https://msdn.microsoft.com/55cfef46-999d-43fa-9b09-9d8916fbf755">PdhGetDataSourceTimeRangeH</a>



<a href="https://msdn.microsoft.com/d1b3de9a-99ab-4339-8e9f-906f5a5d291d">PdhGetDefaultPerfCounterH</a>



<a href="https://msdn.microsoft.com/4950d5b7-3a6f-410d-830f-7868aa84f6d5">PdhGetDefaultPerfObjectH</a>



<a href="https://msdn.microsoft.com/068c55da-d7e0-4111-91c8-a2bbd676f99d">PdhOpenQueryH</a>
 

 

