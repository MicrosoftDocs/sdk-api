---
UID: NF:lmstats.NetStatisticsGet
title: NetStatisticsGet function
author: windows-sdk-content
description: Retrieves operating statistics for a service. Currently, only the workstation and server services are supported.
old-location: fs\netstatisticsget.htm
tech.root: NetShare
ms.assetid: d0e51d8a-2f54-42ca-9759-0da82c1f0f55
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: 0, NetStatisticsGet, NetStatisticsGet function [Files], _win32_netstatisticsget, fs.netstatisticsget, lmstats/NetStatisticsGet, netmgmt.netstatisticsget
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: lmstats.h
req.include-header: Lm.h
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
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetStatisticsGet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NetStatisticsGet function


## -description


Retrieves operating statistics for a service. Currently, only the workstation and server services are supported.


## -parameters




### -param ServerName [in]

Pointer to a string that specifies the DNS or NetBIOS name of the server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.


### -param Service [in]

Pointer to a string that specifies the name of the service about which to get the statistics. Only the values <b>SERVICE_SERVER</b> and <b>SERVICE_WORKSTATION</b> are currently allowed.


### -param Level [in]

Specifies the information level of the data. This parameter can be the following value. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Return statistics about a workstation or a server. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/7a29fe54-fd15-499d-b255-f49025421861">STAT_WORKSTATION_0</a> or a 
<a href="https://msdn.microsoft.com/7eb4e4a9-f4db-4702-a4ad-2d8bfac9f9ce">STAT_SERVER_0</a> structure.

</td>
</tr>
</table>
 


### -param Options [in]

This parameter must be zero.


### -param Buffer [out]

Pointer to the buffer that receives the data. The format of this data depends on the value of the <i>level</i> parameter. This buffer is allocated by the system and must be freed using the 
<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a> and 
<a href="https://msdn.microsoft.com/08599966-68a1-420b-bbc7-6daac833d08f">Network Management Function Buffer Lengths</a>.


## -returns



If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



No special group membership is required to obtain workstation statistics. Only members of the Administrators or Server Operators local group can successfully execute the 
<b>NetStatisticsGet</b> function on a remote server.




## -see-also




<a href="https://msdn.microsoft.com/ed15e1b5-3fdc-4841-85d1-89269684df0e">NetServerGetInfo</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/7eb4e4a9-f4db-4702-a4ad-2d8bfac9f9ce">STAT_SERVER_0</a>



<a href="https://msdn.microsoft.com/7a29fe54-fd15-499d-b255-f49025421861">STAT_WORKSTATION_0</a>



<a href="https://msdn.microsoft.com/4e0217bf-7550-40a2-b47c-8e898a586005">Statistics
		  Functions</a>
 

 

