---
UID: NF:wlanapi.WlanQueryInterface
title: WlanQueryInterface function
author: windows-sdk-content
description: The WlanQueryInterface function queries various parameters of a specified interface.
old-location: nwifi\wlanqueryinterface.htm
old-project: nativewifi
ms.assetid: e20eb9a3-5824-48ee-b13e-b0252bbf495e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WlanQueryInterface, WlanQueryInterface function [NativeWIFI], nwifi.wlanqueryinterface, wlanapi/WlanQueryInterface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wlanapi.h
req.include-header: Wlanapi.h
req.redist: Wireless LAN API for Windows XP with SP2
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
 - Wlanapi.dll
 - Ext-MS-Win-networking-wlanapi-l1-1-0.dll
api_name:
 - WlanQueryInterface
product: Windows
targetos: Windows
req.lib: Wlanapi.lib
req.dll: Wlanapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WlanQueryInterface function


## -description


The <b>WlanQueryInterface</b> function queries various parameters of a specified interface.


## -parameters




### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="https://msdn.microsoft.com/27bfa0c1-4443-47a4-a374-326f553fa3bb">WlanOpenHandle</a> function.


### -param pInterfaceGuid [in]

The GUID of the interface to be queried.


### -param OpCode [in]

A <a href="https://msdn.microsoft.com/4f68e52b-7fa3-4654-b4d3-41ca627c138a">WLAN_INTF_OPCODE</a> value that specifies the parameter to be queried.  The following table lists the valid constants along with the data type of the parameter in <i>ppData</i>.

<table>
<tr>
<th><b>WLAN_INTF_OPCODE</b> value</th>
<th><i>ppData</i> data type</th>
</tr>
<tr>
<td>wlan_intf_opcode_autoconf_enabled</td>
<td>BOOL</td>
</tr>
<tr>
<td>wlan_intf_opcode_background_scan_enabled </td>
<td>BOOL</td>
</tr>
<tr>
<td>wlan_intf_opcode_radio_state </td>
<td>
<a href="https://msdn.microsoft.com/61551b46-785e-4353-910c-8ce23172b176">WLAN_RADIO_STATE</a>
</td>
</tr>
<tr>
<td>wlan_intf_opcode_bss_type </td>
<td>
<a href="https://msdn.microsoft.com/13d57339-655e-4978-974e-e7b12a83d18a">DOT11_BSS_TYPE</a>
</td>
</tr>
<tr>
<td>wlan_intf_opcode_interface_state </td>
<td>
<a href="https://msdn.microsoft.com/209540c0-81b7-4dc5-97ef-5ecc7f19a82b">WLAN_INTERFACE_STATE</a>
</td>
</tr>
<tr>
<td>wlan_intf_opcode_current_connection </td>
<td>
<a href="https://msdn.microsoft.com/91b8058d-faf6-46ee-a03b-f762e9cdae4d">WLAN_CONNECTION_ATTRIBUTES</a>
</td>
</tr>
<tr>
<td>wlan_intf_opcode_channel_number 
</td>
<td>ULONG</td>
</tr>
<tr>
<td>wlan_intf_opcode_supported_infrastructure_auth_cipher_pairs 
</td>
<td>
<a href="https://msdn.microsoft.com/747ee8e6-aafa-42ec-9183-a5a4a2603fc0">WLAN_AUTH_CIPHER_PAIR_LIST</a>
</td>
</tr>
<tr>
<td>wlan_intf_opcode_supported_adhoc_auth_cipher_pairs </td>
<td>
<a href="https://msdn.microsoft.com/747ee8e6-aafa-42ec-9183-a5a4a2603fc0">WLAN_AUTH_CIPHER_PAIR_LIST</a>
</td>
</tr>
<tr>
<td>wlan_intf_opcode_supported_country_or_region_string_list </td>
<td>
<a href="https://msdn.microsoft.com/64343c1f-3543-406f-a64c-94196b8aa17e">WLAN_COUNTRY_OR_REGION_STRING_LIST</a>
</td>
</tr>
<tr>
<td>wlan_intf_opcode_media_streaming_mode </td>
<td>BOOL</td>
</tr>
<tr>
<td>wlan_intf_opcode_statistics </td>
<td>
<a href="https://msdn.microsoft.com/d66d89f1-bb12-4c2e-8c7a-a4eba008955d">WLAN_STATISTICS</a>
</td>
</tr>
<tr>
<td>wlan_intf_opcode_rssi</td>
<td>LONG</td>
</tr>
<tr>
<td>wlan_intf_opcode_current_operation_mode </td>
<td>ULONG</td>
</tr>
<tr>
<td>wlan_intf_opcode_supported_safe_mode</td>
<td>BOOL</td>
</tr>
<tr>
<td>wlan_intf_opcode_certified_safe_mode</td>
<td>BOOL</td>
</tr>
</table>
 

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

