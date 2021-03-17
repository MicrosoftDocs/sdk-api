---
UID: NF:lmuse.NetUseGetInfo
title: NetUseGetInfo function (lmuse.h)
description: The NetUseGetInfo function retrieves information about a connection to a shared resource.
helpviewer_keywords: ["NetUseGetInfo","NetUseGetInfo function [Network Management]","_win32_netusegetinfo","lmuse/NetUseGetInfo","netmgmt.netusegetinfo"]
old-location: netmgmt\netusegetinfo.htm
tech.root: NetMgmt
ms.assetid: 257875db-5ed9-4569-8dbb-5dcc7a6af95c
ms.date: 12/05/2018
ms.keywords: NetUseGetInfo, NetUseGetInfo function [Network Management], _win32_netusegetinfo, lmuse/NetUseGetInfo, netmgmt.netusegetinfo
req.header: lmuse.h
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
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetUseGetInfo
 - lmuse/NetUseGetInfo
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
 - NetUseGetInfo
---

# NetUseGetInfo function


## -description

The
				<b>NetUseGetInfo</b> function retrieves information about a connection to a shared resource.

You can also use the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetconnectiona">WNetGetConnection</a> function to retrieve the name of a network resource associated with a local device.

## -parameters

### -param UncServerName [in]

The UNC name of computer on which to execute this function. If this is parameter is <b>NULL</b>, then the local computer is used. If the <i>UncServerName</i> parameter specified is a remote computer, then the remote computer must support remote RPC calls using the legacy Remote Access Protocol mechanism. 

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.

### -param UseName [in]

A pointer to a string that specifies the name of the connection for which to return information.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.

### -param LevelFlags [in]

The information level of the data requested. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Specifies a local device name and the share name of a remote resource. The <i>BufPtr</i>  parameter is a pointer to a 
<a href="/windows/desktop/api/lmuse/ns-lmuse-use_info_0">USE_INFO_0</a> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Specifies information about the connection between a local device and a shared resource, including connection status and type. The <i>BufPtr</i> parameter is a pointer to a 
<a href="/windows/desktop/api/lmuse/ns-lmuse-use_info_1">USE_INFO_1</a> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Specifies information about the connection between a local device and a shared resource. Information includes the connection status, connection type, user name, and domain name. The <i>BufPtr</i> parameter is a pointer to a 
<a href="/windows/desktop/api/lmuse/ns-lmuse-use_info_2">USE_INFO_2</a> structure.

</td>
</tr>
</table>

### -param bufptr [out]

A pointer to the buffer that receives the data. The format of this data depends on the value of the <i>Level</i> parameter. This buffer is allocated by the system and must be freed using the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a> and 
<a href="/windows/desktop/NetMgmt/network-management-function-buffer-lengths">Network Management Function Buffer Lengths</a>.

## -returns

If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

No special group membership is required to call the 
<b>NetUseGetInfo</b> function. This function cannot be executed on a remote server except in cases of downlevel compatibility.

To list all current connections between the local computer and resources on remote servers, you can call the 
<a href="/windows/desktop/api/lmuse/nf-lmuse-netuseenum">NetUseEnum</a> function.

This function applies only to the Server Message Block (LAN Manager Workstation) client. The <b>NetUseGetInfo</b> function does not support Distributed File System (DFS) shares. To retrieve information for a share using a different network provider (WebDAV or a DFS share, for example), use the <a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetconnectiona">WNetGetConnection</a> function.

## -see-also

<a href="/windows/desktop/api/lmuse/nf-lmuse-netuseenum">NetUseEnum</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/api/lmuse/ns-lmuse-use_info_0">USE_INFO_0</a>



<a href="/windows/desktop/api/lmuse/ns-lmuse-use_info_1">USE_INFO_1</a>



<a href="/windows/desktop/api/lmuse/ns-lmuse-use_info_2">USE_INFO_2</a>



<a href="/windows/desktop/NetMgmt/use-functions">Use Functions</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetconnectiona">WNetGetConnection</a>