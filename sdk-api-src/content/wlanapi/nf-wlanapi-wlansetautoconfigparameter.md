---
UID: NF:wlanapi.WlanSetAutoConfigParameter
title: WlanSetAutoConfigParameter function (wlanapi.h)
description: Sets parameters for the automatic configuration service.
helpviewer_keywords: ["WlanSetAutoConfigParameter","WlanSetAutoConfigParameter function [NativeWIFI]","nwifi.wlansetautoconfigparameter","wlan_autoconf_opcode_allow_explicit_creds","wlan_autoconf_opcode_allow_virtual_station_extensibility","wlan_autoconf_opcode_block_period","wlan_autoconf_opcode_show_denied_networks","wlanapi/WlanSetAutoConfigParameter"]
old-location: nwifi\wlansetautoconfigparameter.htm
tech.root: nwifi
ms.assetid: 4f2514be-f05e-4be6-8c74-ef7a9ffe1c53
ms.date: 12/05/2018
ms.keywords: WlanSetAutoConfigParameter, WlanSetAutoConfigParameter function [NativeWIFI], nwifi.wlansetautoconfigparameter, wlan_autoconf_opcode_allow_explicit_creds, wlan_autoconf_opcode_allow_virtual_station_extensibility, wlan_autoconf_opcode_block_period, wlan_autoconf_opcode_show_denied_networks, wlanapi/WlanSetAutoConfigParameter
req.header: wlanapi.h
req.include-header: Wlanapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WlanSetAutoConfigParameter
 - wlanapi/WlanSetAutoConfigParameter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wlanapi.dll
api_name:
 - WlanSetAutoConfigParameter
---

# WlanSetAutoConfigParameter function


## -description

The <b>WlanSetAutoConfigParameter</b> function sets parameters for the automatic configuration service.

## -parameters

### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param OpCode [in]

A <a href="/windows/win32/api/wlanapi/ne-wlanapi-wlan_autoconf_opcode-r1">WLAN_AUTOCONF_OPCODE</a> value that specifies the parameter to be set. Only some of the opcodes in the <b>WLAN_AUTOCONF_OPCODE</b> enumeration support set operations.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="wlan_autoconf_opcode_show_denied_networks"></a><a id="WLAN_AUTOCONF_OPCODE_SHOW_DENIED_NETWORKS"></a><dl>
<dt><b>wlan_autoconf_opcode_show_denied_networks</b></dt>
</dl>
</td>
<td width="60%">
When set, the <i>pData</i> parameter will contain a <b>BOOL</b> value indicating whether user and group policy-denied networks will be included in the available networks list. 

</td>
</tr>
<tr>
<td width="40%"><a id="wlan_autoconf_opcode_allow_explicit_creds"></a><a id="WLAN_AUTOCONF_OPCODE_ALLOW_EXPLICIT_CREDS"></a><dl>
<dt><b>wlan_autoconf_opcode_allow_explicit_creds</b></dt>
</dl>
</td>
<td width="60%">
When set, the <i>pData</i> parameter will contain a <b>BOOL</b> value indicating whether the current wireless interface has shared user credentials allowed.

</td>
</tr>
<tr>
<td width="40%"><a id="wlan_autoconf_opcode_block_period"></a><a id="WLAN_AUTOCONF_OPCODE_BLOCK_PERIOD"></a><dl>
<dt><b>wlan_autoconf_opcode_block_period</b></dt>
</dl>
</td>
<td width="60%">
When set, the <i>pData</i> parameter will contain a <b>DWORD</b> value for the blocked period setting for the current wireless interface. The blocked period is the amount of time, in seconds, for which automatic connection to a wireless network will not be attempted after a previous failure.

</td>
</tr>
<tr>
<td width="40%"><a id="wlan_autoconf_opcode_allow_virtual_station_extensibility"></a><a id="WLAN_AUTOCONF_OPCODE_ALLOW_VIRTUAL_STATION_EXTENSIBILITY"></a><dl>
<dt><b>wlan_autoconf_opcode_allow_virtual_station_extensibility</b></dt>
</dl>
</td>
<td width="60%">
When set, the <i>pData</i> parameter will contain a <b>BOOL</b> value indicating whether extensibility on a virtual station is allowed. By default, extensibility on a virtual station is allowed. The value for this opcode is persisted across restarts.

