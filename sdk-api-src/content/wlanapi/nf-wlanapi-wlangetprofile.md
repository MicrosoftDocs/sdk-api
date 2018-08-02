---
UID: NF:wlanapi.WlanGetProfile
title: WlanGetProfile function
author: windows-sdk-content
description: Retrieves all information about a specified wireless profile.
old-location: nwifi\wlangetprofile.htm
old-project: NativeWiFi
ms.assetid: 6486e961-402f-45c8-a806-ab91a4f0f156
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WLAN_PROFILE_GET_PLAINTEXT_KEY, WLAN_PROFILE_GROUP_POLICY, WLAN_PROFILE_USER, WlanGetProfile, WlanGetProfile function [NativeWIFI], nwifi.wlangetprofile, wlanapi/WlanGetProfile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: WL_DISPLAY_PAGES, *PWL_DISPLAY_PAGES
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
product: Windows
targetos: Windows
req.lib: Wlanapi.lib
req.dll: Wlanapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WlanGetProfile function


## -description


The <b>WlanGetProfile</b> function retrieves all information about a  specified wireless profile.


## -parameters




### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="https://msdn.microsoft.com/27bfa0c1-4443-47a4-a374-326f553fa3bb">WlanOpenHandle</a> function.


### -param pInterfaceGuid [in]

The GUID of the wireless interface. 

A list of the GUIDs for wireless interfaces on the local computer can be retrieved using the <a href="https://msdn.microsoft.com/7f817edf-1b1d-495c-afd9-d97e3ae0caab">WlanEnumInterfaces</a> function.


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
On input, this flag indicates that the caller wants to retrieve the plain text key from a wireless profile. If the calling thread has the required permissions, the  <b>WlanGetProfile</b> function returns the plain text key in the <a href="https://msdn.microsoft.com/d2ed407e-5eaa-477b-8c4d-a47795048e0b">keyMaterial</a> element of the profile returned in the buffer pointed to by the   <i>pstrProfileXml</i> parameter.

For the <b>WlanGetProfile</b> call to return the plain text key, the <b>wlan_secure_get_plaintext_key</b> permissions from the <a href="https://msdn.microsoft.com/1f6e1460-d27f-4800-8a32-6f9f509753cf">WLAN_SECURABLE_OBJECT</a> enumerated type must be set on the calling thread. The DACL must also contain an ACE that grants <b>WLAN_READ_ACCESS</b> permission to the access token of the calling thread. By default,  the permissions for retrieving the plain text key is allowed only to the members of the Administrators group on a local machine.



If the calling thread lacks the required permissions, the <b>WlanGetProfile</b> function returns the encrypted key in the <a href="https://msdn.microsoft.com/d2ed407e-5eaa-477b-8c4d-a47795048e0b">keyMaterial</a> element of the profile returned in the buffer pointed to by the   <i>pstrProfileXml</i> parameter. No error is returned if the calling thread lacks the required permissions. 

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
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.


</td>
</tr>
</table>
 




## -remarks



If the <b>WlanGetProfile</b> function succeeds, the wireless profile is returned in the buffer pointed to by the <i>pstrProfileXml</i> parameter. The buffer contains a string that is the XML representation of the queried profile. For a description of the XML representation of the wireless profile, see <a href="https://msdn.microsoft.com/b983df2e-95cf-41ce-929e-2bc560854f21">WLAN_profile Schema</a>. 

The caller is responsible for calling the <a href="https://msdn.microsoft.com/241afb9d-8b16-4d76-b311-302b5492853e">WlanFreeMemory</a> function to free the memory allocated for the buffer pointer to by the <i>pstrProfileXml</i> parameter when the buffer is no longer needed.

If <i>pstrProfileXml</i> specifies an all-user profile, the <b>WlanGetProfile</b>  caller must have read access on the profile. Otherwise, the <b>WlanGetProfile</b> call will fail with a return value of <b>ERROR_ACCESS_DENIED</b>. The permissions on an all-user profile are established when the profile is created or saved using <a href="https://msdn.microsoft.com/3f8dca2e-6fe5-4c7d-a135-a33c61ba3dd5">WlanSetProfile</a> or <a href="https://msdn.microsoft.com/e409fd30-eddd-4cc7-acb7-35af6ef51a10">WlanSaveTemporaryProfile</a>.

<b>Windows 7:  </b><p class="note">The <a href="https://msdn.microsoft.com/d2ed407e-5eaa-477b-8c4d-a47795048e0b">keyMaterial</a> element returned in the profile schema pointed to by the <i>pstrProfileXml</i> may be requested as plaintext if the <b>WlanGetProfile</b> function is called with the <b>WLAN_PROFILE_GET_PLAINTEXT_KEY</b>  flag set in the value pointed to by the <i>pdwFlags</i> parameter on input.   

