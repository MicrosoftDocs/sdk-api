---
UID: NS:wlanapi._WLAN_RADIO_STATE
title: "_WLAN_RADIO_STATE"
author: windows-sdk-content
description: Specifies the radio state on a list of physical layer (PHY) types.
old-location: nwifi\wlan_radio_state.htm
old-project: NativeWiFi
ms.assetid: 61551b46-785e-4353-910c-8ce23172b176
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PWLAN_RADIO_STATE, PWLAN_RADIO_STATE, PWLAN_RADIO_STATE structure pointer [NativeWIFI], WLAN_RADIO_STATE, WLAN_RADIO_STATE structure [NativeWIFI], _WLAN_RADIO_STATE, nwifi.wlan_radio_state, wlanapi/PWLAN_RADIO_STATE, wlanapi/WLAN_RADIO_STATE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wlanapi.h
req.include-header: 
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
tech.root: 
req.typenames: WLAN_RADIO_STATE, *PWLAN_RADIO_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - WLAN_RADIO_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WLAN_RADIO_STATE structure


## -description


The <b>WLAN_RADIO_STATE</b> structurespecifies the radio state on a list of physical layer (PHY) types.


## -struct-fields




### -field dwNumberOfPhys

The number of valid PHY indices in the <b>PhyRadioState</b> member.


### -field PhyRadioState

An array of <a href="https://msdn.microsoft.com/20da1494-4264-4d0d-b789-25e2be6a8dd4">WLAN_PHY_RADIO_STATE</a> structures that specify the radio states of a number of PHY indices. Only the first <b>dwNumberOfPhys</b> entries in this array are valid.


## -remarks



The <b>WLAN_RADIO_STATE</b> structure is used with the <a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a> function when the <i>OpCode</i> parameter is set to <b>wlan_intf_opcode_radio_state</b>. If the call is successful, the <i>ppData</i> parameter points to a <b>WLAN_RADIO_STATE</b> structure. 

The <a href="https://msdn.microsoft.com/20da1494-4264-4d0d-b789-25e2be6a8dd4">WLAN_PHY_RADIO_STATE</a> structure members in the <b>WLAN_RADIO_STATE</b> structure can be used with the <a href="https://msdn.microsoft.com/114a2a71-babd-4cd7-860a-fea523bcc865">WlanSetInterface</a> function when the <i>OpCode</i> parameter is set to <b>wlan_intf_opcode_radio_state</b> to change the radio state. 

The <a href="https://msdn.microsoft.com/20da1494-4264-4d0d-b789-25e2be6a8dd4">WLAN_PHY_RADIO_STATE</a> structure is also used for  notification by the media specific module (MSM) when the radio state changes. An application registers to receive MSM notifications by calling the <a href="https://msdn.microsoft.com/e24810da-ed3b-41c4-b7b1-290b01e26cd5">WlanRegisterNotification</a> function with the <i>dwNotifSource</i> parameter set to a value that includes <b>WLAN_NOTIFICATION_SOURCE_MSM</b>. For more information on these notifications, see the <a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a> structure and the <a href="https://msdn.microsoft.com/7847658a-6789-43ad-95ad-b520333863e6">WLAN_NOTIFICATION_MSM</a> enumeration reference.


#### Examples

