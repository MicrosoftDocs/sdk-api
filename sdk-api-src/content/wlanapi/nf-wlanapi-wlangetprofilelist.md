---
UID: NF:wlanapi.WlanGetProfileList
title: WlanGetProfileList function (wlanapi.h)
description: Retrieves the list of profiles.
helpviewer_keywords: ["WlanGetProfileList","WlanGetProfileList function [NativeWIFI]","nwifi.wlangetprofilelist","wlanapi/WlanGetProfileList"]
old-location: nwifi\wlangetprofilelist.htm
tech.root: nwifi
ms.assetid: f4336113-538f-4161-a71f-64a432e31f1c
ms.date: 12/05/2018
ms.keywords: WlanGetProfileList, WlanGetProfileList function [NativeWIFI], nwifi.wlangetprofilelist, wlanapi/WlanGetProfileList
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
 - WlanGetProfileList
 - wlanapi/WlanGetProfileList
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
 - WlanGetProfileList
---

# WlanGetProfileList function


## -description

The <b>WlanGetProfileList</b> function retrieves the list of profiles in preference order.

## -parameters

### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param pInterfaceGuid [in]

The GUID of the wireless interface. 

A list of the GUIDs for wireless interfaces on the local computer can be retrieved using the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces">WlanEnumInterfaces</a> function.

### -param pReserved [in]

Reserved for future use.  Must be set to <b>NULL</b>.

### -param ppProfileList [out]

A <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_profile_info_list">PWLAN_PROFILE_INFO_LIST</a> structure that contains the list of profile information.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is incorrect. This error is returned if any of the following conditions occur:<ul>
<li><i>hClientHandle</i> is <b>NULL</b>.</li>
<li><i>pInterfaceGuid</i> is <b>NULL</b>.</li>
<li><i>ppProfileList</i>  is <b>NULL</b>.</li>
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
Not enough memory is available to process this request and allocate memory for the query results.

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

The <b>WlanGetProfileList</b> function returns only the basic information on the wireless profiles on a wireless interface. The list of wireless profiles   on a wireless interface are retrieved in the preference order. The <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition">WlanSetProfilePosition</a> can be used to change the preference order for the wireless profiles on a wireless interface.

More detailed information for a wireless profile on a wireless interface can be retrieved by using the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile">WlanGetProfile</a> function. The <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilecustomuserdata">WlanGetProfileCustomUserData</a> function can be used to retrieve custom user data for a wireless profile on a wireless interface. A list of the wireless interfaces and associated GUIDs on the local computer can be retrieved using the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces">WlanEnumInterfaces</a> function.

The  <b>WlanGetProfileList</b> function allocates memory for the list of profiles returned in the buffer pointed to by the <i>ppProfileList</i> parameter. The caller is responsible for freeing this memory using the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory">WlanFreeMemory</a> function when this buffer is no longer needed.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>Guest profiles, profiles with Wireless Provisioning Service (WPS) authentication, and profiles with Wi-Fi Protected Access-None (WPA-None)  authentication are not supported. These types of profiles are not returned by <b>WlanGetProfileList</b>, even if a profile of this type appears on the preferred profile list.


#### Examples

The following example enumerates the wireless LAN interfaces on the local computer, retrieves the list of profiles on each wireless LAN interface, and prints values from the retrieved <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_profile_info_list">WLAN_PROFILE_INFO_LIST</a> that contains the <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_profile_info">WLAN_PROFILE_INFO</a> entries.

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


int wmain()
{

    // Declare and initialize variables.

    HANDLE hClient = NULL;
    DWORD dwMaxClient = 2;      //    
    DWORD dwCurVersion = 0;
    DWORD dwResult = 0;
    DWORD dwRetVal = 0;
    int iRet = 0;
    
    WCHAR GuidString[39] = {0};

    unsigned int i, j;

    /* variables used for WlanEnumInterfaces  */

    PWLAN_INTERFACE_INFO_LIST pIfList = NULL;
    PWLAN_INTERFACE_INFO pIfInfo = NULL;

    PWLAN_PROFILE_INFO_LIST pProfileList = NULL;
    PWLAN_PROFILE_INFO pProfile = NULL;

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
        wprintf(L"Current Index: %lu\n", pIfList->dwIndex);
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
                wprintf(L"  Interface GUID[%d]: %ws\n",i, GuidString);
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
            wprintf(L"\n");

            dwResult = WlanGetProfileList(hClient,
                                             &pIfInfo->InterfaceGuid,
                                             NULL, 
                                             &pProfileList);

            if (dwResult != ERROR_SUCCESS) {
                wprintf(L"WlanGetProfileList failed with error: %u\n",
                        dwResult);
                dwRetVal = 1;
                // You can use FormatMessage to find out why the function failed
            } else {
                wprintf(L"WLAN_PROFILE_INFO_LIST for this interface\n");

                wprintf(L"  Num Entries: %lu\n\n", pProfileList->dwNumberOfItems);

                for (j = 0; j < pProfileList->dwNumberOfItems; j++) {
                    pProfile =
                        (WLAN_PROFILE_INFO *) & pProfileList->ProfileInfo[j];

                    wprintf(L"  Profile Name[%u]:  %ws\n", j, pProfile->strProfileName);
                    
                    wprintf(L"  Flags[%u]:\t    0x%x", j, pProfile->dwFlags);
                    if (pProfile->dwFlags & WLAN_PROFILE_GROUP_POLICY)
                        wprintf(L"   Group Policy");
                    if (pProfile->dwFlags & WLAN_PROFILE_USER)
                        wprintf(L"   Per User Profile");
                    wprintf(L"\n");    

                    wprintf(L"\n");
                }
            }
        }

    }
    if (pProfileList != NULL) {
        WlanFreeMemory(pProfileList);
        pProfileList = NULL;
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



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile">WlanDeleteProfile</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory">WlanFreeMemory</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile">WlanGetProfile</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilecustomuserdata">WlanGetProfileCustomUserData</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanrenameprofile">WlanRenameProfile</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansavetemporaryprofile">WlanSaveTemporaryProfile</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile">WlanSetProfile</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilecustomuserdata">WlanSetProfileCustomUserData</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileeapuserdata">WlanSetProfileEapUserData</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileeapxmluserdata">WlanSetProfileEapXmlUserData</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist">WlanSetProfileList</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition">WlanSetProfilePosition</a>