If passed a non-<b>NULL</b> value, points to a <a href="https://msdn.microsoft.com/36f74ee5-499e-4d3d-ae32-a57c5e3b2eac">WLAN_OPCODE_VALUE_TYPE</a> value that specifies the type of opcode returned. This parameter may be <b>NULL</b>. 


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value may be one of the following return codes.




## -remarks



The caller is responsible for using <a href="https://msdn.microsoft.com/241afb9d-8b16-4d76-b311-302b5492853e">WlanFreeMemory</a> to free the memory allocated for <i>ppData</i>.

When   <i>OpCode</i> is set to  <b>wlan_intf_opcode_current_operation_mode</b>,  <b>WlanQueryInterface</b>  queries the current operation mode of the wireless interface. For more information about operation modes, see <a href="http://go.microsoft.com/fwlink/p/?linkid=71672">Native 802.11 Operation Modes</a>. Two operation modes are supported: <b>DOT11_OPERATION_MODE_EXTENSIBLE_STATION</b> and  <b>DOT11_OPERATION_MODE_NETWORK_MONITOR</b>. The operation mode constants are defined in the header file Windot11.h. <i>ppData</i> will point to one of these two values.


#### Examples

The following example enumerates the wireless LAN interfaces on the local computer, queries each interface for the <a href="https://msdn.microsoft.com/91b8058d-faf6-46ee-a03b-f762e9cdae4d">WLAN_CONNECTION_ATTRIBUTES</a> on the interface, and prints values from the retrieved <b>WLAN_CONNECTION_ATTRIBUTES</b> structure.

For another example using the <b>WlanQueryInterface</b> function, see the <a href="https://msdn.microsoft.com/61551b46-785e-4353-910c-8ce23172b176">WLAN_RADIO_STATE</a> structure. 

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




<a href="https://msdn.microsoft.com/13d57339-655e-4978-974e-e7b12a83d18a">DOT11_BSS_TYPE</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=71672">Native 802.11 Operation Modes</a>



<a href="https://msdn.microsoft.com/747ee8e6-aafa-42ec-9183-a5a4a2603fc0">WLAN_AUTH_CIPHER_PAIR_LIST</a>



<a href="https://msdn.microsoft.com/91b8058d-faf6-46ee-a03b-f762e9cdae4d">WLAN_CONNECTION_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/64343c1f-3543-406f-a64c-94196b8aa17e">WLAN_COUNTRY_OR_REGION_STRING_LIST</a>



<a href="https://msdn.microsoft.com/209540c0-81b7-4dc5-97ef-5ecc7f19a82b">WLAN_INTERFACE_STATE</a>



<a href="https://msdn.microsoft.com/4f68e52b-7fa3-4654-b4d3-41ca627c138a">WLAN_INTF_OPCODE</a>



<a href="https://msdn.microsoft.com/36f74ee5-499e-4d3d-ae32-a57c5e3b2eac">WLAN_OPCODE_VALUE_TYPE</a>



<a href="https://msdn.microsoft.com/61551b46-785e-4353-910c-8ce23172b176">WLAN_RADIO_STATE</a>



<a href="https://msdn.microsoft.com/d66d89f1-bb12-4c2e-8c7a-a4eba008955d">WLAN_STATISTICS</a>



<a href="https://msdn.microsoft.com/241afb9d-8b16-4d76-b311-302b5492853e">WlanFreeMemory</a>



<a href="https://msdn.microsoft.com/27bfa0c1-4443-47a4-a374-326f553fa3bb">WlanOpenHandle</a>



<a href="https://msdn.microsoft.com/114a2a71-babd-4cd7-860a-fea523bcc865">WlanSetInterface</a>
 

 

