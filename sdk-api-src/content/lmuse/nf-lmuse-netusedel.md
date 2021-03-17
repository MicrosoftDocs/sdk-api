---
UID: NF:lmuse.NetUseDel
title: NetUseDel function (lmuse.h)
description: The NetUseDel function ends a connection to a shared resource.
helpviewer_keywords: ["NetUseDel","NetUseDel function [Network Management]","USE_FORCE","USE_LOTS_OF_FORCE","USE_NOFORCE","_win32_netusedel","lmuse/NetUseDel","netmgmt.netusedel"]
old-location: netmgmt\netusedel.htm
tech.root: NetMgmt
ms.assetid: 200b0640-71e9-4f60-bf4c-c8df10bfe095
ms.date: 12/05/2018
ms.keywords: NetUseDel, NetUseDel function [Network Management], USE_FORCE, USE_LOTS_OF_FORCE, USE_NOFORCE, _win32_netusedel, lmuse/NetUseDel, netmgmt.netusedel
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
 - NetUseDel
 - lmuse/NetUseDel
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
 - NetUseDel
---

# NetUseDel function


## -description

The
				<b>NetUseDel</b> function ends a connection to a shared resource.

You can also use the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a">WNetCancelConnection2</a> function to terminate a network connection.

## -parameters

### -param UncServerName [in]

The UNC name of the computer on which to execute this function. If this is parameter is <b>NULL</b>, then the local computer is used. 

If the <i>UncServerName</i> parameter specified is a remote computer, then the remote computer must support remote RPC calls using the legacy Remote Access Protocol mechanism. 

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.

### -param UseName [in]

A pointer to a string that specifies the path of the connection to delete.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.

### -param ForceLevelFlags [in]

The level of force to use in deleting the connection.

 This parameter can be one of the following values defined in the <i>lmuseflg.h</i> header file. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="USE_NOFORCE"></a><a id="use_noforce"></a><dl>
<dt><b>USE_NOFORCE</b></dt>
</dl>
</td>
<td width="60%">
Fail the disconnection if open files exist on the connection.

</td>
</tr>
<tr>
<td width="40%"><a id="USE_FORCE"></a><a id="use_force"></a><dl>
<dt><b>USE_FORCE</b></dt>
</dl>
</td>
<td width="60%">
Do not fail the disconnection if open files exist on the connection.

</td>
</tr>
<tr>
<td width="40%"><a id="USE_LOTS_OF_FORCE"></a><a id="use_lots_of_force"></a><dl>
<dt><b>USE_LOTS_OF_FORCE</b></dt>
</dl>
</td>
<td width="60%">
Close any open files and delete the connection.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

The <b>NetUseDel</b> function applies only to the Server Message Block (LAN Manager Workstation) client. The <b>NetUseDel</b> function does not support Distributed File System (DFS) shares or other network file systems. To terminate a connection to a share using a different network provider (WebDAV or a DFS share, for example), use the <a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a">WNetCancelConnection2</a> function.


No special group membership is required to call the 
<b>NetUseDel</b> function. This function cannot be executed on a remote server except in cases of downlevel compatibility.

## -see-also

<a href="/windows/desktop/api/lmuse/nf-lmuse-netuseadd">NetUseAdd</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/NetMgmt/use-functions">Use Functions</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a">WNetCancelConnection2</a>