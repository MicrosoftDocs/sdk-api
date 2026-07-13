---
UID: NF:wlanapi.WlanGetProfile
title: WlanGetProfile function (wlanapi.h)
description: Retrieves all information about a specified wireless profile.
helpviewer_keywords: ["WLAN_PROFILE_GET_PLAINTEXT_KEY","WLAN_PROFILE_GROUP_POLICY","WLAN_PROFILE_USER","WlanGetProfile","WlanGetProfile function [NativeWIFI]","nwifi.wlangetprofile","wlanapi/WlanGetProfile"]
old-location: nwifi\wlangetprofile.htm
tech.root: nwifi
ms.assetid: 6486e961-402f-45c8-a806-ab91a4f0f156
ms.date: 12/05/2018
ms.keywords: WLAN_PROFILE_GET_PLAINTEXT_KEY, WLAN_PROFILE_GROUP_POLICY, WLAN_PROFILE_USER, WlanGetProfile, WlanGetProfile function [NativeWIFI], nwifi.wlangetprofile, wlanapi/WlanGetProfile
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
 - WlanGetProfile
 - wlanapi/WlanGetProfile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - wlanapi.dll
 - Ext-MS-Win-networking-wlanapi-l1-1-0.dll
api_name:
 - WlanGetProfile
---

# WlanGetProfile function


## -description

The <b>WlanGetProfile</b> function retrieves all information about a  specified wireless profile.

## -parameters

### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param pInterfaceGuid [in]

The GUID of the wireless interface. 

A list of the GUIDs for wireless interfaces on the local computer can be retrieved using the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces">WlanEnumInterfaces</a> function.

### -param strProfileName [in]

The name of the profile. Profile names are case-sensitive. This string must be NULL-terminated. The maximum length of the profile name is 255 characters. This means that the maximum length of this string, including the NULL terminator, is 256 characters.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>The name of the profile is derived automatically from the SSID of the network. For infrastructure network profiles, the name of the profile is the SSID of the network. For ad hoc network profiles, the name of the profile is the SSID of the ad hoc network followed by <code>-adhoc</code>.

### -param pReserved [in]

Reserved for future use.  Must be set to <b>NULL</b>.

### -param pstrProfileXml [out]

A string that is the XML representation of the queried profile. There is no predefined maximum string length.

### -param pdwFlags [in, out, optional]

On input, a pointer to the address location used to provide additional information about the request. If this parameter is <b>NULL</b> on input, then no information on profile flags will be returned. On output,  a pointer to the address location used to receive profile flags.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>Per-user profiles are not supported. Set this parameter to <b>NULL</b>. 


The <i>pdwFlags</i> parameter can point to an address location that contains the following values:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WLAN_PROFILE_GET_PLAINTEXT_KEY"></a><a id="wlan_profile_get_plaintext_key"></a><dl>
<dt><b>WLAN_PROFILE_GET_PLAINTEXT_KEY</b></dt>
</dl>
</td>
<td width="60%">
On input, this flag indicates that the caller wants to retrieve the plain text key from a wireless profile. If the calling thread has the required permissions, the  <b>WlanGetProfile</b> function returns the plain text key in the <a href="/windows/win32/nativewifi/wlan-profileschema-sharedkey-security-element#keymaterial">keyMaterial</a> element of the profile returned in the buffer pointed to by the   <i>pstrProfileXml</i> parameter.

For the <b>WlanGetProfile</b> call to return the plain text key, the <b>wlan_secure_get_plaintext_key</b> permissions from the <a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object">WLAN_SECURABLE_OBJECT</a> enumerated type must be set on the calling thread. The DACL must also contain an ACE that grants <b>WLAN_READ_ACCESS</b> permission to the access token of the calling thread. By default,  the permissions for retrieving the plain text key is allowed only to the members of the Administrators group on a local machine.



If the calling thread lacks the required permissions, the <b>WlanGetProfile</b> function returns the encrypted key in the <a href="/windows/win32/nativewifi/wlan-profileschema-sharedkey-security-element#keymaterial">keyMaterial</a> element of the profile returned in the buffer pointed to by the   <i>pstrProfileXml</i> parameter. No error is returned if the calling thread lacks the required permissions. 

<b>Windows 7:  </b>This flag passed on input is an extension to native wireless APIs added on Windows 7 and  later.  The <i>pdwFlags</i> parameter is an __inout_opt parameter on Windows 7 and  later.  

