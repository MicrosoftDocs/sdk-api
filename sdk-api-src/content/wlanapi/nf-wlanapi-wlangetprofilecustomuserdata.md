---
UID: NF:wlanapi.WlanGetProfileCustomUserData
title: WlanGetProfileCustomUserData function (wlanapi.h)
description: Gets the custom user data associated with a wireless profile.
helpviewer_keywords: ["WlanGetProfileCustomUserData","WlanGetProfileCustomUserData function [NativeWIFI]","nwifi.wlangetprofilecustomuserdata","wlanapi/WlanGetProfileCustomUserData"]
old-location: nwifi\wlangetprofilecustomuserdata.htm
tech.root: nwifi
ms.assetid: 5973be2f-8267-496b-827b-778f705accdc
ms.date: 12/05/2018
ms.keywords: WlanGetProfileCustomUserData, WlanGetProfileCustomUserData function [NativeWIFI], nwifi.wlangetprofilecustomuserdata, wlanapi/WlanGetProfileCustomUserData
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WlanGetProfileCustomUserData
 - wlanapi/WlanGetProfileCustomUserData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - wlanapi.dll
api_name:
 - WlanGetProfileCustomUserData
---

# WlanGetProfileCustomUserData function


## -description

The <b>WlanGetProfileCustomUserData</b> function gets the custom user data associated with a wireless profile.

## -parameters

### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param pInterfaceGuid [in]

A pointer to the GUID of the wireless LAN interface.

### -param strProfileName [in]

The name of the profile with which the custom user data is associated. Profile names are case-sensitive. This string must be NULL-terminated.

### -param pReserved

Reserved for future use. Must be set to <b>NULL</b>.

### -param pdwDataSize [out]

The size, in bytes,  of the user data buffer pointed to by the <i>ppData</i> parameter.

### -param ppData [out]

A pointer to the user data.

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
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The system cannot find the file specified. This error is returned if no user custom data exists for the profile specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>hClientHandle</i> parameter is <b>NULL</b> or  not valid, the <i>pInterfaceGuid</i> parameter is <b>NULL</b>, the <i>strProfileName</i> parameter is <b>NULL</b>, the <i>pReserved</i> parameter is not <b>NULL</b>, the <i>pdwDataSize</i> parameter is 0, or the <i>ppData</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The system cannot find the file specified. This error is returned if no custom user data exists for the profile specified.

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
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
This function was called from an unsupported platform. This value will be returned if this function was called from a Windows XP with SP3 or Wireless LAN API for Windows XP with SP2 client.

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

For every wireless WLAN profile used by the Native Wifi AutoConfig service, Windows maintains the concept of custom user data.  This custom user data is initially non-existent, but can be set by calling the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilecustomuserdata">WlanSetProfileCustomUserData</a> function. The custom user data gets reset to empty any time the profile is modified by calling the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile">WlanSetProfile</a> function.

Once custom user data has been set, this data can be accessed using the <b>WlanGetProfileCustomUserData</b> function. 

The caller is responsible for freeing the memory allocated for the buffer pointed to by the <i>ppData</i> parameter using the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory">WlanFreeMemory</a> function.


#### Examples

The following example enumerates the wireless LAN interfaces on the local computer, and then tries to retrieve any custom user data  information for a specific wireless profile on each wireless LAN interface. The size of the user custom data is printed. 

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

    PBYTE pProfileData = NULL;
    DWORD dwDataSize = 0;
   
        // Validate the parameters
    if (argc < 2) {
        wprintf(L"usage: %s <profile>\n", argv[0]);
        wprintf(L"   Gets a wireless profile\n");
        wprintf(L"   Example\n");
        wprintf(L"       %s \"Default Wireless\"\n", argv[0]);
        exit(1);
    }
    
    pProfileName = argv[1];
     
    wprintf(L"Custom user data information for profile: %ws\n\n", pProfileName);
    
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

            dwResult = WlanGetProfileCustomUserData(hClient,
                                             &pIfInfo->InterfaceGuid,
                                             pProfileName,
                                             NULL,
                                             &dwDataSize,
                                             &pProfileData);

            if (dwResult != ERROR_SUCCESS) {
                wprintf(L"WlanGetProfileCustomData failed with error: %u\n",
                        dwResult);
                // You can use FormatMessage to find out why the function failed
            } else {
                wprintf(L"Profile Name:  %ws\n", pProfileName);

                wprintf(L"  dwDataSize:\t    0x%x\n", dwDataSize);
                wprintf(L"  Profile Custom Data:\n");
//                wprintf(L"%ws\n\n", pProfileXml);

                wprintf(L"\n");    

                wprintf(L"\n");
            }
        }

    }
    if (pProfileData != NULL) {
        WlanFreeMemory(pProfileData);
        pProfileData = NULL;
    }

    if (pIfList != NULL) {
        WlanFreeMemory(pIfList);
        pIfList = NULL;
    }

    return dwRetVal;
}

```

## -see-also

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile">WlanGetProfile</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilelist">WlanGetProfileList</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile">WlanSetProfile</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilecustomuserdata">WlanSetProfileCustomUserData</a>