---
UID: NF:wlanapi.WlanGetAvailableNetworkList
title: WlanGetAvailableNetworkList function (wlanapi.h)
description: Retrieves the list of available networks on a wireless LAN interface.
helpviewer_keywords: ["WLAN_AVAILABLE_NETWORK_INCLUDE_ALL_ADHOC_PROFILES","WLAN_AVAILABLE_NETWORK_INCLUDE_ALL_MANUAL_HIDDEN_PROFILES","WlanGetAvailableNetworkList","WlanGetAvailableNetworkList function [NativeWIFI]","nwifi.wlangetavailablenetworklist","nwifi.wlangetvisiblenetworklist","wlanapi/WlanGetAvailableNetworkList"]
old-location: nwifi\wlangetavailablenetworklist.htm
tech.root: nwifi
ms.assetid: 27353a1b-2a3c-4c3b-b512-917d010ee8dd
ms.date: 12/05/2018
ms.keywords: WLAN_AVAILABLE_NETWORK_INCLUDE_ALL_ADHOC_PROFILES, WLAN_AVAILABLE_NETWORK_INCLUDE_ALL_MANUAL_HIDDEN_PROFILES, WlanGetAvailableNetworkList, WlanGetAvailableNetworkList function [NativeWIFI], nwifi.wlangetavailablenetworklist, nwifi.wlangetvisiblenetworklist, wlanapi/WlanGetAvailableNetworkList
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
 - WlanGetAvailableNetworkList
 - wlanapi/WlanGetAvailableNetworkList
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
 - WlanGetAvailableNetworkList
---

# WlanGetAvailableNetworkList function

## -description

> [!NOTE]
> **Some information relates to pre-released product, which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.**

> [!IMPORTANT]
> This API will be affected by upcoming changes to operating system behavior, planned for fall 2024. For more info, see [Changes to API behavior for Wi-Fi access and location](/windows/win32/nativewifi/wi-fi-access-location-changes).

The <b>WlanGetAvailableNetworkList</b> function retrieves the list of available networks on a wireless LAN interface.

## -parameters

### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param pInterfaceGuid [in]

A pointer to the GUID of the wireless LAN interface to be queried.

 The GUID of each wireless LAN interface enabled on a local computer can be determined using the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces">WlanEnumInterfaces</a> function.

### -param dwFlags [in]

A set of flags that control the type of networks returned in the list.  This parameter can be a combination of these possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WLAN_AVAILABLE_NETWORK_INCLUDE_ALL_ADHOC_PROFILES"></a><a id="wlan_available_network_include_all_adhoc_profiles"></a><dl>
<dt><b>WLAN_AVAILABLE_NETWORK_INCLUDE_ALL_ADHOC_PROFILES</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Include all ad hoc network profiles in the available network list, including profiles that are not visible.

<div class="alert"><b>Note</b>  If this flag is specified on Windows XP with SP3 and Wireless LAN API for Windows XP with SP2, it is consider considered an invalid parameter.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="WLAN_AVAILABLE_NETWORK_INCLUDE_ALL_MANUAL_HIDDEN_PROFILES"></a><a id="wlan_available_network_include_all_manual_hidden_profiles"></a><dl>
<dt><b>WLAN_AVAILABLE_NETWORK_INCLUDE_ALL_MANUAL_HIDDEN_PROFILES</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Include all hidden network profiles in the available network list, including profiles that are not visible.

<div class="alert"><b>Note</b>  If this flag is specified on Windows XP with SP3 and Wireless LAN API for Windows XP with SP2, it is consider considered an invalid parameter.</div>
<div> </div>
</td>
</tr>
</table>

### -param pReserved

Reserved for future use.  This parameter must be set to <b>NULL</b>.

### -param ppAvailableNetworkList [out]

A pointer to storage for a pointer to receive the returned list of visible networks in a <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network_list">WLAN_AVAILABLE_NETWORK_LIST</a> structure.

The buffer for the <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network_list">WLAN_AVAILABLE_NETWORK_LIST</a> returned is allocated by the <b>WlanGetAvailableNetworkList</b> function if the call succeeds.

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
A parameter is incorrect. This error is returned if the <i>hClientHandle</i>,  <i>pInterfaceGuid</i>, or <i>ppAvailableNetworkList</i> parameter is <b>NULL</b>. This error is returned if the <i>pReserved</i> is not <b>NULL</b>. This error is also returned if the <i>dwFlags</i> parameter value is set to value that is not valid or the <i>hClientHandle</i> parameter is not valid.

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
<dt><b>ERROR_NDIS_DOT11_POWER_STATE_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The radio associated with the interface is turned off. There are no available networks when the radio is off. 

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
</table>

