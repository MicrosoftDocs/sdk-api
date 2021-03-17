---
UID: NF:wlanapi.WlanSetProfileCustomUserData
title: WlanSetProfileCustomUserData function (wlanapi.h)
description: Sets the custom user data associated with a profile.
helpviewer_keywords: ["WlanSetProfileCustomUserData","WlanSetProfileCustomUserData function [NativeWIFI]","nwifi.wlansetuserdata","wlanapi/WlanSetProfileCustomUserData"]
old-location: nwifi\wlansetuserdata.htm
tech.root: nwifi
ms.assetid: 3b37ff29-4c9b-42c8-b00a-a9dfca1d3fed
ms.date: 12/05/2018
ms.keywords: WlanSetProfileCustomUserData, WlanSetProfileCustomUserData function [NativeWIFI], nwifi.wlansetuserdata, wlanapi/WlanSetProfileCustomUserData
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
 - WlanSetProfileCustomUserData
 - wlanapi/WlanSetProfileCustomUserData
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
 - WlanSetProfileCustomUserData
---

# WlanSetProfileCustomUserData function


## -description

The <b>WlanSetProfileCustomUserData</b> function sets the custom user data associated with a profile.

## -parameters

### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param pInterfaceGuid [in]

The GUID of the interface.

### -param strProfileName [in]

The name of the profile associated with the custom user data. Profile names are case-sensitive. This string must be NULL-terminated.

### -param dwDataSize [in]

The size of <i>pData</i>, in bytes.

### -param pData [in]

A pointer to the user data to be set.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the following conditions occurred:

<ul>
<li><i>hClientHandle</i> is <b>NULL</b> or invalid.</li>
<li><i>pInterfaceGuid</i> is <b>NULL</b>.</li>
<li><i>strProfileName</i> is <b>NULL</b>.</li>
<li><i>pReserved</i> is not <b>NULL</b>.</li>
<li><i>dwDataSize</i> is not 0 and <i>pData</i> is <b>NULL</b>.</li>
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

For every wireless WLAN profile used by the Native Wifi AutoConfig service, Windows maintains the concept of custom user data.  This custom user data is initially non-existent, but can be set by calling the <b>WlanSetProfileCustomUserData</b> function. The custom user data gets reset to empty any time the profile is modified by calling the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile">WlanSetProfile</a> function.

Once custom user data has been set, this data can be accessed using the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilecustomuserdata">WlanGetProfileCustomUserData</a> function. 

All wireless LAN functions require an interface GUID for the wireless interface when performing profile operations. When a wireless interface is removed, its state is cleared from Wireless LAN Service (WLANSVC)  and no profile operations are possible.

The <b>WlanSetProfileCustomUserData</b> function can fail with <b>ERROR_INVALID_PARAMETER</b> if the wireless interface specified in the <i>pInterfaceGuid</i> parameter has been removed from the system (a USB  wireless adapter that has been removed, for example).

## -see-also

<a href="/windows/desktop/NativeWiFi/wlan-profileschema-schema">WLAN_profile Schema</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile">WlanGetProfile</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilecustomuserdata">WlanGetProfileCustomUserData</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilelist">WlanGetProfileList</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile">WlanSetProfile</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileeapuserdata">WlanSetProfileEapUserData</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileeapxmluserdata">WlanSetProfileEapXmlUserData</a>