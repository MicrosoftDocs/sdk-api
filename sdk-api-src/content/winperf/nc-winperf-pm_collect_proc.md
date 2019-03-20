---
UID: NC:winperf.PM_COLLECT_PROC
title: PM_COLLECT_PROC (winperf.h)
author: windows-sdk-content
description: Collects the performance data and returns it to the consumer.
old-location: perf\collectperformancedata.htm
tech.root: perfctrs
ms.assetid: 9903eb4b-017b-47df-81c5-98c4e1ac697d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CollectPerformanceData, CollectPerformanceData callback function [Perf], PM_COLLECT_PROC, PM_COLLECT_PROC callback, base.collectperformancedata, perf.collectperformancedata, winperf/CollectPerformanceData
ms.topic: callback
req.header: winperf.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winperf.h
api_name:
 - CollectPerformanceData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PM_COLLECT_PROC callback function


## -description


Collects the performance data and returns it to the consumer. Implement and export this function if you are writing a performance DLL to provide performance data. The system calls this function whenever a consumer queries the registry for performance data. 

The <b>CollectPerformanceData</b> function is a placeholder for the application-defined function name.


## -parameters




### -param lpValueName

Null-terminated string that contains the query string (for example, "Global" or "238") passed to the <a href="https://msdn.microsoft.com/202d253a-10ff-40e7-8eec-a49717443b81">RegQueryValueEx</a> function. For possible query string values, see <a href="https://msdn.microsoft.com/feac7b8d-1dee-462c-89dc-bec1ba045da2">Using the Registry Functions to Consume Counter Data</a>.


### -param *lppData


### -param lpcbTotalBytes

On input, specifies the size, in bytes, of the <i>pData</i> buffer. 

On output, set <i>pcbData</i> to the size, in bytes, of the data written to the <i>pData</i> buffer. The size must be 8-byte aligned. 

If this function fails, set <i>pcbData</i> to zero.


### -param lpNumObjectTypes

Number of objects returned in <i>pData</i>. 

If this function fails, set <i>pObjectsReturned</i> to zero.


#### - pData

Consumer-allocated buffer that will contain the performance data. 

On output, set <i>pData</i> to one byte past the end of your data. The data must conform to the 
<a href="https://msdn.microsoft.com/9ed4f890-6256-45fd-a310-b5963a6131ae">PERF_OBJECT_TYPE</a> structure.

If this function fails, leave the <i>pData</i> pointer value unchanged.


## -returns



Return one of the following return values only.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The size of the <i>pData</i> buffer as specified by <i>pcbData</i> is not large enough to store the data. Leave <i>pData</i> unchanged, and set <i>pcbData</i> and <i>pObjectsReturned</i> to zero. No attempt is made to indicate the required buffer size, because this can change before the next call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
Return this value in all cases other than the ERROR_MORE_DATA case, even if no data is returned or an error occurs. To report errors other than insufficient buffer size, use the Application Event Log.

</td>
</tr>
</table>
 




## -remarks



If the requested objects specified in the <i>pQuery</i> parameter do not correspond to any of the object indexes that your performance DLL supports, leave the <i>pData</i> parameter unchanged, and set the <i>pcbData</i> and <i>pObjectsReturned</i> parameters to zero. This indicates that no data is returned. 

If you support one or more of the queried objects, determine whether the size of the <i>pData</i> buffer as specified by <i>pcbData</i> is large enough to store the data. If not, leave <i>pData</i> unchanged, and set <i>pcbData</i> and <i>pObjectsReturned</i> to zero. No attempt is made to indicate the required buffer size, because this may change before the next call. Return ERROR_MORE_DATA.

If your data collection is time-consuming, you should respond only to queries for specific objects and Costly queries. You should also lower the priority of the thread collecting the data, so that it does not adversely affect system performance.

If the consumer is running on another computer (remotely), then the <a href="https://msdn.microsoft.com/06913524-77b7-470b-82d9-8be92fda3109">OpenPerformanceData</a>, <a href="https://msdn.microsoft.com/fb97f68d-4992-4969-9b6b-ace26dcd3155">ClosePerformanceData</a>, and <b>CollectPerformanceData</b> functions are called in the context of the Winlogon process, which handles the server side of the remote connection. This distinction is important when troubleshooting problems that occur only remotely.

After your function returns successfully, the system can perform some basic tests to ensure the integrity of the data. By default, no tests are performed. If a test fails, the system generates an event log message and the data is discarded to prevent any further problems due to pointers that are not valid. The following registry value controls the test level.<pre xml:space="preserve"><b>HKEY_LOCAL_MACHINE</b>
   <b>Software</b>
      <b>Microsoft</b>
         <b>Windows NT</b>
            <b>CurrentVersion</b>
               <b>Perflib</b>
                  <b>ExtCounterTestLevel</b></pre>



				
				The following are the possible test levels for <b>ExtCounterTestLevel</b>. 

<table>
<tr>
<th>Level</th>
<th>Meaning</th>
</tr>
<tr>
<td>1</td>
<td>Test the pointers and buffers of trusted counter DLLs. Sends a copy of the user's buffer.</td>
</tr>
<tr>
<td>2</td>
<td>Test pointers and buffer lengths but does not test pointer references or buffer contents. Sends a copy of the user's buffer.</td>
</tr>
<tr>
<td>3</td>
<td>Do not test pointers or buffers. Sends a copy of the user's buffer.</td>
</tr>
<tr>
<td>4</td>
<td>Do not test pointers or buffers. Sends the user's buffer, not a copy.This is the default value.

</td>
</tr>
</table>
 

The following tests are performed at levels 1 and 2:
				

<ul>
<li>Verifies that the value of <i>pcbData</i> is consistent with the returned buffer pointer, <i>pData</i>. If you add the <i>pcbData</i> value to the original buffer pointer passed to this function, you should end up with the same buffer pointer returned by this function. If they are not the same, a error message is logged and the data is ignored.</li>
<li>Verify that a buffer overrun did not occur. The system adds a 1-KB guard page before and after the consumer-allocated buffer. If the returned buffer pointer, <i>pData</i>, points past the first byte of the appended guard page, then it is assumed that the buffer is not valid and the data is ignored. If the buffer pointer exceeds the end of the buffer, but not the end of the guard page, then a buffer overrun error is logged. If the buffer pointer is past the end of the guard page, then a heap error is logged because the heap that the buffer was allocated from could have been corrupted, causing other memory errors.</li>
<li>Verify that the guard pages have not been corrupted. The 1-KB guard pages that were added before and after the buffer are initialized with a data pattern before this function is called. This data pattern is checked after the collect procedure returns. If any discrepancy is detected, a buffer overrun or other memory error is assumed and the data is ignored.</li>
</ul>

				The following tests are performed only if test level 1 is used:
				

<ul>
<li>Verify that the sum of each object's <b>TotalByteLength</b> member is the same as the value of <i>pcbData</i>. If not, the data is ignored.</li>
<li>Verify that the <b>ByteLength</b> member of each instance is consistent. The lengths are consistent if the next object or end of buffer follows the last instance. If not, the data is ignored.</li>
</ul>

#### Examples

For an example, see <a href="https://msdn.microsoft.com/73b022df-0148-4afc-8536-8b1c766b1ee6">Implementing CollectPerformanceData</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/fb97f68d-4992-4969-9b6b-ace26dcd3155">ClosePerformanceData</a>



<a href="https://msdn.microsoft.com/06913524-77b7-470b-82d9-8be92fda3109">OpenPerformanceData</a>
 

 

