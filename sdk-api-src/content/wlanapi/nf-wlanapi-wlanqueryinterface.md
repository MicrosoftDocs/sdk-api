---
UID: NF:wlanapi.WlanQueryInterface
title: WlanQueryInterface function (wlanapi.h)
description: The WlanQueryInterface function queries various parameters of a specified interface.
helpviewer_keywords: ["WlanQueryInterface","WlanQueryInterface function [NativeWIFI]","nwifi.wlanqueryinterface","wlanapi/WlanQueryInterface"]
old-location: nwifi\wlanqueryinterface.htm
tech.root: nwifi
ms.assetid: e20eb9a3-5824-48ee-b13e-b0252bbf495e
ms.date: 03/18/2024
ms.keywords: WlanQueryInterface, WlanQueryInterface function [NativeWIFI], nwifi.wlanqueryinterface, wlanapi/WlanQueryInterface
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
 - WlanQueryInterface
 - wlanapi/WlanQueryInterface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wlanapi.dll
 - Ext-MS-Win-networking-wlanapi-l1-1-0.dll
api_name:
 - WlanQueryInterface
---

# WlanQueryInterface function

## -description

> [!NOTE]
> **Some information relates to pre-released product, which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.**

> [!IMPORTANT]
> This API will be affected by upcoming changes to operating system behavior, planned for fall 2024. For more info, see [Changes to API behavior for Wi-Fi access and location](/windows/win32/nativewifi/wi-fi-access-location-changes).

The <b>WlanQueryInterface</b> function queries various parameters of a specified interface.

## -parameters

### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="/windows/win32/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param pInterfaceGuid [in]

The GUID of the interface to be queried.

### -param OpCode [in]

A <a href="/windows/win32/api/wlanapi/ne-wlanapi-wlan_intf_opcode">WLAN_INTF_OPCODE</a> value that specifies the parameter to be queried.  The following table lists the valid constants along with the data type of the parameter in <i>ppData</i>.

|WLAN_INTF_OPCODE|*ppData* data type|
|-|-|
|wlan_intf_opcode_autoconf_enabled|BOOL|
|wlan_intf_opcode_background_scan_enabled|BOOL|
|wlan_intf_opcode_bss_type|[DOT11_BSS_TYPE](/windows/win32/NativeWiFi/dot11-bss-type)|
|wlan_intf_opcode_certified_safe_mode|BOOL|
|wlan_intf_opcode_channel_number|ULONG|
|wlan_intf_opcode_current_connection|[WLAN_CONNECTION_ATTRIBUTES](/windows/win32/api/wlanapi/ns-wlanapi-wlan_connection_attributes)|
|wlan_intf_opcode_current_operation_mode|ULONG|
|wlan_intf_opcode_hosted_network_capable|BOOL|
|wlan_intf_opcode_interface_state|[WLAN_INTERFACE_STATE](/windows/win32/api/wlanapi/ne-wlanapi-wlan_interface_state-r1)|
|wlan_intf_opcode_management_frame_protection_capable|BOOL|
|wlan_intf_opcode_media_streaming_mode|BOOL|
|wlan_intf_opcode_qos_info|[WLAN_QOS_INFO](/windows/win32/api/wlanapi/ns-wlanapi-wlan_qos_info)|
|wlan_intf_opcode_radio_state|[WLAN_RADIO_STATE](/windows/win32/api/wlanapi/ns-wlanapi-wlan_radio_state)|
|wlan_intf_opcode_realtime_connection_quality|[WLAN_REALTIME_CONNECTION_QUALITY](/windows/win32/api/wlanapi/ns-wlanapi-wlan_realtime_connection_quality)|
|wlan_intf_opcode_rssi|LONG|
|wlan_intf_opcode_secondary_sta_interfaces|[WLAN_INTERFACE_INFO_LIST](/windows/win32/api/wlanapi/ns-wlanapi-wlan_interface_info_list)|
|wlan_intf_opcode_secondary_sta_synchronized_connections|BOOL|
|wlan_intf_opcode_statistics|[WLAN_STATISTICS](/windows/win32/api/wlanapi/ns-wlanapi-wlan_statistics)|
|wlan_intf_opcode_supported_adhoc_auth_cipher_pairs|[WLAN_AUTH_CIPHER_PAIR_LIST](/windows/win32/api/wlanapi/ns-wlanapi-wlan_auth_cipher_pair_list)|
|wlan_intf_opcode_supported_country_or_region_string_list|[WLAN_COUNTRY_OR_REGION_STRING_LIST](/windows/win32/api/wlanapi/ns-wlanapi-wlan_country_or_region_string_list)|
|wlan_intf_opcode_supported_infrastructure_auth_cipher_pairs|[WLAN_AUTH_CIPHER_PAIR_LIST](/windows/win32/api/wlanapi/ns-wlanapi-wlan_auth_cipher_pair_list)|
|wlan_intf_opcode_supported_safe_mode|BOOL|

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>Only the <b>wlan_intf_opcode_autoconf_enabled</b>, <b>wlan_intf_opcode_bss_type</b>, <b>wlan_intf_opcode_interface_state</b>, and  <b>wlan_intf_opcode_current_connection</b> constants are valid.

