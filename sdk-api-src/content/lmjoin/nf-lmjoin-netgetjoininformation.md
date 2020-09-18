---
UID: NF:lmjoin.NetGetJoinInformation
title: NetGetJoinInformation function (lmjoin.h)
description: The NetGetJoinInformation function retrieves join status information for the specified computer.
helpviewer_keywords: ["NetGetJoinInformation","NetGetJoinInformation function [Network Management]","NetSetupDomainName","NetSetupUnjoined","NetSetupUnknownStatus","NetSetupWorkgroupName","_win32_netgetjoininformation","lmjoin/NetGetJoinInformation","netmgmt.netgetjoininformation"]
old-location: netmgmt\netgetjoininformation.htm
tech.root: NetMgmt
ms.assetid: c7cc1cf2-4530-4039-806b-fbee572f564d
ms.date: 12/05/2018
ms.keywords: NetGetJoinInformation, NetGetJoinInformation function [Network Management], NetSetupDomainName, NetSetupUnjoined, NetSetupUnknownStatus, NetSetupWorkgroupName, _win32_netgetjoininformation, lmjoin/NetGetJoinInformation, netmgmt.netgetjoininformation
req.header: lmjoin.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Netapi32.dll; Wkscli.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetGetJoinInformation
 - lmjoin/NetGetJoinInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
 - wkscli.dll
api_name:
 - NetGetJoinInformation
---

# NetGetJoinInformation function


## -description

The 
				<b>NetGetJoinInformation</b> function retrieves join status information for the specified computer.

## -parameters

### -param lpServer [in]

Pointer to a constant string that specifies the DNS or NetBIOS name of the computer on which to call the function. If this parameter is <b>NULL</b>, the local computer is used.

### -param lpNameBuffer [out]

Pointer to the buffer that receives the NetBIOS name of the domain or workgroup to which the computer is joined. This buffer is allocated by the system and must be freed using the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a> and 
<a href="/windows/desktop/NetMgmt/network-management-function-buffer-lengths">Network Management Function Buffer Lengths</a>.

### -param BufferType [out]

Receives the join status of the specified computer. This parameter can have one of the following values. 





```cpp
typedef enum _NETSETUP_JOIN_STATUS {

    NetSetupUnknownStatus = 0,
    NetSetupUnjoined,
    NetSetupWorkgroupName,
    NetSetupDomainName

} NETSETUP_JOIN_STATUS, *PNETSETUP_JOIN_STATUS;

```


These values have the following meanings.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NetSetupUnknownStatus"></a><a id="netsetupunknownstatus"></a><a id="NETSETUPUNKNOWNSTATUS"></a><dl>
<dt><b>NetSetupUnknownStatus</b></dt>
</dl>
</td>
<td width="60%">
The status is unknown.

</td>
</tr>
<tr>
<td width="40%"><a id="NetSetupUnjoined"></a><a id="netsetupunjoined"></a><a id="NETSETUPUNJOINED"></a><dl>
<dt><b>NetSetupUnjoined</b></dt>
</dl>
</td>
<td width="60%">
The computer is not joined.

</td>
</tr>
<tr>
<td width="40%"><a id="NetSetupWorkgroupName"></a><a id="netsetupworkgroupname"></a><a id="NETSETUPWORKGROUPNAME"></a><dl>
<dt><b>NetSetupWorkgroupName</b></dt>
</dl>
</td>
<td width="60%">
The computer is joined to a workgroup.

</td>
</tr>
<tr>
<td width="40%"><a id="NetSetupDomainName"></a><a id="netsetupdomainname"></a><a id="NETSETUPDOMAINNAME"></a><dl>
<dt><b>NetSetupDomainName</b></dt>
</dl>
</td>
<td width="60%">
The computer is joined to a domain.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is NERR_Success.

If the function fails, the return value can be the following error code or one of the 
<a href="/windows/desktop/Debug/system-error-codes">system error codes</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough storage is available to process this command.

</td>
</tr>
</table>

## -remarks

No special group membership is required to successfully execute the 
<b>NetGetJoinInformation</b> function.

## -see-also

<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netgetjoinableous">NetGetJoinableOUs</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>