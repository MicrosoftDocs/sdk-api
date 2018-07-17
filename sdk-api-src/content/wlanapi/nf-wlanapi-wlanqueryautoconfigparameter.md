---
UID: NF:wlanapi.WlanQueryAutoConfigParameter
title: WlanQueryAutoConfigParameter function
author: windows-sdk-content
description: Queries for the parameters of the auto configuration service.
old-location: nwifi\wlanqueryautoconfigparameter.htm
old-project: nativewifi
ms.assetid: 30fcfcf1-0784-4f20-b8c7-311227d0cfca
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: WlanQueryAutoConfigParameter, WlanQueryAutoConfigParameter function [NativeWIFI], nwifi.wlanqueryautoconfigparameter, wlan_autoconf_opcode_allow_explicit_creds, wlan_autoconf_opcode_allow_virtual_station_extensibility, wlan_autoconf_opcode_block_period, wlan_autoconf_opcode_only_use_gp_profiles_for_allowed_networks, wlan_autoconf_opcode_power_setting, wlan_autoconf_opcode_show_denied_networks, wlanapi/WlanQueryAutoConfigParameter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: WL_DISPLAY_PAGES, *PWL_DISPLAY_PAGES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wlanapi.dll
api_name:
 - WlanQueryAutoConfigParameter
product: Windows
targetos: Windows
req.lib: Wlanapi.lib
req.dll: Wlanapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WlanQueryAutoConfigParameter function


## -description


The <b>WlanQueryAutoConfigParameter</b> function queries for the parameters of the auto configuration service.


## -parameters




### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="https://msdn.microsoft.com/27bfa0c1-4443-47a4-a374-326f553fa3bb">WlanOpenHandle</a> function.


### -param OpCode [in]

A value that specifies the configuration parameter to be queried.

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
When set, the <i>ppData</i> parameter will contain a <b>BOOL</b> value indicating whether user and group policy-denied networks will be included in the available networks list. 

If the function returns ERROR_SUCCESS and <i>ppData</i> points to <b>TRUE</b>, then user and group policy-denied networks will be included in the available networks list; if <b>FALSE</b>, user and group policy-denied networks will not be included in the available networks list. 

</td>
</tr>
<tr>
<td width="40%"><a id="wlan_autoconf_opcode_power_setting"></a><a id="WLAN_AUTOCONF_OPCODE_POWER_SETTING"></a><dl>
<dt><b>wlan_autoconf_opcode_power_setting</b></dt>
</dl>
</td>
<td width="60%">
When set, the <i>ppData</i> parameter will contain a <a href="https://msdn.microsoft.com/f2509c87-8a2a-4e6e-9995-e824a17e7083">WLAN_POWER_SETTING</a> value specifying the power settings.

</td>
</tr>
<tr>
<td width="40%"><a id="wlan_autoconf_opcode_only_use_gp_profiles_for_allowed_networks"></a><a id="WLAN_AUTOCONF_OPCODE_ONLY_USE_GP_PROFILES_FOR_ALLOWED_NETWORKS"></a><dl>
<dt><b>wlan_autoconf_opcode_only_use_gp_profiles_for_allowed_networks</b></dt>
</dl>
</td>
<td width="60%">
When set, the <i>ppData</i> parameter will contain a <b>BOOL</b> value indicating whether profiles not created by group policy can be used to connect to an allowed network with a matching group policy profile. 

If the function returns ERROR_SUCCESS and <i>ppData</i> points to <b>TRUE</b>, then only profiles created by group policy can be used; if <b>FALSE</b>, any profile can be used. 

</td>
</tr>
<tr>
<td width="40%"><a id="wlan_autoconf_opcode_allow_explicit_creds"></a><a id="WLAN_AUTOCONF_OPCODE_ALLOW_EXPLICIT_CREDS"></a><dl>
<dt><b>wlan_autoconf_opcode_allow_explicit_creds</b></dt>
</dl>
</td>
<td width="60%">
When set, the <i>ppData</i> parameter will contain a <b>BOOL</b> value indicating whether the current wireless interface has shared user credentials allowed. 

