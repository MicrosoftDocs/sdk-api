---
UID: NF:pdh.PdhGetRawCounterValue
title: PdhGetRawCounterValue function (pdh.h)
author: windows-sdk-content
description: Returns the current raw value of the counter.
old-location: perf\pdhgetrawcountervalue.htm
tech.root: perfctrs
ms.assetid: bb246c82-8748-4e2f-9f44-a206199aff90
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PdhGetRawCounterValue, PdhGetRawCounterValue function [Perf], _win32_pdhgetrawcountervalue, base.pdhgetrawcountervalue, pdh/PdhGetRawCounterValue, perf.pdhgetrawcountervalue
ms.topic: function
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - PdhGetRawCounterValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PdhGetRawCounterValue function


## -description


Returns the current raw value of the counter.
		


## -parameters




### -param hCounter [in]

Handle of the counter from which to retrieve the current raw value. The 
<a href="https://msdn.microsoft.com/b8b9a332-ce28-46d4-92e2-91f9f6c24da5">PdhAddCounter</a> function returns this handle.


### -param lpdwType [out]

Receives the counter type. For a list of counter types, see the Counter Types section of the <a href="Http://go.microsoft.com/fwlink/p/?linkid=84422">Windows Server 2003 Deployment Kit</a>. This parameter is optional.


### -param pValue [out]

A 
<a href="https://msdn.microsoft.com/237a3c82-0ab4-45cb-bd93-2f308178c573">PDH_RAW_COUNTER</a> structure that receives the counter value.


## -returns



If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> or a 
<a href="https://msdn.microsoft.com/ea67d798-81db-44ad-b0fb-24e0c3be7388">PDH error code</a>. The following are possible values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_ARGUMENT</b></dt>
</dl>
</td>
<td width="60%">
A parameter is not valid or is incorrectly formatted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The counter handle is not valid.

</td>
</tr>
</table>
 




## -remarks



The data for the counter is locked (protected) for the duration of the call to 
<b>PdhGetRawCounterValue</b> to prevent any changes during processing of the call.

If 
the specified counter instance does not exist, this function will return ERROR_SUCCESS and the <b>CStatus</b> member of the 
<a href="https://msdn.microsoft.com/237a3c82-0ab4-45cb-bd93-2f308178c573">PDH_RAW_COUNTER</a> structure will contain PDH_CSTATUS_NO_INSTANCE.




## -see-also




<a href="https://msdn.microsoft.com/fd50b1fd-29b7-49a8-bbcc-4d7f0cbd7079">PdhCalculateCounterFromRawValue</a>



<a href="https://msdn.microsoft.com/1d83325b-8deb-4731-9df4-6201da292cdc">PdhCollectQueryData</a>



<a href="https://msdn.microsoft.com/cd104b26-1498-4f95-a411-97d868b43836">PdhGetFormattedCounterValue</a>
 

 

