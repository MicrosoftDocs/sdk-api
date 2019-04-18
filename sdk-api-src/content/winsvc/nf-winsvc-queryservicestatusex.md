---
UID: NF:winsvc.QueryServiceStatusEx
title: QueryServiceStatusEx function (winsvc.h)
author: windows-sdk-content
description: Retrieves the current status of the specified service based on the specified information level.
old-location: base\queryservicestatusex.htm
tech.root: Services
ms.assetid: 3fe02245-97b1-49f3-8f35-2dcd6f221547
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: QueryServiceStatusEx, QueryServiceStatusEx function, _win32_queryservicestatusex, base.queryservicestatusex, winsvc/QueryServiceStatusEx
ms.topic: function
req.header: winsvc.h
req.include-header: Windows.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - sechost.dll
 - API-MS-Win-Service-management-l2-1-0.dll
api_name:
 - QueryServiceStatusEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# QueryServiceStatusEx function


## -description


Retrieves the current status of the specified service based on the specified information level.


## -parameters




### -param hService [in]

A handle to the service. This handle is returned by the 
<a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a> or 
<a href="https://msdn.microsoft.com/e0a42613-95ad-4d0f-a464-c6df33014064">OpenService</a> function, and it must have the SERVICE_QUERY_STATUS access right. For more information, see 
<a href="https://msdn.microsoft.com/23d1c382-6ba4-49e2-8039-c2a91471076c">Service Security and Access Rights</a>.


### -param InfoLevel [in]

The service attributes to be returned. Use SC_STATUS_PROCESS_INFO to retrieve the service status information. The <i>lpBuffer</i> parameter is a pointer to a 
<a href="https://msdn.microsoft.com/303986a0-c51e-4078-a3ca-d59e5a302b36">SERVICE_STATUS_PROCESS</a> structure. 




Currently, no other information levels are defined.


### -param lpBuffer [out, optional]

A pointer to the buffer that receives the status information. The format of this data depends on the value of the <i>InfoLevel</i> parameter.

The maximum size of this array is 8K bytes. To determine the required size, specify NULL for this parameter and 0 for the <i>cbBufSize</i> parameter. The function will fail and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> will return ERROR_INSUFFICIENT_BUFFER. The <i>pcbBytesNeeded</i> parameter will receive the required size.


### -param cbBufSize [in]

The size of the buffer pointed to by the <i>lpBuffer</i> parameter, in bytes.


### -param pcbBytesNeeded [out]

A pointer to a variable that receives the number of bytes needed to store all status information, if the function fails with ERROR_INSUFFICIENT_BUFFER.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The following errors can be returned.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The handle does not have the SERVICE_QUERY_STATUS access right.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer is too small for the 
<a href="https://msdn.microsoft.com/303986a0-c51e-4078-a3ca-d59e5a302b36">SERVICE_STATUS_PROCESS</a> structure. Nothing was written to the structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <b>cbSize</b> member of 
<a href="https://msdn.microsoft.com/303986a0-c51e-4078-a3ca-d59e5a302b36">SERVICE_STATUS_PROCESS</a> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
The <i>InfoLevel</i> parameter contains an unsupported value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SHUTDOWN_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
The system is shutting down; this function cannot be called.

</td>
</tr>
</table>
 




## -remarks



The 
<b>QueryServiceStatusEx</b> function returns the most recent service status information reported to the service control manager. If the service just changed its status, it may not have updated the service control manager yet.

The process identifier returned in the <a href="https://msdn.microsoft.com/303986a0-c51e-4078-a3ca-d59e5a302b36">SERVICE_STATUS_PROCESS</a> structure is valid provided that the state of the service is one of SERVICE_RUNNING, SERVICE_PAUSE_PENDING, SERVICE_PAUSED, or SERVICE_CONTINUE_PENDING. If the service is in a SERVICE_START_PENDING or SERVICE_STOP_PENDING state, however, the process identifier may not be valid, and if the service is in the SERVICE_STOPPED state, it is never valid.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/7ee5254d-b035-4888-88e9-93e3e55d737e">Starting a Service</a> or <a href="https://msdn.microsoft.com/fe16d2a8-3e66-49cc-b9c7-fffbc206e8d3">Stopping a Service</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/303986a0-c51e-4078-a3ca-d59e5a302b36">SERVICE_STATUS_PROCESS</a>



<a href="https://msdn.microsoft.com/63666848-cbac-4853-8b91-89303f9854c0">Service Functions</a>



<a href="https://msdn.microsoft.com/7d2ee779-1554-436a-a65c-f0322745f46a">Service Startup</a>
 

 

