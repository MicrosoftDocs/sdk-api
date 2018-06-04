---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



