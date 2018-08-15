---
UID: NF:wlanapi.WlanUIEditProfile
title: WlanUIEditProfile function
author: windows-sdk-content
description: Displays the wireless profile user interface (UI).
old-location: nwifi\wlanuieditprofile.htm
old-project: nativewifi
ms.assetid: e6453a70-2a11-4f01-adc1-67346a5856b2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WlanUIEditProfile, WlanUIEditProfile function [NativeWIFI], nwifi.wlanuieditprofile, wlanapi/WlanUIEditProfile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wlanapi.h
req.include-header: Wlanapi.h
req.redist: 
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
req.typenames: WL_DISPLAY_PAGES, *PWL_DISPLAY_PAGES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - wlanui.dll
api_name:
 - WlanUIEditProfile
product: Windows
targetos: Windows
req.lib: Wlanui.lib
req.dll: Wlanui.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WlanUIEditProfile function


## -description


Displays the wireless profile user interface (UI). This UI is used to view and edit advanced settings of a wireless network profile.


## -parameters




### -param dwClientVersion [in]

Specifies the highest version of the WLAN API that the client supports. 
Values other than WLAN_UI_API_VERSION will be ignored.


### -param wstrProfileName [in]

Contains the name of the profile to be viewed or edited. Profile names are case-sensitive. This string must be NULL-terminated.

The supplied profile must be present on the interface <i>pInterfaceGuid</i>. That means the profile must have been previously created and saved in the profile store and that the profile must be valid for the supplied interface.


### -param pInterfaceGuid [in]

The GUID of the interface.


### -param hWnd [in]

The handle of the  application window requesting the UI display.


### -param wlStartPage [in]

A <a href="https://msdn.microsoft.com/040433b7-9204-4462-a8fd-7b65bcd1880b">WL_DISPLAY_PAGES</a> value that specifies the active tab when the UI dialog box appears.


### -param pReserved

Reserved for future use. Must be set to <b>NULL</b>. 


### -param pWlanReasonCode [out]

A pointer to a <a href="https://msdn.microsoft.com/7b267f0b-b3f7-4729-bab4-de3bdd0a35a2">WLAN_REASON_CODE</a> value that indicates why the UI display failed.


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
One of the supplied parameters is not valid.

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



If <b>WlanUIEditProfile</b> returns ERROR_SUCCESS, any changes to the profile made in the UI will be saved in the profile store.



