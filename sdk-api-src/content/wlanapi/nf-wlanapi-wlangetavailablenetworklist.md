---
UID: NF:wlanapi.WlanGetAvailableNetworkList
title: WlanGetAvailableNetworkList function
author: windows-sdk-content
description: Retrieves the list of available networks on a wireless LAN interface.
old-location: nwifi\wlangetavailablenetworklist.htm
old-project: NativeWiFi
ms.assetid: 27353a1b-2a3c-4c3b-b512-917d010ee8dd
ms.author: windowssdkdev
ms.date: 04/13/2018
ms.keywords: WLAN_AVAILABLE_NETWORK_INCLUDE_ALL_ADHOC_PROFILES, WLAN_AVAILABLE_NETWORK_INCLUDE_ALL_MANUAL_HIDDEN_PROFILES, WlanGetAvailableNetworkList, WlanGetAvailableNetworkList function [NativeWIFI], nwifi.wlangetavailablenetworklist, nwifi.wlangetvisiblenetworklist, wlanapi/WlanGetAvailableNetworkList
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	wlanapi.dll
-	Ext-MS-Win-networking-wlanapi-l1-1-0.dll
api_name:
-	WlanGetAvailableNetworkList
product: Windows
targetos: Windows
req.lib: Wlanapi.lib
req.dll: Wlanapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WlanGetAvailableNetworkList function


## -description


The <b>WlanGetAvailableNetworkList</b> function retrieves the list of available networks on a wireless LAN interface.


## -parameters




### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="https://msdn.microsoft.com/27bfa0c1-4443-47a4-a374-326f553fa3bb">WlanOpenHandle</a> function.


### -param pInterfaceGuid [in]

A pointer to the GUID of the wireless LAN interface to be queried.

 The GUID of each wireless LAN interface enabled on a local computer can be determined using the <a href="https://msdn.microsoft.com/7f817edf-1b1d-495c-afd9-d97e3ae0caab">WlanEnumInterfaces</a> function.


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

A pointer to storage for a pointer to receive the returned list of visible networks in a <a href="https://msdn.microsoft.com/0ac508b2-9117-423d-89d3-982f070c70e2">WLAN_AVAILABLE_NETWORK_LIST</a> structure.

The buffer for the <a href="https://msdn.microsoft.com/0ac508b2-9117-423d-89d3-982f070c70e2">WLAN_AVAILABLE_NETWORK_LIST</a> returned is allocated by the <b>WlanGetAvailableNetworkList</b> function if the call succeeds.


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



The <b>WlanGetAvailableNetworkList</b> function allocates memory for the list of available networks returned in the buffer pointed to by the <i>ppAvailableNetworkList</i> parameter when the function succeeds. The memory used for the buffer pointed to by <i>ppAvailableNetworkList</i> parameter should be released by calling the <a href="https://msdn.microsoft.com/241afb9d-8b16-4d76-b311-302b5492853e">WlanFreeMemory</a> function after the buffer is no longer needed.


There is a hotfix available for  Wireless LAN API for Windows XP with SP2 that can help improve the performance of applications that call <a href="https://msdn.microsoft.com/241afb9d-8b16-4d76-b311-302b5492853e">WlanFreeMemory</a> and <b>WlanGetAvailableNetworkList</b> many times. For more information, see Help and Knowledge Base article 940541, entitled "FIX: The private bytes of the application continuously increase when an application calls the WlanGetAvailableNetworkList function and the WlanFreeMemory function on a Windows XP Service Pack 2-based computer", in the Help and Support Knowledge Base at <a href="http://go.microsoft.com/fwlink/p/?linkid=102216">http://go.microsoft.com/fwlink/p/?linkid=102216</a>.




#### Examples

