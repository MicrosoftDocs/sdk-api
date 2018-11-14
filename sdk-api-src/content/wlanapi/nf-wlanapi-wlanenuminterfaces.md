---
UID: NF:wlanapi.WlanEnumInterfaces
title: WlanEnumInterfaces function
author: windows-sdk-content
description: Enumerates all of the wireless LAN interfaces currently enabled on the local computer.
old-location: nwifi\wlanenuminterfaces.htm
tech.root: NativeWiFi
ms.assetid: 7f817edf-1b1d-495c-afd9-d97e3ae0caab
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WlanEnumInterfaces, WlanEnumInterfaces function [NativeWIFI], nwifi.wlanenuminterfaces, wlanapi/WlanEnumInterfaces
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Wlanapi.lib
req.dll: Wlanapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - wlanapi.dll
 - Ext-MS-Win-networking-wlanapi-l1-1-0.dll
api_name:
 - WlanEnumInterfaces
product: Windows
targetos: Windows
req.typenames: 
req.redist: Wireless LAN API for Windows XP with SP2
- apiref
: 
- 
: 
- WlanEnumInterfaces
: 
---

# WlanEnumInterfaces function


## -description


The <b>WlanEnumInterfaces</b> function enumerates all of the wireless LAN interfaces currently enabled on the local computer.


## -parameters




### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="https://msdn.microsoft.com/27bfa0c1-4443-47a4-a374-326f553fa3bb">WlanOpenHandle</a> function.


### -param pReserved [in]

Reserved for future use. This parameter must be set to <b>NULL</b>.


### -param ppInterfaceList [out]

A pointer to storage for a pointer to receive the returned list of wireless LAN interfaces in a <a href="https://msdn.microsoft.com/c57f4658-9f1e-4b05-a298-38a064121bb3">WLAN_INTERFACE_INFO_LIST</a> structure.

The buffer for the <a href="https://msdn.microsoft.com/c57f4658-9f1e-4b05-a298-38a064121bb3">WLAN_INTERFACE_INFO_LIST</a> returned is allocated by the <b>WlanEnumInterfaces</b> function if the call succeeds.


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
A parameter is incorrect. This error is returned if the <i>hClientHandle</i> or <i>ppInterfaceList</i> parameter is <b>NULL</b>. This error is returned if the <i>pReserved</i> is not <b>NULL</b>.  This error is also returned if the <i>hClientHandle</i> parameter is not valid.

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



The <b>WlanEnumInterfaces</b> function allocates memory for the list of returned interfaces that is returned in the buffer pointed to by the <i>ppInterfaceList</i> parameter when the function succeeds. The memory used for the buffer pointed to by <i>ppInterfaceList</i> parameter should be released by calling the <a href="https://msdn.microsoft.com/241afb9d-8b16-4d76-b311-302b5492853e">WlanFreeMemory</a> function after the buffer is no longer needed.



#### Examples

The following example enumerates the wireless LAN interfaces on the local computer and prints values from the retrieved <a href="https://msdn.microsoft.com/c57f4658-9f1e-4b05-a298-38a064121bb3">WLAN_INTERFACE_INFO_LIST</a> structure and the enumerated <a href="https://msdn.microsoft.com/906e7d59-ebd0-47e7-985e-f5d313f19ecb">WLAN_INTERFACE_INFO</a> structures.

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
    DWORD dwMaxClient = 2;   //    
    DWORD dwCurVersion = 0;
    DWORD dwResult = 0;
    int iRet = 0;
    
    WCHAR GuidString[40] = {0};
     
    int i;

    /* variables used for WlanEnumInterfaces  */
    
    PWLAN_INTERFACE_INFO_LIST pIfList = NULL;
    PWLAN_INTERFACE_INFO pIfInfo = NULL;

    
    dwResult = WlanOpenHandle(dwMaxClient, NULL, &amp;dwCurVersion, &amp;hClient); 
    if (dwResult != ERROR_SUCCESS)  {
        wprintf(L"WlanOpenHandle failed with error: %u\n", dwResult);
        // FormatMessage can be used to find out why the function failed
        return 1;
    }
    
    dwResult = WlanEnumInterfaces(hClient, NULL, &amp;pIfList); 
    if (dwResult != ERROR_SUCCESS)  {
        wprintf(L"WlanEnumInterfaces failed with error: %u\n", dwResult);
        // FormatMessage can be used to find out why the function failed
        return 1;
    }
    else {
        wprintf(L"Num Entries: %lu\n", pIfList-&gt;dwNumberOfItems);
        wprintf(L"Current Index: %lu\n", pIfList-&gt;dwIndex);
        for (i = 0; i &lt; (int) pIfList-&gt;dwNumberOfItems; i++) {
            pIfInfo = (WLAN_INTERFACE_INFO *) &amp;pIfList-&gt;InterfaceInfo[i];
            wprintf(L"  Interface Index[%d]:\t %lu\n", i, i);
            iRet = StringFromGUID2(pIfInfo-&gt;InterfaceGuid, (LPOLESTR) &amp;GuidString, 39); 
            // For c rather than C++ source code, the above line needs to be
            // iRet = StringFromGUID2(&amp;pIfInfo-&gt;InterfaceGuid, (LPOLESTR) &amp;GuidString, 39); 
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
        }
    }

    if (pIfList != NULL) {
        WlanFreeMemory(pIfList);
        pIfList = NULL;
    }
    return 0;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/906e7d59-ebd0-47e7-985e-f5d313f19ecb">WLAN_INTERFACE_INFO</a>



<a href="https://msdn.microsoft.com/c57f4658-9f1e-4b05-a298-38a064121bb3">WLAN_INTERFACE_INFO_LIST</a>



<a href="https://msdn.microsoft.com/241afb9d-8b16-4d76-b311-302b5492853e">WlanFreeMemory</a>
 

 

