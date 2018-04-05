---
UID: NF:wlanapi.WlanSetProfileCustomUserData
title: WlanSetProfileCustomUserData function
author: windows-driver-content
description: Sets the custom user data associated with a profile.
old-location: nwifi\wlansetuserdata.htm
old-project: NativeWiFi
ms.assetid: 3b37ff29-4c9b-42c8-b00a-a9dfca1d3fed
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: WlanSetProfileCustomUserData, WlanSetProfileCustomUserData function [NativeWIFI], nwifi.wlansetuserdata, wlanapi/WlanSetProfileCustomUserData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: WL_DISPLAY_PAGES, *PWL_DISPLAY_PAGES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	wlanapi.dll
api_name:
-	WlanSetProfileCustomUserData
product: Windows
targetos: Windows
req.lib: Wlanapi.lib
req.dll: Wlanapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WlanSetProfileCustomUserData function


## -description


The <b>WlanSetProfileCustomUserData</b> function sets the custom user data associated with a profile.


## -parameters




### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="https://msdn.microsoft.com/27bfa0c1-4443-47a4-a374-326f553fa3bb">WlanOpenHandle</a> function.


### -param pInterfaceGuid [in]

The GUID of the interface.


### -param strProfileName [in]

The name of the profile associated with the custom user data. Profile names are case-sensitive. This string must be NULL-terminated.


### -param dwDataSize [in]

The size of <i>pData</i>, in bytes.


### -param pData [in]

A pointer to the user data to be set.


### -param pReserved

Reserved for future use. Must be set to <b>NULL</b>.


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
One of the following conditions occurred:

<ul>
<li><i>hClientHandle</i> is <b>NULL</b> or invalid.</li>
<li><i>pInterfaceGuid</i> is <b>NULL</b>.</li>
<li><i>strProfileName</i> is <b>NULL</b>.</li>
<li><i>pReserved</i> is not <b>NULL</b>.</li>
<li><i>dwDataSize</i> is not 0 and <i>pData</i> is <b>NULL</b>.</li>
</ul>
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



For every wireless WLAN profile used by the Native Wifi AutoConfig service, Windows maintains the concept of custom user data.  This custom user data is initially non-existent, but can be set by calling the <b>WlanSetProfileCustomUserData</b> function. The custom user data gets reset to empty any time the profile is modified by calling the <a href="https://msdn.microsoft.com/3f8dca2e-6fe5-4c7d-a135-a33c61ba3dd5">WlanSetProfile</a> function.

Once custom user data has been set, this data can be accessed using the <a href="https://msdn.microsoft.com/5973be2f-8267-496b-827b-778f705accdc">WlanGetProfileCustomUserData</a> function. 

All wireless LAN functions require an interface GUID for the wireless interface when performing profile operations. When a wireless interface is removed, its state is cleared from Wireless LAN Service (WLANSVC)  and no profile operations are possible.

The <b>WlanSetProfileCustomUserData</b> function can fail with <b>ERROR_INVALID_PARAMETER</b> if the wireless interface specified in the <i>pInterfaceGuid</i> parameter has been removed from the system (a USB  wireless adapter that has been removed, for example). 




## -see-also




<a href="https://msdn.microsoft.com/8312d213-1d01-4bd0-a8d9-65ca23560888">WLAN_profile Schema</a>



<a href="https://msdn.microsoft.com/6486e961-402f-45c8-a806-ab91a4f0f156">WlanGetProfile</a>



<a href="https://msdn.microsoft.com/5973be2f-8267-496b-827b-778f705accdc">WlanGetProfileCustomUserData</a>



<a href="https://msdn.microsoft.com/f4336113-538f-4161-a71f-64a432e31f1c">WlanGetProfileList</a>



<a href="https://msdn.microsoft.com/3f8dca2e-6fe5-4c7d-a135-a33c61ba3dd5">WlanSetProfile</a>



<a href="https://msdn.microsoft.com/2bef0f2f-165d-446a-afa8-735658048152">WlanSetProfileEapUserData</a>



<a href="https://msdn.microsoft.com/c34c39c0-8200-438a-8353-238225aea5cb">WlanSetProfileEapXmlUserData</a>
 

 

