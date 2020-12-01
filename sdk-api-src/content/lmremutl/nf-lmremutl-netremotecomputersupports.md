---
UID: NF:lmremutl.NetRemoteComputerSupports
title: NetRemoteComputerSupports function (lmremutl.h)
description: The NetRemoteComputerSupports function queries the redirector to retrieve the optional features the remote system supports.
helpviewer_keywords: ["NetRemoteComputerSupports","NetRemoteComputerSupports function [Network Management]","SUPPORTS_LOCAL","SUPPORTS_REMOTE_ADMIN_PROTOCOL","SUPPORTS_RPC","SUPPORTS_SAM_PROTOCOL","SUPPORTS_UNICODE","_win32_netremotecomputersupports","lmremutl/NetRemoteComputerSupports","netmgmt.netremotecomputersupports"]
old-location: netmgmt\netremotecomputersupports.htm
tech.root: NetMgmt
ms.assetid: e807489a-250e-4d4c-adb6-eff8ac30603b
ms.date: 12/05/2018
ms.keywords: NetRemoteComputerSupports, NetRemoteComputerSupports function [Network Management], SUPPORTS_LOCAL, SUPPORTS_REMOTE_ADMIN_PROTOCOL, SUPPORTS_RPC, SUPPORTS_SAM_PROTOCOL, SUPPORTS_UNICODE, _win32_netremotecomputersupports, lmremutl/NetRemoteComputerSupports, netmgmt.netremotecomputersupports
req.header: lmremutl.h
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
 - NetRemoteComputerSupports
 - lmremutl/NetRemoteComputerSupports
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
 - NetRemoteComputerSupports
---

# NetRemoteComputerSupports function


## -description

The 
				<b>NetRemoteComputerSupports</b> function queries the redirector to retrieve the optional features the remote system supports. Features include Unicode, Remote Procedure Call (RPC), and Remote Administration Protocol support. The function establishes a network connection if one does not exist.

## -parameters

### -param UncServerName [in]

Pointer to a constant string that specifies the name of the remote server to query. If this parameter is <b>NULL</b>, the local computer is used.

### -param OptionsWanted [in]

Specifies a value that contains a set of bit flags indicating the features of interest. This parameter must be at least one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SUPPORTS_REMOTE_ADMIN_PROTOCOL"></a><a id="supports_remote_admin_protocol"></a><dl>
<dt><b>SUPPORTS_REMOTE_ADMIN_PROTOCOL</b></dt>
</dl>
</td>
<td width="60%">
Requests Remote Administration Protocol support.

</td>
</tr>
<tr>
<td width="40%"><a id="SUPPORTS_RPC"></a><a id="supports_rpc"></a><dl>
<dt><b>SUPPORTS_RPC</b></dt>
</dl>
</td>
<td width="60%">
Requests RPC support.

</td>
</tr>
<tr>
<td width="40%"><a id="SUPPORTS_SAM_PROTOCOL"></a><a id="supports_sam_protocol"></a><dl>
<dt><b>SUPPORTS_SAM_PROTOCOL</b></dt>
</dl>
</td>
<td width="60%">
Requests Security Account Manager (SAM) support.

</td>
</tr>
<tr>
<td width="40%"><a id="SUPPORTS_UNICODE"></a><a id="supports_unicode"></a><dl>
<dt><b>SUPPORTS_UNICODE</b></dt>
</dl>
</td>
<td width="60%">
Requests Unicode standard support.

</td>
</tr>
<tr>
<td width="40%"><a id="SUPPORTS_LOCAL"></a><a id="supports_local"></a><dl>
<dt><b>SUPPORTS_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
Requests support for the first three values listed in this table. If UNICODE is defined by the calling application, requests the four features listed previously.

</td>
</tr>
</table>

### -param OptionsSupported [out]

Pointer to a value that receives a set of bit flags. The flags indicate which features specified by the <i>OptionsWanted</i> parameter are implemented on the computer specified by the <i>UncServerName</i> parameter. (All other bits are set to zero.) 




The value of this parameter is valid only when the 
<b>NetRemoteComputerSupports</b> function returns NERR_Success.

## -returns

If the function succeeds, the return value is NERR_Success.

If the function fails, the return value can be one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Either the <i>OptionsWanted</i> parameter or the <i>OptionsSupported</i> parameter is <b>NULL</b>; both parameters are required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory is available.

</td>
</tr>
</table>

## -remarks

No special group membership is required to successfully execute the 
<b>NetRemoteComputerSupports</b> function.

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo">NetServerGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/NetMgmt/remote-utility-functions">Remote
		  Utility Functions</a>