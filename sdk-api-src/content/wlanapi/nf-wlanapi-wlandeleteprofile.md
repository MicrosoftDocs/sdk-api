---
UID: NF:wlanapi.WlanDeleteProfile
title: WlanDeleteProfile function (wlanapi.h)
description: Deletes a wireless profile for a wireless interface on the local computer.
helpviewer_keywords: ["WlanDeleteProfile","WlanDeleteProfile function [NativeWIFI]","nwifi.wlandeleteprofile","wlanapi/WlanDeleteProfile"]
old-location: nwifi\wlandeleteprofile.htm
tech.root: nwifi
ms.assetid: 2d1152ad-8106-4b8f-9856-9e6e36daa063
ms.date: 12/05/2018
ms.keywords: WlanDeleteProfile, WlanDeleteProfile function [NativeWIFI], nwifi.wlandeleteprofile, wlanapi/WlanDeleteProfile
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
 - WlanDeleteProfile
 - wlanapi/WlanDeleteProfile
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
 - WlanDeleteProfile
---

# WlanDeleteProfile function


## -description

The <b>WlanDeleteProfile</b> function deletes a wireless profile for a wireless interface on  the local computer.

## -parameters

### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param pInterfaceGuid [in]

The GUID of the interface from which to delete the profile.

### -param strProfileName [in]

The name of the profile to be deleted. Profile names are case-sensitive. This string must be NULL-terminated.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>The supplied name must match the profile name derived automatically from the SSID of the network. For an infrastructure network profile, the SSID must be supplied for the profile name. For an ad hoc network profile, the supplied name must be the SSID of the ad hoc network followed by <code>-adhoc</code>.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>hClientHandle</i> parameter is <b>NULL</b> or  not valid,  the <i>pInterfaceGuid</i> parameter is <b>NULL</b>, the <i>strProfileName</i> parameter is <b>NULL</b>, or <i>pReserved</i> is not <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle specified in the <i>hClientHandle</i>  parameter was not found in the handle table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The wireless profile specified by <i>strProfileName</i> was not found in the profile store.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient permissions to delete the profile. 

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

The <b>WlanDeleteProfile</b> function deletes a wireless profile for a wireless interface on  the local computer. 

All wireless LAN functions require an interface GUID for the wireless interface when performing profile operations. When a wireless interface is removed, its state is cleared from Wireless LAN Service (WLANSVC)  and no profile operations are possible.

The <b>WlanDeleteProfile</b> function can fail with <b>ERROR_INVALID_PARAMETER</b> if the wireless interface specified in the <i>pInterfaceGuid</i> parameter for the wireless LAN profile has been removed from the system (a USB  wireless adapter that has been removed, for example). 

To delete a profile at the command line, use the <b>netsh wlan delete profile</b> command. For more information, see <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)">Netsh Commands for Wireless Local Area Network (wlan)</a>. 


#### Examples

The following example enumerates the wireless LAN interfaces on the local computer and tries to delete a specific wireless profile on each wireless LAN interface. 

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

int _cdecl wmain(int argc, WCHAR ** argv)
{

    // Declare and initialize variables.

    HANDLE hClient = NULL;
    DWORD dwMaxClient = 2;      //    
    DWORD dwCurVersion = 0;
    DWORD dwResult = 0;
    DWORD dwRetVal = 0;
    int iRet = 0;

    WCHAR GuidString[39] = { 0 };

    unsigned int i;

    /* variables used for WlanEnumInterfaces  */

    PWLAN_INTERFACE_INFO_LIST pIfList = NULL;
    PWLAN_INTERFACE_INFO pIfInfo = NULL;

    LPCWSTR pProfileName = NULL;

    // Validate the parameters
    if (argc < 2) {
        wprintf(L"usage: %s <profile>\n", argv[0]);
        wprintf(L"   Deletes a wireless profile\n");
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
        wprintf(L"Current Index: %lu\n", pIfList->dwIndex);
        for (i = 0; i < pIfList->dwNumberOfItems; i++) {
            pIfInfo = (WLAN_INTERFACE_INFO *) & pIfList->InterfaceInfo[i];
            wprintf(L"  Interface Index[%u]:\t %lu\n", i, i);
            iRet =
                StringFromGUID2(pIfInfo->InterfaceGuid, (LPOLESTR) & GuidString,
                                sizeof (GuidString) / sizeof (*GuidString));
            // For c rather than C++ source code, the above line needs to be
            // iRet = StringFromGUID2(&pIfInfo->InterfaceGuid, (LPOLESTR) &GuidString, 
            //     sizeof(GuidString)/sizeof(*GuidString)); 
            if (iRet == 0)
                wprintf(L"StringFromGUID2 failed\n");
            else {
                wprintf(L"  InterfaceGUID[%d]: %ws\n", i, GuidString);
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
                wprintf
                    (L"Auto configuration is discovering settings for the network\n");
                break;
            case wlan_interface_state_authenticating:
                wprintf(L"In process of authenticating\n");
                break;
            default:
                wprintf(L"Unknown state %ld\n", pIfInfo->isState);
                break;
            }
            wprintf(L"\n");

            dwResult = WlanDeleteProfile(hClient,
                                         &pIfInfo->InterfaceGuid,
                                         pProfileName, NULL);

            if (dwResult != ERROR_SUCCESS) {
                wprintf
                    (L"WlanDeleteProfile failed on this interface with error: %u\n",
                     dwResult);
                if (dwResult == ERROR_NOT_FOUND)
                    wprintf
                        (L"  Error was the following profile was not found: %ws\n",
                         pProfileName);
                // You can use FormatMessage to find out why the function failed
            } else {
                wprintf(L"Successfully deleted Profile Name: %ws\n",
                        pProfileName);
            }
            wprintf(L"\n");
        }

    }
    if (pIfList != NULL) {
        WlanFreeMemory(pIfList);
        pIfList = NULL;
    }

    return dwRetVal;
}


```

## -see-also

<a href="/windows/desktop/NativeWiFi/native-wifi-api-permissions">Native Wifi API Permissions</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile">WlanGetProfile</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilelist">WlanGetProfileList</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanrenameprofile">WlanRenameProfile</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile">WlanSetProfile</a>