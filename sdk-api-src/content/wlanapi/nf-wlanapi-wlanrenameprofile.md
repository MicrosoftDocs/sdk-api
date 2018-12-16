---
UID: NF:wlanapi.WlanRenameProfile
title: WlanRenameProfile function
author: windows-sdk-content
description: Renames the specified profile.
old-location: nwifi\wlanrenameprofile.htm
tech.root: NativeWiFi
ms.assetid: 488e9f87-8b98-48c6-81d5-d7237cdf5bd5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WlanRenameProfile, WlanRenameProfile function [NativeWIFI], nwifi.wlanrenameprofile, wlanapi/WlanRenameProfile
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
api_name:
 - WlanRenameProfile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WlanRenameProfile function


## -description


The <b>WlanRenameProfile</b> function renames the specified profile.


## -parameters




### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="https://msdn.microsoft.com/27bfa0c1-4443-47a4-a374-326f553fa3bb">WlanOpenHandle</a> function.


### -param pInterfaceGuid [in]

The GUID of the interface. 



### -param strOldProfileName [in]

The profile name to be changed. 


### -param strNewProfileName [in]

The new name of the profile.


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
<dt><b>ERROR_INVALID PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
<i>hClientHandle</i> is <b>NULL</b> or not valid,  <i>pInterfaceGuid</i> is <b>NULL</b>, <i>strOldProfileName</i> is <b>NULL</b>, <i>strNewProfileName</i> is <b>NULL</b>, or <i>pReserved</i> is not <b>NULL</b>.

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
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The profile specified by <i>strOldProfileName</i> was not found in the profile store.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient permissions to rename the profile. 

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
 




## -see-also




<a href="https://msdn.microsoft.com/2d1152ad-8106-4b8f-9856-9e6e36daa063">WlanDeleteProfile</a>



<a href="https://msdn.microsoft.com/6486e961-402f-45c8-a806-ab91a4f0f156">WlanGetProfile</a>



<a href="https://msdn.microsoft.com/3f8dca2e-6fe5-4c7d-a135-a33c61ba3dd5">WlanSetProfile</a>
 

 