</td>
</tr>
<tr>
<td width="40%"><a id="WLAN_PROFILE_GROUP_POLICY"></a><a id="wlan_profile_group_policy"></a><dl>
<dt><b>WLAN_PROFILE_GROUP_POLICY</b></dt>
</dl>
</td>
<td width="60%">
On output when the <b>WlanGetProfile</b> call is successful, this flag indicates that this profile was created by group policy.  A group policy profile is read-only. Neither the content nor the preference order of the profile can be changed.

</td>
</tr>
<tr>
<td width="40%"><a id="WLAN_PROFILE_USER"></a><a id="wlan_profile_user"></a><dl>
<dt><b>WLAN_PROFILE_USER</b></dt>
</dl>
</td>
<td width="60%">
On output when the <b>WlanGetProfile</b> call is successful, this flag indicates that the profile is a user profile for the specific user in whose context the calling thread resides. If not set, this profile is an all-user profile.

</td>
</tr>
</table>

### -param pdwGrantedAccess [out, optional]

The access mask of the all-user profile.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>WLAN_READ_ACCESS</dt>
</dl>
</td>
<td width="60%">
The user can view the contents of the profile.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>WLAN_EXECUTE_ACCESS</dt>
</dl>
</td>
<td width="60%">
The user has read access, and the user can also connect to and disconnect from a network using the profile. If a user has WLAN_EXECUTE_ACCESS, then the user also has WLAN_READ_ACCESS. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>WLAN_WRITE_ACCESS</dt>
</dl>
</td>
<td width="60%">
The user has execute access and the user can also modify the content of the  profile or delete the profile. If a user has WLAN_WRITE_ACCESS, then the user also has WLAN_EXECUTE_ACCESS and WLAN_READ_ACCESS.

</td>
</tr>
</table>

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
The caller does not have sufficient permissions.  This error is returned if the <i>pstrProfileXml</i> parameter specifies an all-user profile, but the caller does not have read access on the profile. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
A handle is invalid. This error is returned if the handle specified in the <i>hClientHandle</i>  parameter was not found in the handle table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is incorrect. This error is returned if any of the following conditions occur:<ul>
<li><i>hClientHandle</i> is <b>NULL</b>.</li>
<li><i>pInterfaceGuid</i> is <b>NULL</b>.</li>
<li><i>pstrProfileXml</i>  is <b>NULL</b>.</li>
<li><i>pReserved</i> is not <b>NULL</b>.</li>
</ul>


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough storage is available to process this command. This error is returned if the system was unable to allocate memory for the profile.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The profile specified by <i>strProfileName</i> was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Various RPC and other error codes. Use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.


</td>
</tr>
</table>

## -remarks

If the <b>WlanGetProfile</b> function succeeds, the wireless profile is returned in the buffer pointed to by the <i>pstrProfileXml</i> parameter. The buffer contains a string that is the XML representation of the queried profile. For a description of the XML representation of the wireless profile, see <a href="/windows/desktop/NativeWiFi/wlan-policyschema-schema">WLAN_profile Schema</a>. 

The caller is responsible for calling the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory">WlanFreeMemory</a> function to free the memory allocated for the buffer pointer to by the <i>pstrProfileXml</i> parameter when the buffer is no longer needed.

If <i>pstrProfileXml</i> specifies an all-user profile, the <b>WlanGetProfile</b>  caller must have read access on the profile. Otherwise, the <b>WlanGetProfile</b> call will fail with a return value of <b>ERROR_ACCESS_DENIED</b>. The permissions on an all-user profile are established when the profile is created or saved using <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile">WlanSetProfile</a> or <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansavetemporaryprofile">WlanSaveTemporaryProfile</a>.

<b>Windows 7:  </b><p class="note">The <a href="/windows/win32/nativewifi/wlan-profileschema-sharedkey-security-element#keymaterial">keyMaterial</a> element returned in the profile schema pointed to by the <i>pstrProfileXml</i> may be requested as plaintext if the <b>WlanGetProfile</b> function is called with the <b>WLAN_PROFILE_GET_PLAINTEXT_KEY</b>  flag set in the value pointed to by the <i>pdwFlags</i> parameter on input.   

<p class="note">For a WEP key, both 5 ASCII characters or 10 hexadecimal characters can be used to set the plaintext key when the profile is created or updated. However, a WEP profile will be saved with  10 hexadecimal characters in the key no matter what the original input was used to create the profile. So in the profile returned by the  <b>WlanGetProfile</b> function, the plaintext WEP key  is always returned as 10 hexadecimal characters.


<p class="note">For the <b>WlanGetProfile</b> call to return the plain text key, the <b>wlan_secure_get_plaintext_key</b> permissions from the <a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object">WLAN_SECURABLE_OBJECT</a> enumerated type must be set on the calling thread. The DACL must also contain an ACE that grants <b>WLAN_READ_ACCESS</b> permission to the access token of the calling thread. By default,  the permissions for retrieving the plain text key is allowed only to the members of the Administrators group on a local machine.