<p class="note">For a WEP key, both 5 ASCII characters or 10 hexadecimal characters can be used to set the plaintext key when the profile is created or updated. However, a WEP profile will be saved with  10 hexadecimal characters in the key no matter what the original input was used to create the profile. So in the profile returned by the  <b>WlanGetProfile</b> function, the plaintext WEP key  is always returned as 10 hexadecimal characters.


<p class="note">For the <b>WlanGetProfile</b> call to return the plain text key, the <b>wlan_secure_get_plaintext_key</b> permissions from the <a href="https://msdn.microsoft.com/1f6e1460-d27f-4800-8a32-6f9f509753cf">WLAN_SECURABLE_OBJECT</a> enumerated type must be set on the calling thread. The DACL must also contain an ACE that grants <b>WLAN_READ_ACCESS</b> permission to the access token of the calling thread. By default,  the permissions for retrieving the plain text key is allowed only to the members of the Administrators group on a local machine.



<p class="note">If the calling thread lacks the required permissions, the <b>WlanGetProfile</b> function returns the encrypted key in the <a href="https://msdn.microsoft.com/d2ed407e-5eaa-477b-8c4d-a47795048e0b">keyMaterial</a> element of the profile returned in the buffer pointed to by the   <i>pstrProfileXml</i> parameter. No error is returned if the calling thread lacks the required permissions. 

<p class="note">By default, the <a href="https://msdn.microsoft.com/d2ed407e-5eaa-477b-8c4d-a47795048e0b">keyMaterial</a> element returned in the profile pointed to by the <i>pstrProfileXml</i> is encrypted.   If your process runs in the context of the LocalSystem account on the same computer, then you can unencrypt key material by calling the <a href="https://msdn.microsoft.com/54eab3b0-d341-47c6-9c32-79328d7a7155">CryptUnprotectData</a> function. 



<b>Windows Server 2008 and Windows Vista:  </b>The <a href="https://msdn.microsoft.com/d2ed407e-5eaa-477b-8c4d-a47795048e0b">keyMaterial</a> element returned in the profile schema pointed to by the <i>pstrProfileXml</i> is always encrypted.  If your process runs in the context of the LocalSystem account, then you can unencrypt key material by calling the <a href="https://msdn.microsoft.com/54eab3b0-d341-47c6-9c32-79328d7a7155">CryptUnprotectData</a> function.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>The key material is never encrypted.


#### Examples

The following example enumerates the wireless LAN interfaces on the local computer, retrieves information for a specific wireless profile on each wireless LAN interface, and prints the values retrieved. The string that is the XML representation of the queried profile is also printed.

<div class="alert"><b>Note</b>  This example will fail to load on Windows Server 2008 and Windows Server 2008 R2 if the Wireless LAN Service is not installed and started.</div>
<div> </div>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#ifndef UNICODE
#define UNICODE
#endif

#include &lt;windows.h&gt;
#include &lt;wlanapi.h&gt;
#include &lt;objbase.h&gt;
#include &lt;wtypes.h&gt;

