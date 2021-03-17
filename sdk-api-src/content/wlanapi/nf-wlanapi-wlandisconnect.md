---
UID: NF:wlanapi.WlanDisconnect
title: WlanDisconnect function (wlanapi.h)
description: Disconnects an interface from its current network.
helpviewer_keywords: ["WlanDisconnect","WlanDisconnect function [NativeWIFI]","nwifi.wlandisconnect","wlanapi/WlanDisconnect"]
old-location: nwifi\wlandisconnect.htm
tech.root: nwifi
ms.assetid: cc48ee72-3125-45a0-ac16-0c520ee3cd44
ms.date: 12/05/2018
ms.keywords: WlanDisconnect, WlanDisconnect function [NativeWIFI], nwifi.wlandisconnect, wlanapi/WlanDisconnect
req.header: wlanapi.h
req.include-header: Wlanapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wlanapi.lib
req.dll: Wlanapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Wireless LAN API for Windows XP with SP2
ms.custom: 19H1
f1_keywords:
 - WlanDisconnect
 - wlanapi/WlanDisconnect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - wlanapi.dll
api_name:
 - WlanDisconnect
---

# WlanDisconnect function


## -description

The <b>WlanDisconnect</b> function  disconnects an interface from its current network.

## -parameters

### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param pInterfaceGuid [in]

The GUID of the interface to be disconnected.

### -param pReserved

Reserved for future use.  Must be set to <b>NULL</b>.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value may be one of the following return codes.

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
<i>hClientHandle</i> is <b>NULL</b> or invalid,  <i>pInterfaceGuid</i> is <b>NULL</b>, or <i>pReserved</i> is not <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle <i>hClientHandle</i>  was not found in the handle table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_STATUS</b></dt>
</dl>
</td>
<td width="60%">
Various error codes.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate memory for the query results.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient permissions. 

</td>
</tr>
</table>

## -remarks

When the connection was established using <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect">WlanConnect</a>, a profile was specified by the <b>strProfile</b> member of the <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters">WLAN_CONNECTION_PARAMETERS</a> structure pointed to by  <i>pConnectionParameters</i>. If that profile was an all-user profile, the <b>WlanDisconnect</b>  caller must have execute access on the profile. Otherwise, the <b>WlanDisconnect</b> call will fail with return value ERROR_ACCESS_DENIED. The permissions on an all-user profile are established when the profile is created or saved using <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile">WlanSetProfile</a> or <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansavetemporaryprofile">WlanSaveTemporaryProfile</a>.

To perform a disconnection operation at the command line, use the <b>netsh wlan disconnect</b> command. For more information, see <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)">Netsh Commands for Wireless Local Area Network (wlan)</a>. 

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b><b>WlanDisconnect</b> has the side effect of modifying the profile associated with the disconnected network. A network profile becomes an on-demand profile after a <b>WlanDisconnect</b> call. The Wireless Zero Configuration service will not connect automatically to a network with an on-demand profile when the network is in range. Do not call <b>WlanDisconnect</b> before calling <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect">WlanConnect</a> unless you want to change a profile to an on-demand profile. When you call <b>WlanConnect</b> to establish a network connection, any existing network connection is dropped automatically.

## -see-also

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect">WlanConnect</a>