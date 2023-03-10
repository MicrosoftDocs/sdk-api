---
UID: NF:wlanapi.WlanConnect
title: WlanConnect function (wlanapi.h)
description: Attempts to connect to a specific network.
helpviewer_keywords: ["WlanConnect","WlanConnect function [NativeWIFI]","nwifi.wlanconnect","wlanapi/WlanConnect"]
old-location: nwifi\wlanconnect.htm
tech.root: nwifi
ms.assetid: 24ab2024-e786-454f-860f-cf2431f001bb
ms.date: 12/05/2018
ms.keywords: WlanConnect, WlanConnect function [NativeWIFI], nwifi.wlanconnect, wlanapi/WlanConnect
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
 - WlanConnect
 - wlanapi/WlanConnect
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
 - WlanConnect
---

# WlanConnect function


## -description

The <b>WlanConnect</b> function attempts to connect to a specific network.

## -parameters

### -param hClientHandle [in]

The client's session handle, returned by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param pInterfaceGuid [in]

The GUID of the interface to use for the connection.

### -param pConnectionParameters [in]

Pointer to a <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters">WLAN_CONNECTION_PARAMETERS</a> structure that specifies the connection type, mode, network profile, SSID that identifies the network, and other parameters.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>There are some constraints on  the  <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters">WLAN_CONNECTION_PARAMETERS</a> members. This means that structures that are valid for   Windows Server 2008 and Windows Vista may not be valid for Windows XP with SP3 or Wireless LAN API for Windows XP with SP2. For a list of constraints, see <b>WLAN_CONNECTION_PARAMETERS</b>.

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
One of the following conditions occurred:

<ul>
<li><i>hClientHandle</i> is <b>NULL</b> or invalid.</li>
<li><i>pInterfaceGuid</i> is <b>NULL</b>.</li>
<li><i>pConnectionParameters</i> is <b>NULL</b>.</li>
<li>The <b>dwFlags</b> member of the  structure pointed to by <i>pConnectionParameters</i> is not set to one of the values specified on the <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters">WLAN_CONNECTION_PARAMETERS</a> page.</li>
<li>The <b>wlanConnectionMode</b> member of the  structure pointed to by <i>pConnectionParameters</i> is set to <b>wlan_connection_mode_discovery_secure</b> or <b>wlan_connection_mode_discovery_unsecure</b>, and the <b>pDot11Ssid</b> member of the same structure is <b>NULL</b>.</li>
<li>The <b>wlanConnectionMode</b> member of the  structure pointed to by <i>pConnectionParameters</i> is set to <b>wlan_connection_mode_discovery_secure</b> or <b>wlan_connection_mode_discovery_unsecure</b>, and the <b>dot11BssType</b> member of the same structure is set to <b>dot11_BSS_type_any</b>.</li>
<li>The <b>wlanConnectionMode</b> member of the  structure pointed to by <i>pConnectionParameters</i> is set to <b>wlan_connection_mode_profile</b>, and the <b>strProfile</b> member of the same structure is <b>NULL</b> or  the length of the profile exceeds WLAN_MAX_NAME_LENGTH.</li>
<li>The <b>wlanConnectionMode</b> member of the  structure pointed to by <i>pConnectionParameters</i> is set to <b>wlan_connection_mode_profile</b>, and the <b>strProfile</b> member of the same structure is <b>NULL</b> or  the length of the profile is zero.</li>
<li>The <b>wlanConnectionMode</b> member of the  structure pointed to by <i>pConnectionParameters</i> is set to <b>wlan_connection_mode_invalid</b> or <b>wlan_connection_mode_auto</b>.</li>
<li>The <b>dot11BssType</b> member of the  structure pointed to by <i>pConnectionParameters</i> is set to <b>dot11_BSS_type_infrastructure</b>, and the <b>dwFlags</b> member of the same structure is set to <b>WLAN_CONNECTION_ADHOC_JOIN_ONLY</b>.</li>
<li>The <b>dot11BssType</b> member of the  structure pointed to by <i>pConnectionParameters</i> is set to <b>dot11_BSS_type_independent</b>, and the <b>dwFlags</b> member of the same structure is set to <b>WLAN_CONNECTION_HIDDEN_NETWORK</b>.</li>
<li>The <b>dwFlags</b> member of the  structure pointed to by <i>pConnectionParameters</i> is set to <b>WLAN_CONNECTION_IGNORE_PRIVACY_BIT</b>, and either the <b>wlanConnectionMode</b> member of the same structure is not set to <b>wlan_connection_mode_temporary_profile</b> or the <b>dot11BssType</b> member of the same structure is set to <b>dot11_BSS_type_independent</b>.</li>
</ul>
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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient permissions. 

</td>
</tr>
</table>

## -remarks

The <b>WlanConnect</b> function returns immediately.  To be notified when a connection is established or when no further connections will be attempted, a client must register for notifications by calling <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification">WlanRegisterNotification</a>.

The <b>strProfile</b> member of the <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters">WLAN_CONNECTION_PARAMETERS</a> structure pointed to by <i>pConnectionParameters</i> specifies the profile to use for connection. If this profile is an all-user profile, the <b>WlanConnect</b>  caller must have execute access on the profile. Otherwise, the <b>WlanConnect</b> call will fail with return value ERROR_ACCESS_DENIED. The permissions on an all-user profile are established when the profile is created or saved using <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile">WlanSetProfile</a> or <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansavetemporaryprofile">WlanSaveTemporaryProfile</a>.

To perform a connection operation at the command line, use the <b>netsh wlan connect</b> command. For more information, see <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)">Netsh Commands for Wireless Local Area Network (wlan)</a>. 

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>You can only use <b>WlanConnect</b> to connect to networks on the preferred network list. To add a network to the preferred network list, call <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile">WlanSetProfile</a>.

## -see-also

<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters">WLAN_CONNECTION_PARAMETERS</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect">WlanDisconnect</a>