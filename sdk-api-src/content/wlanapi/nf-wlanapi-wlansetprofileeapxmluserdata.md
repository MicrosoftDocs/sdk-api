---
UID: NF:wlanapi.WlanSetProfileEapXmlUserData
title: WlanSetProfileEapXmlUserData function (wlanapi.h)
description: Sets the Extensible Authentication Protocol (EAP) user credentials as specified by an XML string.
helpviewer_keywords: ["WLAN_SET_EAPHOST_DATA_ALL_USERS","WlanSetProfileEapXmlUserData","WlanSetProfileEapXmlUserData function [NativeWIFI]","nwifi.wlansetprofileeapxmluserdata","wlanapi/WlanSetProfileEapXmlUserData"]
old-location: nwifi\wlansetprofileeapxmluserdata.htm
tech.root: nwifi
ms.assetid: c34c39c0-8200-438a-8353-238225aea5cb
ms.date: 12/05/2018
ms.keywords: WLAN_SET_EAPHOST_DATA_ALL_USERS, WlanSetProfileEapXmlUserData, WlanSetProfileEapXmlUserData function [NativeWIFI], nwifi.wlansetprofileeapxmluserdata, wlanapi/WlanSetProfileEapXmlUserData
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
 - WlanSetProfileEapXmlUserData
 - wlanapi/WlanSetProfileEapXmlUserData
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
 - WlanSetProfileEapXmlUserData
---

## -description

The **WlanSetProfileEapXmlUserData** function sets the Extensible Authentication Protocol (EAP) user credentials as specified by an XML string. The user credentials apply to a profile on an adapter. These credentials can be used only by the caller.

## -parameters

### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="/windows/win32/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param pInterfaceGuid [in]

The GUID of the interface.

### -param strProfileName [in]

The name of the profile associated with the EAP user data. Profile names are case-sensitive. This string must be NULL-terminated.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>The supplied name must match the profile name derived automatically from the SSID of the network. For an infrastructure network profile, the SSID must be supplied for the profile name. For an ad hoc network profile, the supplied name must be the SSID of the ad hoc network followed by <code>-adhoc</code>.

### -param dwFlags [in]

A set of flags that modify the behavior of the function. 

On Wireless LAN API for Windows XP with SP2, Windows XP with SP3,Windows Vista, and Windows Server 2008, this parameter is reserved and should be set to zero. 

On Windows 7, Windows Server 2008 R2,  and later, this parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WLAN_SET_EAPHOST_DATA_ALL_USERS"></a><a id="wlan_set_eaphost_data_all_users"></a><dl>
<dt><b>WLAN_SET_EAPHOST_DATA_ALL_USERS</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Set EAP host data for all users of this profile.

</td>
</tr>
</table>

### -param strEapXmlUserData [in]

A pointer to XML data used to set the user credentials. 

The XML data must be based on the <a href="/windows/win32/eaphost/eaphostusercredentialsschema-schema">EAPHost User Credentials schema</a>. To view sample user credential XML data, see EAPHost <a href="/windows/win32/eaphost/user-profiles">User Properties</a>.

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
Access is denied. This value is returned if the caller does not have write access to the profile.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_PROFILE</b></dt>
</dl>
</td>
<td width="60%">
The network connection profile is corrupted. This error is returned if the profile specified in the <i>strProfileName</i> parameter could not be parsed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is incorrect. This value is returned if any of the following conditions occur:<ul>
<li><i>hClientHandle</i> is <b>NULL</b>.</li>
<li><i>pInterfaceGuid</i> is <b>NULL</b>.</li>
<li><i>strProfileName</i> is <b>NULL</b>.</li>
<li><i>strEapXmlUserData</i> is <b>NULL</b>.</li>
<li><i>pReserved</i> is not <b>NULL</b>.</li>
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
A handle is invalid. This error is returned if the handle <i>hClientHandle</i>  was not found in the handle table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough storage is available to process this command.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. 

This value is returned when profile settings do not permit storage of user data. This can occur when single signon (SSO) is enabled. 

On Windows 7, Windows Server 2008 R2 ,  and later, this value is returned if the <a href="/windows/win32/api/wlanapi/nf-wlanapi-wlansetprofileeapxmluserdata">WlanSetProfileEapXmlUserData</a> function was called on a profile that uses a method other than 802.1X for authentication. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_NOT_ACTIVE</b></dt>
</dl>
</td>
<td width="60%">
The service has not been started. This value is returned if the Wireless LAN service is not running.

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

The  **WlanSetProfileEapXmlUserData** function sets the EAP user credentials to use on a profile. This function can be called only on a profile that uses 802.1X for authentication. On Windows Vista and Windows Server 2008, these credentials can only be used by the caller.

The <i>eapType</i> parameter is an  <a href="/windows/win32/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a> structure that contains type, identification, and author information about an EAP method. The <b>eapType</b> member of the <b>EAP_METHOD_TYPE</b> structure is an  <a href="/windows/win32/api/eaptypes/ns-eaptypes-eap_type">EAP_TYPE</a> structure that contains the type and vendor identification information for an EAP method.

For more information on the allocation of EAP method types, see section 6.2 of <a href="http://tools.ietf.org/html/rfc3748">RFC 3748</a> published by the IETF.

On Windows 10, Windows Server 2016,  and later, the  **WlanSetProfileEapXmlUserData** function is enhanced. EAP user credentials can be set for all users of  a profile if the <i>dwFlags</i> parameter contains <b>WLAN_SET_EAPHOST_DATA_ALL_USERS</b>. 

All wireless LAN functions require an interface GUID for the wireless interface when performing profile operations. When a wireless interface is removed, its state is cleared from Wireless LAN Service (WLANSVC)  and no profile operations are possible.

The **WlanSetProfileEapXmlUserData** function can fail with <b>ERROR_INVALID_PARAMETER</b> if the wireless interface specified in the <i>pInterfaceGuid</i> parameter has been removed from the system (a USB  wireless adapter that has been removed, for example). 

The **WlanSetProfileEapXmlUserData** might cause wireless connection failure when you use **EAP-TTLS** and the API is called from a 32-bit application running on a 64-bit operating system (OS). Your application should be built for the same CPU architecture as the target OS.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2: </b>This function can only be used for Protected EAP (PEAP) credentials. It can't be used for other EAP types.

## -see-also

<a href="/windows/win32/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a>



<a href="/windows/win32/api/eaptypes/ns-eaptypes-eap_type">EAP_TYPE</a>



<a href="/windows/win32/api/wlanapi/nf-wlanapi-wlangetprofile">WlanGetProfile</a>



<a href="/windows/win32/api/wlanapi/nf-wlanapi-wlangetprofilecustomuserdata">WlanGetProfileCustomUserData</a>



<a href="/windows/win32/api/wlanapi/nf-wlanapi-wlangetprofilelist">WlanGetProfileList</a>



<a href="/windows/win32/api/wlanapi/nf-wlanapi-wlansetprofile">WlanSetProfile</a>



<a href="/windows/win32/api/wlanapi/nf-wlanapi-wlansetprofilecustomuserdata">WlanSetProfileCustomUserData</a>



<a href="/windows/win32/api/wlanapi/nf-wlanapi-wlansetprofileeapuserdata">WlanSetProfileEapUserData</a>
