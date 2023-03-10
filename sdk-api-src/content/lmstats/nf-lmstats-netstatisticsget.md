---
UID: NF:lmstats.NetStatisticsGet
title: NetStatisticsGet function (lmstats.h)
description: Retrieves operating statistics for a service. Currently, only the workstation and server services are supported.
helpviewer_keywords: ["0","NetStatisticsGet","NetStatisticsGet function [Files]","_win32_netstatisticsget","fs.netstatisticsget","lmstats/NetStatisticsGet","netmgmt.netstatisticsget"]
old-location: fs\netstatisticsget.htm
tech.root: fs
ms.assetid: d0e51d8a-2f54-42ca-9759-0da82c1f0f55
ms.date: 12/05/2018
ms.keywords: 0, NetStatisticsGet, NetStatisticsGet function [Files], _win32_netstatisticsget, fs.netstatisticsget, lmstats/NetStatisticsGet, netmgmt.netstatisticsget
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetStatisticsGet
 - lmstats/NetStatisticsGet
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetStatisticsGet
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
<a href="/windows/win32/api/lmstats/ns-lmstats-stat_workstation_0~r1">STAT_WORKSTATION_0</a> or a 
<a href="/windows/desktop/api/lmstats/ns-lmstats-stat_server_0">STAT_SERVER_0</a> structure.

</td>
</tr>
</table>

### -param Options [in]

This parameter must be zero.

### -param Buffer [out]

Pointer to the buffer that receives the data. The format of this data depends on the value of the <i>level</i> parameter. This buffer is allocated by the system and must be freed using the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a> and 
<a href="/windows/desktop/NetMgmt/network-management-function-buffer-lengths">Network Management Function Buffer Lengths</a>.

## -returns

If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

No special group membership is required to obtain workstation statistics. Only members of the Administrators or Server Operators local group can successfully execute the 
<b>NetStatisticsGet</b> function on a remote server.

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo">NetServerGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/api/lmstats/ns-lmstats-stat_server_0">STAT_SERVER_0</a>



<a href="/windows/win32/api/lmstats/ns-lmstats-stat_workstation_0~r1">STAT_WORKSTATION_0</a>



<a href="/windows/desktop/NetShare/statistics-functions">Statistics
		  Functions</a>