The following example enumerates the wireless LAN interfaces on the local computer, queries each interface for the <b>WLAN_RADIO_STATE</b> on the interface, and prints values from the retrieved <b>WLAN_RADIO_STATE</b> structure.

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

    WCHAR GuidString[39] = { 0 };

    unsigned int i;

    // variables used for WlanEnumInterfaces

    PWLAN_INTERFACE_INFO_LIST pIfList = NULL;
    PWLAN_INTERFACE_INFO pIfInfo = NULL;

    // variables used for WlanQueryInterfaces for opcode = wlan_intf_opcode_radio_state
    PWLAN_RADIO_STATE pradioStateInfo = NULL;
    DWORD radioStateInfoSize = sizeof (WLAN_RADIO_STATE);
    WLAN_OPCODE_VALUE_TYPE opCode = wlan_opcode_value_type_invalid;

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
            pIfInfo = (WLAN_INTERFACE_INFO *) &amp; pIfList-&gt;InterfaceInfo[i];
            wprintf(L"  Interface Index[%u]:\t %lu\n", i, i);
            iRet =
                StringFromGUID2(pIfInfo-&gt;InterfaceGuid, (LPOLESTR) &amp; GuidString,
                                sizeof (GuidString) / sizeof (*GuidString));
            // For c rather than C++ source code, the above line needs to be
            // iRet = StringFromGUID2(&amp;pIfInfo-&gt;InterfaceGuid, (LPOLESTR) &amp;GuidString, 
            //     sizeof(GuidString)/sizeof(*GuidString)); 
            if (iRet == 0)
                wprintf(L"StringFromGUID2 failed\n");
            else {
                wprintf(L"  InterfaceGUID[%d]:\t %ws\n", i, GuidString);
            }
            wprintf(L"  Interface Description[%d]: %ws", i, pIfInfo-&gt;strInterfaceDescription);
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

            dwResult = WlanQueryInterface(hClient,
                                          &amp;pIfInfo-&gt;InterfaceGuid,
                                          wlan_intf_opcode_radio_state,
                                          NULL,
                                          &amp;radioStateInfoSize,
                                          (PVOID *) &amp; pradioStateInfo, &amp;opCode);

            if (dwResult != ERROR_SUCCESS) {
                wprintf(L"WlanQueryInterface failed with error: %u\n", dwResult);
                dwRetVal = 1;
                // You can use FormatMessage to find out why the function failed
            } else {
                wprintf(L"  WLAN_RADIO_STATE for this interface\n");

                wprintf(L"  Number of valid PHYs:\t %u\n", pradioStateInfo-&gt;dwNumberOfPhys);
                wprintf(L"  Radio state:\n");
                wprintf(L"      Index of PHYs type[0]:\t %u\n",
                        pradioStateInfo-&gt;PhyRadioState[0].dwPhyIndex);

                wprintf(L"      Software radio state[0]:\t ");
                switch (pradioStateInfo-&gt;PhyRadioState[0].dot11SoftwareRadioState) {
                case dot11_radio_state_unknown:
                    wprintf(L"Unknown\n");
                    break;
                case dot11_radio_state_on:
                    wprintf(L"On\n");
                    break;
                case dot11_radio_state_off:
                    wprintf(L"Off\n");
                    break;
                default:
                    wprintf(L"Other Unknown state %ld\n", pradioStateInfo-&gt;PhyRadioState[0].dot11SoftwareRadioState);
                    break;
                }
                
                
                wprintf(L"      Hardware radio state[0]:\t ");
                switch (pradioStateInfo-&gt;PhyRadioState[0].dot11HardwareRadioState) {
                case dot11_radio_state_unknown:
                    wprintf(L"Unknown\n");
                    break;
                case dot11_radio_state_on:
                    wprintf(L"On\n");
                    break;
                case dot11_radio_state_off:
                    wprintf(L"Off\n");
                    break;
                default:
                    wprintf(L"Other Unknown state %ld\n", pradioStateInfo-&gt;PhyRadioState[0].dot11HardwareRadioState);
                    break;
                }
                
                wprintf(L"\n");
            }
        }
    }

if (pradioStateInfo != NULL) {
    WlanFreeMemory(pradioStateInfo);
    pradioStateInfo = NULL;
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




<a href="https://msdn.microsoft.com/58589825-407c-4635-a2ea-20695b63ec2c">WLAN_NOTIFICATION_DATA</a>



<a href="https://msdn.microsoft.com/7847658a-6789-43ad-95ad-b520333863e6">WLAN_NOTIFICATION_MSM</a>



<a href="https://msdn.microsoft.com/20da1494-4264-4d0d-b789-25e2be6a8dd4">WLAN_PHY_RADIO_STATE</a>



<a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a>



<a href="https://msdn.microsoft.com/114a2a71-babd-4cd7-860a-fea523bcc865">WlanSetInterface</a>
 

 