### -param pReserved

Reserved for future use. Must be set to <b>NULL</b>.

### -param pdwDataSize [out]

The size of the <i>ppData</i> parameter, in bytes.

### -param ppData [out]

Pointer to the memory location that contains the queried value of the parameter specified by the <i>OpCode</i> parameter.

<div class="alert"><b>Note</b>  If <i>OpCode</i> is set to <b>wlan_intf_opcode_autoconf_enabled</b>, <b>wlan_intf_opcode_background_scan_enabled</b>, or <b>wlan_intf_opcode_media_streaming_mode</b>, then the pointer referenced by <i>ppData</i> may point to an integer value. If the pointer referenced by <i>ppData</i> points to 0, then the integer value should be converted  to the boolean value <b>FALSE</b>. If the pointer referenced by <i>ppData</i> points to a nonzero integer, then the integer value should be converted  to the boolean value <b>TRUE</b>. </div>
<div> </div>

### -param pWlanOpcodeValueType [out, optional]

If passed a non-<b>NULL</b> value, points to a <a href="/windows/win32/api/wlanapi/ne-wlanapi-wlan_opcode_value_type-r1">WLAN_OPCODE_VALUE_TYPE</a> value that specifies the type of opcode returned. This parameter may be <b>NULL</b>.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value may be one of the following return codes.

## -remarks

The caller is responsible for using <a href="/windows/win32/api/wlanapi/nf-wlanapi-wlanfreememory">WlanFreeMemory</a> to free the memory allocated for <i>ppData</i>.

When   <i>OpCode</i> is set to  <b>wlan_intf_opcode_current_operation_mode</b>,  <b>WlanQueryInterface</b>  queries the current operation mode of the wireless interface. For more information about operation modes, see <a href="https://www.microsoft.com/?ref=go">Native 802.11 Operation Modes</a>. Two operation modes are supported: <b>DOT11_OPERATION_MODE_EXTENSIBLE_STATION</b> and  <b>DOT11_OPERATION_MODE_NETWORK_MONITOR</b>. The operation mode constants are defined in the header file Windot11.h. <i>ppData</i> will point to one of these two values.


#### Examples

The following example enumerates the wireless LAN interfaces on the local computer, queries each interface for the <a href="/windows/win32/api/wlanapi/ns-wlanapi-wlan_connection_attributes">WLAN_CONNECTION_ATTRIBUTES</a> on the interface, and prints values from the retrieved <b>WLAN_CONNECTION_ATTRIBUTES</b> structure.

For another example using the <b>WlanQueryInterface</b> function, see the <a href="/windows/win32/api/wlanapi/ns-wlanapi-wlan_radio_state">WLAN_RADIO_STATE</a> structure. 