This enumeration value is supported on Windows 7 and on Windows Server 2008 R2 with the Wireless LAN Service installed.

</td>
</tr>
</table>

### -param dwDataSize [in]

The size of the <i>pData</i> parameter, in bytes. This parameter must be set to <code>sizeof(BOOL)</code> for a BOOL or <code>sizeof(DWORD)</code> for a DWORD, depending on the value of the <i>OpCode</i> parameter.

### -param pData [in]

The value to be set for the parameter specified in <i>OpCode</i> parameter. The <i>pData</i> parameter must point to a boolean or DWORD value, depending on the value of the <i>OpCode</i> parameter. The <i>pData</i> parameter must not be <b>NULL</b>.

<div class="alert"><b>Note</b>  The <i>pData</i> parameter may point to an integer value when a boolean is required. If <i>pData</i> points to 0, then the value is converted to <b>FALSE</b>. If <i>pData</i> points to a nonzero integer, then the value is converted to <b>TRUE</b>. </div>
<div> </div>

### -param pReserved

Reserved for future use. Must be set to <b>NULL</b>.

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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. This error is returned if the caller does not have sufficient permissions to set the configuration parameter when the <i>OpCode</i> parameter is wlan_autoconf_opcode_show_denied_networks or wlan_autoconf_opcode_allow_virtual_station_extensibility. When the <i>OpCode</i> parameter is set to one of these values, the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetautoconfigparameter">WlanSetAutoConfigParameter</a>  function retrieves the discretionary access control list (DACL) stored for opcode object. If the DACL does not contain an access control entry (ACE) that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread, then <b>WlanSetAutoConfigParameter</b>  returns <b>ERROR_ACCESS_DENIED</b>.

This error is also returned if the configuration parameter is set by group policy on a domain. When group policy is set for an opcode, applications are prevented from making changes. For the following <i>OpCode</i> parameters may be set by group policy: wlan_autoconf_opcode_show_denied_networks, wlan_autoconf_opcode_allow_explicit_creds, and wlan_autoconf_opcode_block_period

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter was bad. This error is returned if the <i>hClientHandle</i> parameter is <b>NULL</b>, the <i>pData</i> parameter is <b>NULL</b>, or the <i>pReserved</i> parameter is not <b>NULL</b>. This error is also returned if <i>OpCode</i> parameter specified is not one of the <a href="/windows/win32/api/wlanapi/ne-wlanapi-wlan_autoconf_opcode-r1">WLAN_AUTOCONF_OPCODE</a> values for a configuration parameter that can be set. This error is also returned if the <i>dwDataSize</i> parameter is not set to <code>sizeof(BOOL)</code>, or the <i>dwDataSize</i> is not set to <code>sizeof(BOOL)</code> depending on the value of the <i>OpCode</i> parameter.

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
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
This function was called from an unsupported platform. This value will be returned if this function was called from a Windows XP with SP3 or Wireless LAN API for Windows XP with SP2 client.

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
</table>

## -remarks

The <b>WlanSetAutoConfigParameter</b> function sets parameters used by Auto Configuration Module (ACM), the wireless configuration component supported on Windows Vista and  later.

Depending on the value of the <i>OpCode</i> parameter, the data pointed to by <i>pData</i> will be converted to a boolean value before the automatic configuration parameter is set. If <i>pData</i> points to 0, then the parameter is set to <b>FALSE</b>; otherwise, the parameter is set to <b>TRUE</b>.

## -see-also

<a href="/windows/win32/api/wlanapi/ne-wlanapi-wlan_autoconf_opcode-r1">WLAN_AUTOCONF_OPCODE</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryautoconfigparameter">WlanQueryAutoConfigParameter</a>