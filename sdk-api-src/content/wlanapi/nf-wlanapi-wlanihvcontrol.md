---
UID: NF:wlanapi.WlanIhvControl
title: WlanIhvControl function (wlanapi.h)
description: Provides a mechanism for independent hardware vendor (IHV) control of WLAN drivers or services.
helpviewer_keywords: ["WlanIhvControl","WlanIhvControl function [NativeWIFI]","nwifi.wlanihvcontrol","wlanapi/WlanIhvControl"]
old-location: nwifi\wlanihvcontrol.htm
tech.root: nwifi
ms.assetid: 3fc32119-0f92-4939-8125-812f45584d45
ms.date: 12/05/2018
ms.keywords: WlanIhvControl, WlanIhvControl function [NativeWIFI], nwifi.wlanihvcontrol, wlanapi/WlanIhvControl
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
 - WlanIhvControl
 - wlanapi/WlanIhvControl
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
 - WlanIhvControl
---

# WlanIhvControl function


## -description

The <b>WlanIhvControl</b> function provides a mechanism for independent hardware vendor (IHV) control of WLAN drivers or services.

## -parameters

### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle">WlanOpenHandle</a> function.

### -param pInterfaceGuid [in]

The GUID of the interface.

### -param Type [in]

 A <a href="/windows/win32/api/wlanapi/ne-wlanapi-wlan_ihv_control_type-r1">WLAN_IHV_CONTROL_TYPE</a> structure that specifies the type of software bypassed by the IHV control function.

### -param dwInBufferSize [in]

The size, in bytes, of the input buffer.

### -param pInBuffer [in]

A generic buffer for driver or service interface input.

### -param dwOutBufferSize [in]

The size, in bytes, of the output buffer.

### -param pOutBuffer [in, out, optional]

A generic buffer for driver or service interface output.

### -param pdwBytesReturned [out]

The number of bytes returned.

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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient permissions to perform this operation. When called, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanihvcontrol">WlanIhvControl</a>  retrieves the discretionary access control list (DACL) stored with the  <b>wlan_secure_ihv_control</b> object. If the DACL does not contain an access control entry (ACE) that grants WLAN_WRITE_ACCESS permission to the access token of the calling thread, then <b>WlanIhvControl</b>    returns <b>ERROR_ACCESS_DENIED</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
<i>hClientHandle</i> is <b>NULL</b> or invalid, <i>pInterfaceGuid</i> is <b>NULL</b>, or <i>pdwBytesReturned</i> is <b>NULL</b>.

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

## -see-also

<a href="/windows/win32/api/wlanapi/ne-wlanapi-wlan_ihv_control_type-r1">WLAN_IHV_CONTROL_TYPE</a>