<p class="note">If the calling thread lacks the required permissions, the <b>WlanGetProfile</b> function returns the encrypted key in the <a href="/windows/win32/nativewifi/wlan-profileschema-sharedkey-security-element#keymaterial">keyMaterial</a> element of the profile returned in the buffer pointed to by the   <i>pstrProfileXml</i> parameter. No error is returned if the calling thread lacks the required permissions. 

<p class="note">By default, the <a href="/windows/win32/nativewifi/wlan-profileschema-sharedkey-security-element#keymaterial">keyMaterial</a> element returned in the profile pointed to by the <i>pstrProfileXml</i> is encrypted.   If your process runs in the context of the LocalSystem account on the same computer, then you can unencrypt key material by calling the <a href="/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata">CryptUnprotectData</a> function. 



<b>Windows Server 2008 and Windows Vista:  </b>The <a href="/windows/win32/nativewifi/wlan-profileschema-sharedkey-security-element#keymaterial">keyMaterial</a> element returned in the profile schema pointed to by the <i>pstrProfileXml</i> is always encrypted.  If your process runs in the context of the LocalSystem account, then you can unencrypt key material by calling the <a href="/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata">CryptUnprotectData</a> function.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>The key material is never encrypted.


#### Examples

The following example enumerates the wireless LAN interfaces on the local computer, retrieves information for a specific wireless profile on each wireless LAN interface, and prints the values retrieved. The string that is the XML representation of the queried profile is also printed.

<div class="alert"><b>Note</b>  This example will fail to load on Windows Server 2008 and Windows Server 2008 R2 if the Wireless LAN Service is not installed and started.</div>
<div> </div>

