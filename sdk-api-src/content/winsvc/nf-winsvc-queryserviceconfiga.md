---
UID: NF:winsvc.QueryServiceConfigA
title: QueryServiceConfigA function
author: windows-sdk-content
description: Retrieves the configuration parameters of the specified service.
old-location: base\queryserviceconfig.htm
tech.root: services
ms.assetid: 364c5f61-dfbe-460b-8e42-5c457b65c050
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: QueryServiceConfig, QueryServiceConfig function, QueryServiceConfigA, QueryServiceConfigW, _win32_queryserviceconfig, base.queryserviceconfig, winsvc/QueryServiceConfig, winsvc/QueryServiceConfigA, winsvc/QueryServiceConfigW
ms.topic: function
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: QueryServiceConfigW (Unicode) and QueryServiceConfigA (ANSI)
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
 - API-MS-Win-DownLevel-AdvApi32-l2-1-0.dll
 - sechost.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - API-MS-Win-Service-management-l2-1-0.dll
 - API-MS-Win-Service-Winsvc-l1-1-0.dll
 - API-MS-Win-Service-Winsvc-l1-2-0.dll
api_name:
 - QueryServiceConfig
 - QueryServiceConfigA
 - QueryServiceConfigW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# QueryServiceConfigA function


## -description


Retrieves the configuration parameters of the specified service. Optional configuration parameters are available using the 
<a href="https://msdn.microsoft.com/cb090e59-aeff-4420-bb7c-912a4911006f">QueryServiceConfig2</a> function.


## -parameters




### -param hService [in]

A handle to the service. This handle is returned by the 
<a href="https://msdn.microsoft.com/e0a42613-95ad-4d0f-a464-c6df33014064">OpenService</a> or 
<a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a> function, and it must have the SERVICE_QUERY_CONFIG access right. For more information, see 
<a href="https://msdn.microsoft.com/23d1c382-6ba4-49e2-8039-c2a91471076c">Service Security and Access Rights</a>.


### -param lpServiceConfig [out, optional]

A pointer to a buffer that receives the service configuration information. The format of the data is a 
<a href="https://msdn.microsoft.com/069c1431-a04b-4e96-953b-14c5c0700857">QUERY_SERVICE_CONFIG</a> structure.

The maximum size of this array is 8K bytes. To determine the required size, specify NULL for this parameter and 0 for the <i>cbBufSize</i> parameter. The function will fail and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> will return ERROR_INSUFFICIENT_BUFFER. The <i>pcbBytesNeeded</i> parameter will receive the required size.


### -param cbBufSize [in]

The size of the buffer pointed to by the <i>lpServiceConfig</i> parameter, in bytes.


### -param pcbBytesNeeded [out]

A pointer to a variable that receives the number of bytes needed to store all the configuration information, if the function fails with ERROR_INSUFFICIENT_BUFFER.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following error codes can be set by the service control manager. Others can be set by the registry functions that are called by the service control manager.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The handle does not have the SERVICE_QUERY_CONFIG access right.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
There is more service configuration information than would fit into the <i>lpServiceConfig</i> buffer. The number of bytes required to get all the information is returned in the <i>pcbBytesNeeded</i> parameter. Nothing is written to <i>lpServiceConfig</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified handle is invalid.

</td>
</tr>
</table>
 




## -remarks



The 
<b>QueryServiceConfig</b> function returns the service configuration information kept in the registry for a particular service. This configuration information is first set by a service control program using the 
<a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a> function. This information may have been updated by a service configuration program using the 
<a href="https://msdn.microsoft.com/add8a99b-aced-4341-9790-86efac76df6b">ChangeServiceConfig</a> function.

If the service was running when the configuration information was last changed, the information returned by 
<b>QueryServiceConfig</b> will not reflect the current configuration of the service. Instead, it will reflect the configuration of the service when it is next run. The <b>DisplayName</b> key is an exception to this. When the <b>DisplayName</b> key is changed, it takes effect immediately, regardless of whether the service is running.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/e6633dc9-c9b6-457d-8adc-e751ec9cf71d">Querying a Service's Configuration</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/add8a99b-aced-4341-9790-86efac76df6b">ChangeServiceConfig</a>



<a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a>



<a href="https://msdn.microsoft.com/e0a42613-95ad-4d0f-a464-c6df33014064">OpenService</a>



<a href="https://msdn.microsoft.com/069c1431-a04b-4e96-953b-14c5c0700857">QUERY_SERVICE_CONFIG</a>



<a href="https://msdn.microsoft.com/cb090e59-aeff-4420-bb7c-912a4911006f">QueryServiceConfig2</a>



<a href="https://msdn.microsoft.com/499b63fd-e77b-4b90-9ee7-ff4b7b12c431">QueryServiceDynamicInformation</a>



<a href="https://msdn.microsoft.com/5d95945f-f11b-42af-b302-8d924917b9ab">QueryServiceObjectSecurity</a>



<a href="https://msdn.microsoft.com/fc8c631e-076c-4745-8db0-90f46a202e6a">Service Configuration</a>



<a href="https://msdn.microsoft.com/63666848-cbac-4853-8b91-89303f9854c0">Service Functions</a>
 

 