<div class="alert"><b>Note</b>  This example will fail to load on Windows Server 2008 and Windows Server 2008 R2 if the Wireless LAN Service is not installed and started.</div>
<div> </div>

```cpp
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#include <wlanapi.h>
#include <Windot11.h>           // for DOT11_SSID struct
#include <objbase.h>
#include <wtypes.h>

//#include <wchar.h>
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

    WCHAR GuidString[39] = { 0 };

    unsigned int i, k;

    // variables used for WlanEnumInterfaces

    PWLAN_INTERFACE_INFO_LIST pIfList = NULL;
    PWLAN_INTERFACE_INFO pIfInfo = NULL;

    // variables used for WlanQueryInterfaces for opcode = wlan_intf_opcode_current_connection
    PWLAN_CONNECTION_ATTRIBUTES pConnectInfo = NULL;
    DWORD connectInfoSize = sizeof(WLAN_CONNECTION_ATTRIBUTES);
    WLAN_OPCODE_VALUE_TYPE opCode = wlan_opcode_value_type_invalid;

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
                wprintf(L"  InterfaceGUID[%d]:\t %ws\n", i, GuidString);
            }
            wprintf(L"  Interface Description[%d]: %ws", i, pIfInfo->strInterfaceDescription);
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

            // If interface state is connected, call WlanQueryInterface
            // to get current connection attributes
            if (pIfInfo->isState == wlan_interface_state_connected) {
                dwResult = WlanQueryInterface(hClient,
                                              &pIfInfo->InterfaceGuid,
                                              wlan_intf_opcode_current_connection,
                                              NULL,
                                              &connectInfoSize,
                                              (PVOID *) &pConnectInfo, 
                                              &opCode);

                if (dwResult != ERROR_SUCCESS) {
                    wprintf(L"WlanQueryInterface failed with error: %u\n", dwResult);
                    dwRetVal = 1;
                    // You can use FormatMessage to find out why the function failed
                } else {
                    wprintf(L"  WLAN_CONNECTION_ATTRIBUTES for this interface\n");

                    wprintf(L"  Interface State:\t ");
                    switch (pConnectInfo->isState) {
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

                    wprintf(L"  Connection Mode:\t ");
                    switch (pConnectInfo->wlanConnectionMode) {
                    case wlan_connection_mode_profile:
                        wprintf(L"A profile is used to make the connection\n");
                        break;
                    case wlan_connection_mode_temporary_profile:
                        wprintf(L"A temporary profile is used to make the connection\n");
                        break;
                    case wlan_connection_mode_discovery_secure:
                        wprintf(L"Secure discovery is used to make the connection\n");
                        break;
                    case wlan_connection_mode_discovery_unsecure:
                        wprintf(L"Unsecure discovery is used to make the connection\n");
                        break;
                    case wlan_connection_mode_auto:
                        wprintf
                            (L"connection initiated by wireless service automatically using a persistent profile\n");
                        break;
                    case wlan_connection_mode_invalid:
                        wprintf(L"Invalid connection mode\n");
                        break;
                    default:
                        wprintf(L"Unknown connection mode %ld\n",
                                pConnectInfo->wlanConnectionMode);
                        break;
                    }

                    wprintf(L"  Profile name used:\t %ws\n", pConnectInfo->strProfileName);

                    wprintf(L"  Association Attributes for this connection\n");
                    wprintf(L"    SSID:\t\t ");
                    if (pConnectInfo->wlanAssociationAttributes.dot11Ssid.uSSIDLength == 0)
                        wprintf(L"\n");
                    else {
                        for (k = 0;
                             k < pConnectInfo->wlanAssociationAttributes.dot11Ssid.uSSIDLength;
                             k++) {
                            wprintf(L"%c",
                                    (int) pConnectInfo->wlanAssociationAttributes.dot11Ssid.
                                    ucSSID[k]);
                        }
                        wprintf(L"\n");
                    }

                    wprintf(L"    BSS Network type:\t ");
                    switch (pConnectInfo->wlanAssociationAttributes.dot11BssType) {
                    case dot11_BSS_type_infrastructure:
                        wprintf(L"Infrastructure\n");
                        break;
                    case dot11_BSS_type_independent:
                        wprintf(L"Infrastructure\n");
                        break;
                    default:
                        wprintf(L"Other = %lu\n",
                                pConnectInfo->wlanAssociationAttributes.dot11BssType);
                        break;
                    }

                    wprintf(L"    MAC address:\t ");
                    for (k = 0; k < sizeof (pConnectInfo->wlanAssociationAttributes.dot11Bssid);
                         k++) {
                        if (k == 5)
                            wprintf(L"%.2X\n",
                                    pConnectInfo->wlanAssociationAttributes.dot11Bssid[k]);
                        else
                            wprintf(L"%.2X-",
                                    pConnectInfo->wlanAssociationAttributes.dot11Bssid[k]);
                    }

                    wprintf(L"    PHY network type:\t ");
                    switch (pConnectInfo->wlanAssociationAttributes.dot11PhyType) {
                    case dot11_phy_type_fhss:
                        wprintf(L"Frequency-hopping spread-spectrum (FHSS)\n");
                        break;
                    case dot11_phy_type_dsss:
                        wprintf(L"Direct sequence spread spectrum (DSSS)\n");
                        break;
                    case dot11_phy_type_irbaseband:
                        wprintf(L"Infrared (IR) baseband\n");
                        break;
                    case dot11_phy_type_ofdm:
                        wprintf(L"Orthogonal frequency division multiplexing (OFDM)\n");
                        break;
                    case dot11_phy_type_hrdsss:
                        wprintf(L"High-rate DSSS (HRDSSS) = \n");
                        break;
                    case dot11_phy_type_erp:
                        wprintf(L"Extended rate PHY type\n");
                        break;
                    case dot11_phy_type_ht:
                        wprintf(L"802.11n PHY type\n");
                        break;
                    default:
                        wprintf(L"Unknown = %lu\n",
                                pConnectInfo->wlanAssociationAttributes.dot11PhyType);
                        break;
                    }

                    wprintf(L"    PHY index:\t\t %u\n",
                            pConnectInfo->wlanAssociationAttributes.uDot11PhyIndex);

                    wprintf(L"    Signal Quality:\t %d\n",
                            pConnectInfo->wlanAssociationAttributes.wlanSignalQuality);

                    wprintf(L"    Receiving Rate:\t %ld\n",
                            pConnectInfo->wlanAssociationAttributes.ulRxRate);

                    wprintf(L"    Transmission Rate:\t %ld\n",
                            pConnectInfo->wlanAssociationAttributes.ulTxRate);
                    wprintf(L"\n");
                    
                    wprintf(L"  Security Attributes for this connection\n");

                    wprintf(L"    Security enabled:\t ");
                    if (pConnectInfo->wlanSecurityAttributes.bSecurityEnabled == 0)
                        wprintf(L"No\n");
                    else
                        wprintf(L"Yes\n");

                    wprintf(L"    802.1X enabled:\t ");
                    if (pConnectInfo->wlanSecurityAttributes.bOneXEnabled == 0)
                        wprintf(L"No\n");
                    else
                        wprintf(L"Yes\n");

                    wprintf(L"    Authentication Algorithm: ");
                    switch (pConnectInfo->wlanSecurityAttributes.dot11AuthAlgorithm) {
                    case DOT11_AUTH_ALGO_80211_OPEN:
                        wprintf(L"802.11 Open\n");
                        break;
                    case DOT11_AUTH_ALGO_80211_SHARED_KEY:
                        wprintf(L"802.11 Shared\n");
                        break;
                    case DOT11_AUTH_ALGO_WPA:
                        wprintf(L"WPA\n");
                        break;
                    case DOT11_AUTH_ALGO_WPA_PSK:
                        wprintf(L"WPA-PSK\n");
                        break;
                    case DOT11_AUTH_ALGO_WPA_NONE:
                        wprintf(L"WPA-None\n");
                        break;
                    case DOT11_AUTH_ALGO_RSNA:
                        wprintf(L"RSNA\n");
                        break;
                    case DOT11_AUTH_ALGO_RSNA_PSK:
                        wprintf(L"RSNA with PSK\n");
                        break;
                    default:
                        wprintf(L"Other (%lu)\n", pConnectInfo->wlanSecurityAttributes.dot11AuthAlgorithm);
                        break;
                    }
                        
                    wprintf(L"    Cipher Algorithm:\t ");
                    switch (pConnectInfo->wlanSecurityAttributes.dot11CipherAlgorithm) {
                    case DOT11_CIPHER_ALGO_NONE:
                        wprintf(L"None\n");
                        break;
                    case DOT11_CIPHER_ALGO_WEP40:
                        wprintf(L"WEP-40\n");
                        break;
                    case DOT11_CIPHER_ALGO_TKIP:
                        wprintf(L"TKIP\n");
                        break;
                    case DOT11_CIPHER_ALGO_CCMP:
                        wprintf(L"CCMP\n");
                        break;
                    case DOT11_CIPHER_ALGO_WEP104:
                        wprintf(L"WEP-104\n");
                        break;
                    case DOT11_CIPHER_ALGO_WEP:
                        wprintf(L"WEP\n");
                        break;
                    default:
                        wprintf(L"Other (0x%x)\n", pConnectInfo->wlanSecurityAttributes.dot11CipherAlgorithm);
                        break;
                    }
                    wprintf(L"\n");
                }
            }
        }

    }
    if (pConnectInfo != NULL) {
        WlanFreeMemory(pConnectInfo);
        pConnectInfo = NULL;
    }

    if (pIfList != NULL) {
        WlanFreeMemory(pIfList);
        pIfList = NULL;
    }

    return dwRetVal;
}

```

