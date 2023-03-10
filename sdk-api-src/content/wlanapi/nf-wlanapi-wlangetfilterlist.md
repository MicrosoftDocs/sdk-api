---
UID: NF:wlanapi.WlanGetFilterList
title: WlanGetFilterList function (wlanapi.h)
description: Retrieves a group policy or user permission list.
helpviewer_keywords: ["WlanGetFilterList","WlanGetFilterList function [NativeWIFI]","nwifi.wlangetfilterlist","wlanapi/WlanGetFilterList"]
old-location: nwifi\wlangetfilterlist.htm
tech.root: nwifi
ms.assetid: 3ea88e52-34bb-47a6-b345-c789d1d8047d
ms.date: 12/05/2018
ms.keywords: WlanGetFilterList, WlanGetFilterList function [NativeWIFI], nwifi.wlangetfilterlist, wlanapi/WlanGetFilterList
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
 - WlanGetFilterList
 - wlanapi/WlanGetFilterList
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
 - WlanGetFilterList
---

# WlanGetFilterList function


## -description

The <b>WlanGetFilterList</b> function retrieves a group policy or user permission list.

## -parameters

### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param wlanFilterListType [in]

A <a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_filter_list_type">WLAN_FILTER_LIST_TYPE</a> value that specifies the type of filter list.  All user defined and group policy filter lists can be queried.

### -param pReserved

Reserved for future use.  Must be set to <b>NULL</b>.

### -param ppNetworkList [out]

Pointer to a <a href="/windows/desktop/api/wlanapi/ns-wlanapi-dot11_network_list">DOT11_NETWORK_LIST</a> structure that contains the list of permitted or denied networks.

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
The caller does not have sufficient permissions to get the filter list. 

When called with <i>wlanFilterListType</i> set to <b>wlan_filter_list_type_user_permit</b>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist">WlanGetFilterList</a> retrieves the discretionary access control list (DACL) stored with the  <b>wlan_secure_permit_list</b> object. When called with <i>wlanFilterListType</i> set to <b>wlan_filter_list_type_user_deny</b>, <b>WlanGetFilterList</b> retrieves the DACL stored with the  <b>wlan_secure_deny_list</b> object. In either of these cases, if the DACL does not contain an access control entry (ACE) that grants WLAN_READ_ACCESS permission to the access token of the calling thread, then <b>WlanGetFilterList</b>  returns <b>ERROR_ACCESS_DENIED</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
<i>hClientHandle</i> is <b>NULL</b> or invalid, <i>ppNetworkList</i> is <b>NULL</b>, or <i>pReserved</i> is not <b>NULL</b>.

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

User permission lists can be set by calling <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist">WlanSetFilterList</a>.

## -see-also

<a href="/windows/desktop/api/wlanapi/ns-wlanapi-dot11_network_list">DOT11_NETWORK_LIST</a>



<a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_filter_list_type">WLAN_FILTER_LIST_TYPE</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist">WlanSetFilterList</a>