The following example enumerates the wireless LAN interfaces on the local computer, retrieves the list of available networks on each wireless LAN interface, and prints values from the retrieved <a href="https://msdn.microsoft.com/0ac508b2-9117-423d-89d3-982f070c70e2">WLAN_AVAILABLE_NETWORK_LIST</a> that contains the <a href="https://msdn.microsoft.com/82883cea-515b-426d-9961-c144ce99b3db">WLAN_AVAILABLE_NETWORK</a> entries.

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
        wprintf(L"Num Entries: %lu\n", pIfList-&gt;dwNumberOfItems);
        wprintf(L"Current Index: %lu\n", pIfList-&gt;dwIndex);
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
            wprintf(L"\n");

            dwResult = WlanGetAvailableNetworkList(hClient,
                                             &amp;pIfInfo-&gt;InterfaceGuid,
                                             0, 
                                             NULL, 
                                             &amp;pBssList);

            if (dwResult != ERROR_SUCCESS) {
                wprintf(L"WlanGetAvailableNetworkList failed with error: %u\n",
                        dwResult);
                dwRetVal = 1;
                // You can use FormatMessage to find out why the function failed
            } else {
                wprintf(L"WLAN_AVAILABLE_NETWORK_LIST for this interface\n");

                wprintf(L"  Num Entries: %lu\n\n", pBssList-&gt;dwNumberOfItems);

                for (j = 0; j &lt; pBssList-&gt;dwNumberOfItems; j++) {
                    pBssEntry =
                        (WLAN_AVAILABLE_NETWORK *) &amp; pBssList-&gt;Network[j];

                    wprintf(L"  Profile Name[%u]:  %ws\n", j, pBssEntry-&gt;strProfileName);
                    
                    wprintf(L"  SSID[%u]:\t\t ", j);
                    if (pBssEntry-&gt;dot11Ssid.uSSIDLength == 0)
                        wprintf(L"\n");
                    else {   
                        for (k = 0; k &lt; pBssEntry-&gt;dot11Ssid.uSSIDLength; k++) {
                            wprintf(L"%c", (int) pBssEntry-&gt;dot11Ssid.ucSSID[k]);
                        }
                        wprintf(L"\n");
                    }
                        
                    wprintf(L"  BSS Network type[%u]:\t ", j);
                    switch (pBssEntry-&gt;dot11BssType) {
                    case dot11_BSS_type_infrastructure   :
                        wprintf(L"Infrastructure (%u)\n", pBssEntry-&gt;dot11BssType);
                        break;
                    case dot11_BSS_type_independent:
                        wprintf(L"Infrastructure (%u)\n", pBssEntry-&gt;dot11BssType);
                        break;
                    default:
                        wprintf(L"Other (%lu)\n", pBssEntry-&gt;dot11BssType);
                        break;
                    }
                                
                    wprintf(L"  Number of BSSIDs[%u]:\t %u\n", j, pBssEntry-&gt;uNumberOfBssids);

                    wprintf(L"  Connectable[%u]:\t ", j);
                    if (pBssEntry-&gt;bNetworkConnectable)
                        wprintf(L"Yes\n");
                    else {
                        wprintf(L"No\n");
                        wprintf(L"  Not connectable WLAN_REASON_CODE value[%u]:\t %u\n", j, 
                            pBssEntry-&gt;wlanNotConnectableReason);
                    }        

                    wprintf(L"  Number of PHY types supported[%u]:\t %u\n", j, pBssEntry-&gt;uNumberOfPhyTypes);

                    if (pBssEntry-&gt;wlanSignalQuality == 0)
                        iRSSI = -100;
                    else if (pBssEntry-&gt;wlanSignalQuality == 100)   
                        iRSSI = -50;
                    else
                        iRSSI = -100 + (pBssEntry-&gt;wlanSignalQuality/2);    
                        
                    wprintf(L"  Signal Quality[%u]:\t %u (RSSI: %i dBm)\n", j, 
                        pBssEntry-&gt;wlanSignalQuality, iRSSI);

                    wprintf(L"  Security Enabled[%u]:\t ", j);
                    if (pBssEntry-&gt;bSecurityEnabled)
                        wprintf(L"Yes\n");
                    else
                        wprintf(L"No\n");
                        
                    wprintf(L"  Default AuthAlgorithm[%u]: ", j);
                    switch (pBssEntry-&gt;dot11DefaultAuthAlgorithm) {
                    case DOT11_AUTH_ALGO_80211_OPEN:
                        wprintf(L"802.11 Open (%u)\n", pBssEntry-&gt;dot11DefaultAuthAlgorithm);
                        break;
                    case DOT11_AUTH_ALGO_80211_SHARED_KEY:
                        wprintf(L"802.11 Shared (%u)\n", pBssEntry-&gt;dot11DefaultAuthAlgorithm);
                        break;
                    case DOT11_AUTH_ALGO_WPA:
                        wprintf(L"WPA (%u)\n", pBssEntry-&gt;dot11DefaultAuthAlgorithm);
                        break;
                    case DOT11_AUTH_ALGO_WPA_PSK:
                        wprintf(L"WPA-PSK (%u)\n", pBssEntry-&gt;dot11DefaultAuthAlgorithm);
                        break;
                    case DOT11_AUTH_ALGO_WPA_NONE:
                        wprintf(L"WPA-None (%u)\n", pBssEntry-&gt;dot11DefaultAuthAlgorithm);
                        break;
                    case DOT11_AUTH_ALGO_RSNA:
                        wprintf(L"RSNA (%u)\n", pBssEntry-&gt;dot11DefaultAuthAlgorithm);
                        break;
                    case DOT11_AUTH_ALGO_RSNA_PSK:
                        wprintf(L"RSNA with PSK(%u)\n", pBssEntry-&gt;dot11DefaultAuthAlgorithm);
                        break;
                    default:
                        wprintf(L"Other (%lu)\n", pBssEntry-&gt;dot11DefaultAuthAlgorithm);
                        break;
                    }
                        
                    wprintf(L"  Default CipherAlgorithm[%u]: ", j);
                    switch (pBssEntry-&gt;dot11DefaultCipherAlgorithm) {
                    case DOT11_CIPHER_ALGO_NONE:
                        wprintf(L"None (0x%x)\n", pBssEntry-&gt;dot11DefaultCipherAlgorithm);
                        break;
                    case DOT11_CIPHER_ALGO_WEP40:
                        wprintf(L"WEP-40 (0x%x)\n", pBssEntry-&gt;dot11DefaultCipherAlgorithm);
                        break;
                    case DOT11_CIPHER_ALGO_TKIP:
                        wprintf(L"TKIP (0x%x)\n", pBssEntry-&gt;dot11DefaultCipherAlgorithm);
                        break;
                    case DOT11_CIPHER_ALGO_CCMP:
                        wprintf(L"CCMP (0x%x)\n", pBssEntry-&gt;dot11DefaultCipherAlgorithm);
                        break;
                    case DOT11_CIPHER_ALGO_WEP104:
                        wprintf(L"WEP-104 (0x%x)\n", pBssEntry-&gt;dot11DefaultCipherAlgorithm);
                        break;
                    case DOT11_CIPHER_ALGO_WEP:
                        wprintf(L"WEP (0x%x)\n", pBssEntry-&gt;dot11DefaultCipherAlgorithm);
                        break;
                    default:
                        wprintf(L"Other (0x%x)\n", pBssEntry-&gt;dot11DefaultCipherAlgorithm);
                        break;
                    }

                    wprintf(L"  Flags[%u]:\t 0x%x", j, pBssEntry-&gt;dwFlags);
                    if (pBssEntry-&gt;dwFlags) {
                        if (pBssEntry-&gt;dwFlags &amp; WLAN_AVAILABLE_NETWORK_CONNECTED)
                            wprintf(L" - Currently connected");
                        if (pBssEntry-&gt;dwFlags &amp; WLAN_AVAILABLE_NETWORK_CONNECTED)
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/82883cea-515b-426d-9961-c144ce99b3db">WLAN_AVAILABLE_NETWORK</a>



<a href="https://msdn.microsoft.com/0ac508b2-9117-423d-89d3-982f070c70e2">WLAN_AVAILABLE_NETWORK_LIST</a>



<a href="https://msdn.microsoft.com/25a76128-13d9-47dd-9c73-1fbf06a908be">WLAN_BSS_ENTRY</a>



<a href="https://msdn.microsoft.com/aeb68835-31ce-4fa7-980a-91a328fbcbc3">WLAN_BSS_LIST</a>



<a href="https://msdn.microsoft.com/7f817edf-1b1d-495c-afd9-d97e3ae0caab">WlanEnumInterfaces</a>



<a href="https://msdn.microsoft.com/241afb9d-8b16-4d76-b311-302b5492853e">WlanFreeMemory</a>



<a href="https://msdn.microsoft.com/62f51b6e-3db1-48cd-8853-0dbe522c5e82">WlanGetNetworkBssList</a>



<a href="https://msdn.microsoft.com/cf30b285-9694-4ab0-ad13-c1ec4d8cb6e1">WlanScan</a>
 

 

