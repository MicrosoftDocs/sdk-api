---
UID: NF:wlanapi.WlanSetFilterList
title: WlanSetFilterList function (wlanapi.h)
description: Sets the permit/deny list.
helpviewer_keywords: ["WlanSetFilterList","WlanSetFilterList function [NativeWIFI]","nwifi.wlansetfilterlist","wlanapi/WlanSetFilterList"]
old-location: nwifi\wlansetfilterlist.htm
tech.root: nwifi
ms.assetid: 697682c9-cb26-42d6-86b5-d7adebcedc68
ms.date: 12/05/2018
ms.keywords: WlanSetFilterList, WlanSetFilterList function [NativeWIFI], nwifi.wlansetfilterlist, wlanapi/WlanSetFilterList
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
 - WlanSetFilterList
 - wlanapi/WlanSetFilterList
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
 - WlanSetFilterList
---

# WlanSetFilterList function


## -description

The <b>WlanSetFilterList</b> function sets the permit/deny list.

## -parameters

### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param wlanFilterListType [in]

A <a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_filter_list_type">WLAN_FILTER_LIST_TYPE</a> value that specifies the type of filter list.  The value must be either <b>wlan_filter_list_type_user_permit</b> or <b>wlan_filter_list_type_user_deny</b>.  Group policy-defined lists cannot be set using this function.

### -param pNetworkList [in, optional]

Pointer to a <a href="/windows/desktop/api/wlanapi/ns-wlanapi-dot11_network_list">DOT11_NETWORK_LIST</a> structure that contains the list of networks to permit or deny. The <b>dwIndex</b> member of the structure must have a value less than the value of the <b>dwNumberOfItems</b> member of the structure; otherwise, an access violation may occur.

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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient permissions to set the filter list. 

When called with <i>wlanFilterListType</i> set to <b>wlan_filter_list_type_user_permit</b>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist">WlanSetFilterList</a> retrieves the discretionary access control list (DACL) stored with the  <b>wlan_secure_permit_list</b> object. When called with <i>wlanFilterListType</i>  set to <b>wlan_filter_list_type_user_deny</b>, <b>WlanSetFilterList</b> retrieves the DACL stored with the  <b>wlan_secure_deny_list</b> object. In either of these cases, if the DACL does not contain an access control entry (ACE) that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread, then <b>WlanSetFilterList</b>  returns <b>ERROR_ACCESS_DENIED</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
<i>hClientHandle</i> is <b>NULL</b> or invalid or <i>pReserved</i> is not <b>NULL</b>.

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

The group policy permit and deny lists take precedence over the user's permit and deny lists. That means access to a network on the user's permit list will be denied if the network appears on the group policy deny list. Similarly, access to a network on the user's deny list will be permitted if the network appears on the group policy permit list. Networks that are not on a user  list or a group policy list will be permitted.  

Denied networks cannot be connected by means of auto config and will not be included on the visible networks list. New user permit and deny lists overwrite previous versions of the user lists.  

To clear a filter list, set the <i>pNetworkList</i> parameter to <b>NULL</b>, or pass a pointer to a <a href="/windows/desktop/api/wlanapi/ns-wlanapi-dot11_network_list">DOT11_NETWORK_LIST</a> structure that has the <b>dwNumberOfItems</b> member set to 0.

To add all SSIDs to a filter list, pass a pointer to a  <a href="/windows/desktop/api/wlanapi/ns-wlanapi-dot11_network_list">DOT11_NETWORK_LIST</a> structure with an associated <a href="/windows/desktop/api/wlanapi/ns-wlanapi-dot11_network">DOT11_NETWORK</a> structure that has the  <b>uSSIDLength</b> member of its <a href="/windows/desktop/NativeWiFi/dot11-ssid">DOT11_SSID</a> structure set to 0.

To add all BSS types to a filter list, pass a pointer to a  <a href="/windows/desktop/api/wlanapi/ns-wlanapi-dot11_network_list">DOT11_NETWORK_LIST</a> with an associated <a href="/windows/desktop/api/wlanapi/ns-wlanapi-dot11_network">DOT11_NETWORK</a> structure that has its <b>dot11BssType</b> member set to <b>dot11_BSS_type_any</b>.

The <b>netsh wlan add filter</b> and <b>netsh wlan delete filter</b> commands provide similar functionality at the command line. For more information, see <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)">Netsh Commands for Wireless Local Area Network (wlan)</a>.

## -see-also

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist">WlanGetFilterList</a>