```cpp
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#include <wlanapi.h>
#include <objbase.h>
#include <wtypes.h>

#include <stdio.h>
#include <stdlib.h>

// Need to link with Wlanapi.lib and Ole32.lib
#pragma comment(lib, "wlanapi.lib")
#pragma comment(lib, "ole32.lib")


int _cdecl wmain(int argc, WCHAR **argv)
{

    // Declare and initialize variables.

    HANDLE hClient = NULL;
    DWORD dwMaxClient = 2;      //    
    DWORD dwCurVersion = 0;
    DWORD dwResult = 0;
    DWORD dwRetVal = 0;
    int iRet = 0;
    
    WCHAR GuidString[39] = {0};

    unsigned int i;

    /* variables used for WlanEnumInterfaces  */

    PWLAN_INTERFACE_INFO_LIST pIfList = NULL;
    PWLAN_INTERFACE_INFO pIfInfo = NULL;

    LPCWSTR pProfileName = NULL;
    LPWSTR pProfileXml = NULL;
    DWORD dwFlags = 0;
    DWORD dwGrantedAccess = 0;
   
        // Validate the parameters
    if (argc < 2) {
        wprintf(L"usage: %s <profile>\n", argv[0]);
        wprintf(L"   Gets a wireless profile\n");
        wprintf(L"   Example\n");
        wprintf(L"       %s \"Default Wireless\"\n", argv[0]);
        exit(1);
    }
    
    pProfileName = argv[1];
     
    wprintf(L"Information for profile: %ws\n\n", pProfileName);
    
    dwResult = WlanOpenHandle(dwMaxClient, NULL, &dwCurVersion, &hClient);
    if (dwResult != ERROR_SUCCESS) {
        wprintf(L"WlanOpenHandle failed with error: %u\n", dwResult);
        return 1;
        // You can use FormatMessage here to find out why the function failed
    }

    dwResult = WlanEnumInterfaces(hClient, NULL, &pIfList);
    if (dwResult != ERROR_SUCCESS) {
        wprintf(L"WlanEnumInterfaces failed with error: %u\n", dwResult);
        return 1;
        // You can use FormatMessage here to find out why the function failed
    } else {
        wprintf(L"WLAN_INTERFACE_INFO_LIST for this system\n");

        wprintf(L"Num Entries: %lu\n", pIfList->dwNumberOfItems);
        wprintf(L"Current Index: %lu\n\n", pIfList->dwIndex);
        for (i = 0; i < (int) pIfList->dwNumberOfItems; i++) {
            pIfInfo = (WLAN_INTERFACE_INFO *) &pIfList->InterfaceInfo[i];
            wprintf(L"  Interface Index[%u]:\t %lu\n", i, i);
            iRet = StringFromGUID2(pIfInfo->InterfaceGuid, (LPOLESTR) &GuidString, 
                sizeof(GuidString)/sizeof(*GuidString)); 
            // For c rather than C++ source code, the above line needs to be
            // iRet = StringFromGUID2(&pIfInfo->InterfaceGuid, (LPOLESTR) &GuidString, 
            //     sizeof(GuidString)/sizeof(*GuidString)); 
            if (iRet == 0)
                wprintf(L"StringFromGUID2 failed\n");
            else {
                wprintf(L"  InterfaceGUID[%d]: %ws\n",i, GuidString);
            }    
            wprintf(L"  Interface Description[%d]: %ws", i, 
                pIfInfo->strInterfaceDescription);
            wprintf(L"\n");
            wprintf(L"  Interface State[%d]:\t ", i);
            switch (pIfInfo->isState) {
            case wlan_interface_state_not_ready:
                wprintf(L"Not ready\n");
                break;
            case wlan_interface_state_connected:
                wprintf(L"Connected\n");
                break;
            case wlan_interface_state_ad_hoc_network_formed:
                wprintf(L"First node in a ad hoc network\n");
                break;
            case wlan_interface_state_disconnecting:
                wprintf(L"Disconnecting\n");
                break;
            case wlan_interface_state_disconnected:
                wprintf(L"Not connected\n");
                break;
            case wlan_interface_state_associating:
                wprintf(L"Attempting to associate with a network\n");
                break;
            case wlan_interface_state_discovering:
                wprintf(L"Auto configuration is discovering settings for the network\n");
                break;
            case wlan_interface_state_authenticating:
                wprintf(L"In process of authenticating\n");
                break;
            default:
                wprintf(L"Unknown state %ld\n", pIfInfo->isState);
                break;
            }
            wprintf(L"\n\n");

            dwResult = WlanGetProfile(hClient,
                                             &pIfInfo->InterfaceGuid,
                                             pProfileName,
                                             NULL, 
                                             &pProfileXml,
                                             &dwFlags,
                                             &dwGrantedAccess);

            if (dwResult != ERROR_SUCCESS) {
                wprintf(L"WlanGetProfile failed with error: %u\n",
                        dwResult);
                // You can use FormatMessage to find out why the function failed
            } else {
                wprintf(L"  Profile Name:  %ws\n", pProfileName);

                wprintf(L"  Profile XML string:\n");
                wprintf(L"%ws\n\n", pProfileXml);

                wprintf(L"  dwFlags:\t    0x%x", dwFlags);
//                    if (dwFlags & WLAN_PROFILE_GET_PLAINTEXT_KEY)
//                        wprintf(L"   Get Plain Text Key");
                    if (dwFlags & WLAN_PROFILE_GROUP_POLICY)
                        wprintf(L"  Group Policy");
                    if (dwFlags & WLAN_PROFILE_USER)
                        wprintf(L"  Per User Profile");
                    wprintf(L"\n");    

                wprintf(L"  dwGrantedAccess:  0x%x", dwGrantedAccess);
                if (dwGrantedAccess & WLAN_READ_ACCESS)
                    wprintf(L"  Read access");
                if (dwGrantedAccess & WLAN_EXECUTE_ACCESS)
                    wprintf(L"  Execute access");
                if (dwGrantedAccess & WLAN_WRITE_ACCESS)
                    wprintf(L"  Write access");
                wprintf(L"\n");    

                wprintf(L"\n");
            }
        }

    }
    if (pProfileXml != NULL) {
        WlanFreeMemory(pProfileXml);
        pProfileXml = NULL;
    }

    if (pIfList != NULL) {
        WlanFreeMemory(pIfList);
        pIfList = NULL;
    }

    return dwRetVal;
}

```

## -see-also

<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_profile_info">WLAN_PROFILE_INFO</a>



<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_profile_info_list">WLAN_PROFILE_INFO_LIST</a>



<a href="/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object">WLAN_SECURABLE_OBJECT</a>



<a href="/windows/desktop/NativeWiFi/wlan-policyschema-schema">WLAN_profile Schema</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile">WlanDeleteProfile</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces">WlanEnumInterfaces</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory">WlanFreeMemory</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilecustomuserdata">WlanGetProfileCustomUserData</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilelist">WlanGetProfileList</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanrenameprofile">WlanRenameProfile</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansavetemporaryprofile">WlanSaveTemporaryProfile</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile">WlanSetProfile</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilecustomuserdata">WlanSetProfileCustomUserData</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileeapuserdata">WlanSetProfileEapUserData</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileeapxmluserdata">WlanSetProfileEapXmlUserData</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist">WlanSetProfileList</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition">WlanSetProfilePosition</a>