---
UID: NF:wlanapi.WlanSetProfileEapUserData
title: WlanSetProfileEapUserData function (wlanapi.h)
description: Sets the Extensible Authentication Protocol (EAP) user credentials as specified by raw EAP data.
helpviewer_keywords: ["WLAN_SET_EAPHOST_DATA_ALL_USERS","WlanSetProfileEapUserData","WlanSetProfileEapUserData function [NativeWIFI]","nwifi.wlansetprofileeapuserdata","wlanapi/WlanSetProfileEapUserData"]
old-location: nwifi\wlansetprofileeapuserdata.htm
tech.root: NativeWiFi
ms.assetid: 2bef0f2f-165d-446a-afa8-735658048152
ms.date: 12/05/2018
ms.keywords: WLAN_SET_EAPHOST_DATA_ALL_USERS, WlanSetProfileEapUserData, WlanSetProfileEapUserData function [NativeWIFI], nwifi.wlansetprofileeapuserdata, wlanapi/WlanSetProfileEapUserData
f1_keywords:
- wlanapi/WlanSetProfileEapUserData
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- wlanapi.dll
api_name:
- WlanSetProfileEapUserData
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WlanSetProfileEapUserData function


## -description


The  <b>WlanSetProfileEapUserData</b> function sets the Extensible Authentication Protocol (EAP) user credentials as specified by raw EAP data. The user credentials apply to a profile on an interface. 


## -parameters




### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="https://docs.microsoft.com/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.


### -param pInterfaceGuid [in]

The GUID of the interface.


### -param strProfileName [in]

The name of the profile associated with the EAP user data. Profile names are case-sensitive. This string must be NULL-terminated.


### -param eapType [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a> structure that contains the method for which the caller is supplying EAP user credentials.


### -param dwFlags [in]

A set of flags that modify the behavior of the function. 

On Windows Vista and Windows Server 2008, this parameter is reserved and should be set to zero. 

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
 


### -param dwEapUserDataSize [in]

The size, in bytes, of the data pointed to by <i>pbEapUserData</i>.


### -param pbEapUserData [in]

A pointer to the raw EAP data used to set the user credentials.

On Windows Vista and Windows Server 2008, this parameter must not be <b>NULL</b>. 

On Windows 7, Windows Server 2008 R2,  and later, this parameter can be set to <b>NULL</b> to delete the stored credentials for this profile if the <i>dwFlags</i> parameter contains <b>WLAN_SET_EAPHOST_DATA_ALL_USERS</b>  and the <i>dwEapUserDataSize</i> parameter is 0.


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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is incorrect. This value is returned if any of the following conditions occur:

<ul>
<li><i>hClientHandle</i> is <b>NULL</b>.</li>
<li><i>pInterfaceGuid</i> is <b>NULL</b>.</li>
<li><i>strProfileName</i> is <b>NULL</b></li>
<li><i>pvReserved</i> is not <b>NULL</b>.</li>
</ul>


On Windows Vista and Windows Server 2008, this value is returned if the <i>pbEapUserData</i> parameter is <b>NULL</b>. 

On Windows 7, Windows Server 2008 R2 ,  and later, this error is returned if the <i>pbEapUserData</i> parameter is <b>NULL</b>, but the <i>dwEapUserDataSize</i> parameter is not 0 or the <i>dwFlags</i> parameter does not contain <b>WLAN_SET_EAPHOST_DATA_ALL_USERS</b>.

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

This value is returned when profile settings do not permit storage of user data. This can occur when single signon (SSO) is enabled  or when the request was to delete the stored credentials for this profile (the <i>pbEapUserData</i> parameter was <b>NULL</b>, the  <i>dwFlags</i> parameter contains <b>WLAN_SET_EAPHOST_DATA_ALL_USERS</b>,   and the <i>dwEapUserDataSize</i> parameter is 0). 

On Windows 10, Windows Server 2016 ,  and later, this value is returned if the <a href="https://docs.microsoft.com/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileeapuserdata">WlanSetProfileEapUserData</a> function was called on a profile that uses a method other than 802.1X for authentication. 

This value is also returned if this function was called from a Windows XP with SP3 or Wireless LAN API for Windows XP with SP2 client.

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



The  <b>WlanSetProfileEapUserData</b> function sets the EAP user credentials to use on a profile.  On Windows Vista and Windows Server 2008, these credentials can only be used by the caller.

The <i>eapType</i> parameter is an  <a href="https://docs.microsoft.com/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a> structure that contains type, identification, and author information about an EAP method. The <b>eapType</b> member of the <b>EAP_METHOD_TYPE</b> structure is an  <a href="https://docs.microsoft.com/windows/desktop/api/eaptypes/ns-eaptypes-eap_type">EAP_TYPE</a> structure that contains the type and vendor identification information for an EAP method.


For more information on the allocation of EAP method types, see section 6.2 of <a href="http://tools.ietf.org/html/rfc3748">RFC 3748</a> published by the IETF.

On Windows 7, Windows Server 2008 R2,  and later, the  <b>WlanSetProfileEapUserData</b> function is enhanced. EAP user credentials can be set for all users of  a profile if the <i>dwFlags</i> parameter contains <b>WLAN_SET_EAPHOST_DATA_ALL_USERS</b>. The EAP user credentials on a profile can also be  deleted. To delete the EAP user credentials on a profile, the <i>pbEapUserData</i> parameter must be <b>NULL</b>, the <i>dwFlags</i> parameter must equal <b>WLAN_SET_EAPHOST_DATA_ALL_USERS</b>,  and the <i>dwEapUserDataSize</i> parameter must be 0.

All wireless LAN functions require an interface GUID for the wireless interface when performing profile operations. When a wireless interface is removed, its state is cleared from Wireless LAN Service (WLANSVC)  and no profile operations are possible.

The <b>WlanSetProfileEapUserData</b> function can fail with <b>ERROR_INVALID_PARAMETER</b> if the wireless interface specified in the <i>pInterfaceGuid</i> parameter has been removed from the system (a USB  wireless adapter that has been removed, for example). 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/eaptypes/ns-eaptypes-eap_type">EAP_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile">WlanGetProfile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilecustomuserdata">WlanGetProfileCustomUserData</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilelist">WlanGetProfileList</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile">WlanSetProfile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileeapxmluserdata">WlanSetProfileEapXmlUserData</a>
 

 