## -see-also

<a href="/windows/win32/NativeWiFi/dot11-bss-type">DOT11_BSS_TYPE</a>



<a href="https://www.microsoft.com/?ref=go">Native 802.11 Operation Modes</a>



<a href="/windows/win32/api/wlanapi/ns-wlanapi-wlan_auth_cipher_pair_list">WLAN_AUTH_CIPHER_PAIR_LIST</a>



<a href="/windows/win32/api/wlanapi/ns-wlanapi-wlan_connection_attributes">WLAN_CONNECTION_ATTRIBUTES</a>



<a href="/windows/win32/api/wlanapi/ns-wlanapi-wlan_country_or_region_string_list">WLAN_COUNTRY_OR_REGION_STRING_LIST</a>



<a href="/windows/win32/api/wlanapi/ne-wlanapi-wlan_interface_state-r1">WLAN_INTERFACE_STATE</a>



<a href="/windows/win32/api/wlanapi/ne-wlanapi-wlan_intf_opcode">WLAN_INTF_OPCODE</a>



<a href="/windows/win32/api/wlanapi/ne-wlanapi-wlan_opcode_value_type-r1">WLAN_OPCODE_VALUE_TYPE</a>



<a href="/windows/win32/api/wlanapi/ns-wlanapi-wlan_radio_state">WLAN_RADIO_STATE</a>



<a href="/windows/win32/api/wlanapi/ns-wlanapi-wlan_statistics">WLAN_STATISTICS</a>



<a href="/windows/win32/api/wlanapi/nf-wlanapi-wlanfreememory">WlanFreeMemory</a>



<a href="/windows/win32/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a>



<a href="/windows/win32/api/wlanapi/nf-wlanapi-wlansetinterface">WlanSetInterface</a>