#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;

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
    if (argc &lt; 2) {
        wprintf(L"usage: %s &lt;profile&gt;\n", argv[0]);
        wprintf(L"   Gets a wireless profile\n");
        wprintf(L"   Example\n");
        wprintf(L"       %s \"Default Wireless\"\n", argv[0]);
        exit(1);
    }
    
    pProfileName = argv[1];
     
    wprintf(L"Information for profile: %ws\n\n", pProfileName);
    
    dwResult = WlanOpenHandle(dwMaxClient, NULL, &amp;dwCurVersion, &amp;hClient);
    if (dwResult != ERROR_SUCCESS) {
        wprintf(L"WlanOpenHandle failed with error: %u\n", dwResult);
        return 1;
        // You can use FormatMessage here to find out why the function failed
    }

    dwResult = WlanEnumInterfaces(hClient, NULL, &amp;pIfList);
    if (dwResult != ERROR_SUCCESS) {
        wprintf(L"WlanEnumInterfaces failed with error: %u\n", dwResult);
        return 1;
        // You can use FormatMessage here to find out why the function failed
    } else {
        wprintf(L"WLAN_INTERFACE_INFO_LIST for this system\n");

        wprintf(L"Num Entries: %lu\n", pIfList-&gt;dwNumberOfItems);
        wprintf(L"Current Index: %lu\n\n", pIfList-&gt;dwIndex);
        for (i = 0; i &lt; (int) pIfList-&gt;dwNumberOfItems; i++) {
            pIfInfo = (WLAN_INTERFACE_INFO *) &amp;pIfList-&gt;InterfaceInfo[i];
            wprintf(L"  Interface Index[%u]:\t %lu\n", i, i);
            iRet = StringFromGUID2(pIfInfo-&gt;InterfaceGuid, (LPOLESTR) &amp;GuidString, 
                sizeof(GuidString)/sizeof(*GuidString)); 
            // For c rather than C++ source code, the above line needs to be
            // iRet = StringFromGUID2(&amp;pIfInfo-&gt;InterfaceGuid, (LPOLESTR) &amp;GuidString, 
            //     sizeof(GuidString)/sizeof(*GuidString)); 
            if (iRet == 0)
                wprintf(L"StringFromGUID2 failed\n");
            else {
                wprintf(L"  InterfaceGUID[%d]: %ws\n",i, GuidString);
            }    
            wprintf(L"  Interface Description[%d]: %ws", i, 
                pIfInfo-&gt;strInterfaceDescription);
            wprintf(L"\n");
            wprintf(L"  Interface State[%d]:\t ", i);
            switch (pIfInfo-&gt;isState) {
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
                wprintf(L"Unknown state %ld\n", pIfInfo-&gt;isState);
                break;
            }
            wprintf(L"\n\n");

            dwResult = WlanGetProfile(hClient,
                                             &amp;pIfInfo-&gt;InterfaceGuid,
                                             pProfileName,
                                             NULL, 
                                             &amp;pProfileXml,
                                             &amp;dwFlags,
                                             &amp;dwGrantedAccess);

            if (dwResult != ERROR_SUCCESS) {
                wprintf(L"WlanGetProfile failed with error: %u\n",
                        dwResult);
                // You can use FormatMessage to find out why the function failed
            } else {
                wprintf(L"  Profile Name:  %ws\n", pProfileName);

                wprintf(L"  Profile XML string:\n");
                wprintf(L"%ws\n\n", pProfileXml);

                wprintf(L"  dwFlags:\t    0x%x", dwFlags);
//                    if (dwFlags &amp; WLAN_PROFILE_GET_PLAINTEXT_KEY)
//                        wprintf(L"   Get Plain Text Key");
                    if (dwFlags &amp; WLAN_PROFILE_GROUP_POLICY)
                        wprintf(L"  Group Policy");
                    if (dwFlags &amp; WLAN_PROFILE_USER)
                        wprintf(L"  Per User Profile");
                    wprintf(L"\n");    

                wprintf(L"  dwGrantedAccess:  0x%x", dwGrantedAccess);
                if (dwGrantedAccess &amp; WLAN_READ_ACCESS)
                    wprintf(L"  Read access");
                if (dwGrantedAccess &amp; WLAN_EXECUTE_ACCESS)
                    wprintf(L"  Execute access");
                if (dwGrantedAccess &amp; WLAN_WRITE_ACCESS)
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ca45278c-2e1e-4080-825a-d6a05e463858">WLAN_PROFILE_INFO</a>



<a href="https://msdn.microsoft.com/d5a3d475-0ae0-4860-a433-dd916c586f50">WLAN_PROFILE_INFO_LIST</a>



<a href="https://msdn.microsoft.com/1f6e1460-d27f-4800-8a32-6f9f509753cf">WLAN_SECURABLE_OBJECT</a>



<a href="https://msdn.microsoft.com/b983df2e-95cf-41ce-929e-2bc560854f21">WLAN_profile Schema</a>



<a href="https://msdn.microsoft.com/2d1152ad-8106-4b8f-9856-9e6e36daa063">WlanDeleteProfile</a>



<a href="https://msdn.microsoft.com/7f817edf-1b1d-495c-afd9-d97e3ae0caab">WlanEnumInterfaces</a>



<a href="https://msdn.microsoft.com/241afb9d-8b16-4d76-b311-302b5492853e">WlanFreeMemory</a>



<a href="https://msdn.microsoft.com/5973be2f-8267-496b-827b-778f705accdc">WlanGetProfileCustomUserData</a>



<a href="https://msdn.microsoft.com/f4336113-538f-4161-a71f-64a432e31f1c">WlanGetProfileList</a>



<a href="https://msdn.microsoft.com/27bfa0c1-4443-47a4-a374-326f553fa3bb">WlanOpenHandle</a>



<a href="https://msdn.microsoft.com/488e9f87-8b98-48c6-81d5-d7237cdf5bd5">WlanRenameProfile</a>



<a href="https://msdn.microsoft.com/e409fd30-eddd-4cc7-acb7-35af6ef51a10">WlanSaveTemporaryProfile</a>



<a href="https://msdn.microsoft.com/3f8dca2e-6fe5-4c7d-a135-a33c61ba3dd5">WlanSetProfile</a>



<a href="https://msdn.microsoft.com/3b37ff29-4c9b-42c8-b00a-a9dfca1d3fed">WlanSetProfileCustomUserData</a>



<a href="https://msdn.microsoft.com/2bef0f2f-165d-446a-afa8-735658048152">WlanSetProfileEapUserData</a>



<a href="https://msdn.microsoft.com/c34c39c0-8200-438a-8353-238225aea5cb">WlanSetProfileEapXmlUserData</a>



<a href="https://msdn.microsoft.com/980c7920-a25e-4e05-a742-77178a7f000a">WlanSetProfileList</a>



<a href="https://msdn.microsoft.com/06ef9f55-b425-4f61-9b9e-3c27cc3796f6">WlanSetProfilePosition</a>
 

 