## -remarks

The <b>WlanGetAvailableNetworkList</b> function allocates memory for the list of available networks returned in the buffer pointed to by the <i>ppAvailableNetworkList</i> parameter when the function succeeds. The memory used for the buffer pointed to by <i>ppAvailableNetworkList</i> parameter should be released by calling the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory">WlanFreeMemory</a> function after the buffer is no longer needed.


There is a hotfix available for  Wireless LAN API for Windows XP with SP2 that can help improve the performance of applications that call <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory">WlanFreeMemory</a> and <b>WlanGetAvailableNetworkList</b> many times. 


#### Examples

The following example enumerates the wireless LAN interfaces on the local computer, retrieves the list of available networks on each wireless LAN interface, and prints values from the retrieved <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network_list">WLAN_AVAILABLE_NETWORK_LIST</a> that contains the <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network">WLAN_AVAILABLE_NETWORK</a> entries.

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

    unsigned int i, j, k;

    /* variables used for WlanEnumInterfaces  */

    PWLAN_INTERFACE_INFO_LIST pIfList = NULL;
    PWLAN_INTERFACE_INFO pIfInfo = NULL;

    PWLAN_AVAILABLE_NETWORK_LIST pBssList = NULL;
    PWLAN_AVAILABLE_NETWORK pBssEntry = NULL;
    
    int iRSSI = 0;

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
            wprintf(L"\n");

            dwResult = WlanGetAvailableNetworkList(hClient,
                                             &pIfInfo->InterfaceGuid,
                                             0, 
                                             NULL, 
                                             &pBssList);

            if (dwResult != ERROR_SUCCESS) {
                wprintf(L"WlanGetAvailableNetworkList failed with error: %u\n",
                        dwResult);
                dwRetVal = 1;
                // You can use FormatMessage to find out why the function failed
            } else {
                wprintf(L"WLAN_AVAILABLE_NETWORK_LIST for this interface\n");

                wprintf(L"  Num Entries: %lu\n\n", pBssList->dwNumberOfItems);

                for (j = 0; j < pBssList->dwNumberOfItems; j++) {
                    pBssEntry =
                        (WLAN_AVAILABLE_NETWORK *) & pBssList->Network[j];

                    wprintf(L"  Profile Name[%u]:  %ws\n", j, pBssEntry->strProfileName);
                    
                    wprintf(L"  SSID[%u]:\t\t ", j);
                    if (pBssEntry->dot11Ssid.uSSIDLength == 0)
                        wprintf(L"\n");
                    else {   
                        for (k = 0; k < pBssEntry->dot11Ssid.uSSIDLength; k++) {
                            wprintf(L"%c", (int) pBssEntry->dot11Ssid.ucSSID[k]);
                        }
                        wprintf(L"\n");
                    }
                        
                    wprintf(L"  BSS Network type[%u]:\t ", j);
                    switch (pBssEntry->dot11BssType) {
                    case dot11_BSS_type_infrastructure   :
                        wprintf(L"Infrastructure (%u)\n", pBssEntry->dot11BssType);
                        break;
                    case dot11_BSS_type_independent:
                        wprintf(L"Infrastructure (%u)\n", pBssEntry->dot11BssType);
                        break;
                    default:
                        wprintf(L"Other (%lu)\n", pBssEntry->dot11BssType);
                        break;
                    }
                                
                    wprintf(L"  Number of BSSIDs[%u]:\t %u\n", j, pBssEntry->uNumberOfBssids);

                    wprintf(L"  Connectable[%u]:\t ", j);
                    if (pBssEntry->bNetworkConnectable)
                        wprintf(L"Yes\n");
                    else {
                        wprintf(L"No\n");
                        wprintf(L"  Not connectable WLAN_REASON_CODE value[%u]:\t %u\n", j, 
                            pBssEntry->wlanNotConnectableReason);
                    }        

                    wprintf(L"  Number of PHY types supported[%u]:\t %u\n", j, pBssEntry->uNumberOfPhyTypes);

                    if (pBssEntry->wlanSignalQuality == 0)
                        iRSSI = -100;
                    else if (pBssEntry->wlanSignalQuality == 100)   
                        iRSSI = -50;
                    else
                        iRSSI = -100 + (pBssEntry->wlanSignalQuality/2);    
                        
                    wprintf(L"  Signal Quality[%u]:\t %u (RSSI: %i dBm)\n", j, 
                        pBssEntry->wlanSignalQuality, iRSSI);

                    wprintf(L"  Security Enabled[%u]:\t ", j);
                    if (pBssEntry->bSecurityEnabled)
                        wprintf(L"Yes\n");
                    else
                        wprintf(L"No\n");
                        
                    wprintf(L"  Default AuthAlgorithm[%u]: ", j);
                    switch (pBssEntry->dot11DefaultAuthAlgorithm) {
                    case DOT11_AUTH_ALGO_80211_OPEN:
                        wprintf(L"802.11 Open (%u)\n", pBssEntry->dot11DefaultAuthAlgorithm);
                        break;
                    case DOT11_AUTH_ALGO_80211_SHARED_KEY:
                        wprintf(L"802.11 Shared (%u)\n", pBssEntry->dot11DefaultAuthAlgorithm);
                        break;
                    case DOT11_AUTH_ALGO_WPA:
                        wprintf(L"WPA (%u)\n", pBssEntry->dot11DefaultAuthAlgorithm);
                        break;
                    case DOT11_AUTH_ALGO_WPA_PSK:
                        wprintf(L"WPA-PSK (%u)\n", pBssEntry->dot11DefaultAuthAlgorithm);
                        break;
                    case DOT11_AUTH_ALGO_WPA_NONE:
                        wprintf(L"WPA-None (%u)\n", pBssEntry->dot11DefaultAuthAlgorithm);
                        break;
                    case DOT11_AUTH_ALGO_RSNA:
                        wprintf(L"RSNA (%u)\n", pBssEntry->dot11DefaultAuthAlgorithm);
                        break;
                    case DOT11_AUTH_ALGO_RSNA_PSK:
                        wprintf(L"RSNA with PSK(%u)\n", pBssEntry->dot11DefaultAuthAlgorithm);
                        break;
                    default:
                        wprintf(L"Other (%lu)\n", pBssEntry->dot11DefaultAuthAlgorithm);
                        break;
                    }
                        
                    wprintf(L"  Default CipherAlgorithm[%u]: ", j);
                    switch (pBssEntry->dot11DefaultCipherAlgorithm) {
                    case DOT11_CIPHER_ALGO_NONE:
                        wprintf(L"None (0x%x)\n", pBssEntry->dot11DefaultCipherAlgorithm);
                        break;
                    case DOT11_CIPHER_ALGO_WEP40:
                        wprintf(L"WEP-40 (0x%x)\n", pBssEntry->dot11DefaultCipherAlgorithm);
                        break;
                    case DOT11_CIPHER_ALGO_TKIP:
                        wprintf(L"TKIP (0x%x)\n", pBssEntry->dot11DefaultCipherAlgorithm);
                        break;
                    case DOT11_CIPHER_ALGO_CCMP:
                        wprintf(L"CCMP (0x%x)\n", pBssEntry->dot11DefaultCipherAlgorithm);
                        break;
                    case DOT11_CIPHER_ALGO_WEP104:
                        wprintf(L"WEP-104 (0x%x)\n", pBssEntry->dot11DefaultCipherAlgorithm);
                        break;
                    case DOT11_CIPHER_ALGO_WEP:
                        wprintf(L"WEP (0x%x)\n", pBssEntry->dot11DefaultCipherAlgorithm);
                        break;
                    default:
                        wprintf(L"Other (0x%x)\n", pBssEntry->dot11DefaultCipherAlgorithm);
                        break;
                    }

                    wprintf(L"  Flags[%u]:\t 0x%x", j, pBssEntry->dwFlags);
                    if (pBssEntry->dwFlags) {
                        if (pBssEntry->dwFlags & WLAN_AVAILABLE_NETWORK_CONNECTED)
                            wprintf(L" - Currently connected");
                        if (pBssEntry->dwFlags & WLAN_AVAILABLE_NETWORK_HAS_PROFILE)
                            wprintf(L" - Has profile");
                    }   
                    wprintf(L"\n");
                    
                    wprintf(L"\n");
                }
            }
        }

    }
    if (pBssList != NULL) {
        WlanFreeMemory(pBssList);
        pBssList = NULL;
    }

    if (pIfList != NULL) {
        WlanFreeMemory(pIfList);
        pIfList = NULL;
    }

    return dwRetVal;
}

```

## -see-also

<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network">WLAN_AVAILABLE_NETWORK</a>



<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network_list">WLAN_AVAILABLE_NETWORK_LIST</a>



<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry">WLAN_BSS_ENTRY</a>



<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_list">WLAN_BSS_LIST</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces">WlanEnumInterfaces</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory">WlanFreeMemory</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetnetworkbsslist">WlanGetNetworkBssList</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan">WlanScan</a>