If the function returns ERROR_SUCCESS and <i>ppData</i> points to <b>TRUE</b>, then the current wireless interface has shared user credentials allowed; if <b>FALSE</b>, the current wireless interface does not allow shared user credentials. 

</td>
</tr>
<tr>
<td width="40%"><a id="wlan_autoconf_opcode_block_period"></a><a id="WLAN_AUTOCONF_OPCODE_BLOCK_PERIOD"></a><dl>
<dt><b>wlan_autoconf_opcode_block_period</b></dt>
</dl>
</td>
<td width="60%">
When set, the <i>ppData</i> parameter will contain a <b>DWORD</b> value that indicates the blocked period setting for the current wireless interface. The blocked period is the amount of time, in seconds, for which automatic connection to a wireless network will not be attempted after a previous failure.

</td>
</tr>
<tr>
<td width="40%"><a id="wlan_autoconf_opcode_allow_virtual_station_extensibility"></a><a id="WLAN_AUTOCONF_OPCODE_ALLOW_VIRTUAL_STATION_EXTENSIBILITY"></a><dl>
<dt><b>wlan_autoconf_opcode_allow_virtual_station_extensibility</b></dt>
</dl>
</td>
<td width="60%">
When set, the <i>ppData</i> parameter will contain a <b>BOOL</b> value indicating whether extensibility on a virtual station is allowed. By default, extensibility on a virtual station is allowed. The value for this opcode is persisted across restarts. 

If the function returns ERROR_SUCCESS and <i>ppData</i> points to <b>TRUE</b>, then extensibility on a virtual station is allowed; if <b>FALSE</b>, extensibility on a virtual station is not allowed. 

</td>
</tr>
</table>
 


### -param pReserved

Reserved for future use.  Must be set to <b>NULL</b>.


### -param pdwDataSize [out]

Specifies the size of the <i>ppData</i> parameter, in bytes.


### -param ppData [out]

Pointer to the memory that contains the queried value for the parameter specified in <i>OpCode</i>.

<div class="alert"><b>Note</b>  If <i>OpCode</i> is set to <b>wlan_autoconf_opcode_show_denied_networks</b>, then the pointer referenced by <i>ppData</i> may point to an integer value. If the pointer referenced by <i>ppData</i> points to 0, then the integer value should be converted  to the boolean value <b>FALSE</b>. If the pointer referenced by <i>ppData</i> points to a nonzero integer, then the integer value should be converted  to the boolean value <b>TRUE</b>. </div>
<div> </div>

### -param pWlanOpcodeValueType [out, optional]

A <a href="https://msdn.microsoft.com/36f74ee5-499e-4d3d-ae32-a57c5e3b2eac">WLAN_OPCODE_VALUE_TYPE</a> value. 


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
The caller does not have sufficient permissions to get configuration parameters. 

When called with <i>OpCode</i> set to <b>wlan_autoconf_opcode_show_denied_networks</b>, <a href="https://msdn.microsoft.com/30fcfcf1-0784-4f20-b8c7-311227d0cfca">WlanQueryAutoConfigParameter</a> retrieves the discretionary access control list (DACL) stored with the  <b>wlan_secure_show_denied</b> object. If the DACL does not contain an access control entry (ACE) that grants WLAN_READ_ACCESS permission to the access token of the calling thread, then <b>WlanQueryAutoConfigParameter</b>  returns <b>ERROR_ACCESS_DENIED</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
<i>hClientHandle</i> is <b>NULL</b> or invalid, <i>pReserved</i> is not <b>NULL</b>, <i>ppData</i> is <b>NULL</b>, or <i>pdwDataSize</i> is <b>NULL</b>.

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



The <b>WlanQueryAutoConfigParameter</b> function queries for the parameters used by Auto Configuration Module (ACM), the wireless configuration component supported on Windows Vista and  later.




## -see-also




<a href="https://msdn.microsoft.com/d7816d6f-0f8c-4d53-aa70-357aaca360d0">WLAN_AUTOCONF_OPCODE</a>



<a href="https://msdn.microsoft.com/4f2514be-f05e-4be6-8c74-ef7a9ffe1c53">WlanSetAutoConfigParameter</a>
 

 

