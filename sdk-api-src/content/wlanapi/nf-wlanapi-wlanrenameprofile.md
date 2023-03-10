---
UID: NF:wlanapi.WlanRenameProfile
title: WlanRenameProfile function (wlanapi.h)
description: Renames the specified profile.
helpviewer_keywords: ["WlanRenameProfile","WlanRenameProfile function [NativeWIFI]","nwifi.wlanrenameprofile","wlanapi/WlanRenameProfile"]
old-location: nwifi\wlanrenameprofile.htm
tech.root: nwifi
ms.assetid: 488e9f87-8b98-48c6-81d5-d7237cdf5bd5
ms.date: 12/05/2018
ms.keywords: WlanRenameProfile, WlanRenameProfile function [NativeWIFI], nwifi.wlanrenameprofile, wlanapi/WlanRenameProfile
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
 - WlanRenameProfile
 - wlanapi/WlanRenameProfile
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
 - WlanRenameProfile
---

# WlanRenameProfile function


## -description

The <b>WlanRenameProfile</b> function renames the specified profile.

## -parameters

### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

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

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile">WlanDeleteProfile</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile">WlanGetProfile</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile">WlanSetProfile</a>