---
UID: NF:wlanapi.WlanReasonCodeToString
title: WlanReasonCodeToString function (wlanapi.h)
description: Retrieves a string that describes a specified reason code.
helpviewer_keywords: ["WlanReasonCodeToString","WlanReasonCodeToString function [NativeWIFI]","nwifi.wlanreasoncodetostring","wlanapi/WlanReasonCodeToString"]
old-location: nwifi\wlanreasoncodetostring.htm
tech.root: nwifi
ms.assetid: 2a02e2d2-91d0-4b54-ad02-a76442edcff8
ms.date: 12/05/2018
ms.keywords: WlanReasonCodeToString, WlanReasonCodeToString function [NativeWIFI], nwifi.wlanreasoncodetostring, wlanapi/WlanReasonCodeToString
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
targetos: Windows
req.typenames: 
req.redist: Wireless LAN API for Windows XP with SP2
ms.custom: 19H1
f1_keywords:
 - WlanReasonCodeToString
 - wlanapi/WlanReasonCodeToString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - wlanapi.dll
 - Ext-MS-Win-networking-wlanapi-l1-1-0.dll
api_name:
 - WlanReasonCodeToString
---

# WlanReasonCodeToString function


## -description

The <b>WlanReasonCodeToString</b> function retrieves a  string that describes a specified reason code.

## -parameters

### -param dwReasonCode [in]

A <a href="/windows/desktop/NativeWiFi/wlan-reason-code">WLAN_REASON_CODE</a> value of which the string description is requested.

### -param dwBufferSize [in]

The size of the buffer used to store the string, in <b>WCHAR</b>.  If the reason code string is longer than the buffer, it will be truncated and NULL-terminated. If <i>dwBufferSize</i> is larger than the actual amount of memory allocated to <i>pStringBuffer</i>, then an access violation will occur in the calling program.

### -param pStringBuffer [in]

Pointer to a buffer that will receive the string. The caller must allocate memory to <i>pStringBuffer</i> before calling <b>WlanReasonCodeToString</b>.

### -param pReserved

Reserved for future use.  Must be set to <b>NULL</b>.

## -returns

If the function succeeds, the return value is a pointer to a constant string.

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
A parameter is incorrect. This error is returned if any of the following conditions occur:<ul>
<li><i>dwBufferSize</i> is 0.</li>
<li><i>pStringBuffer</i> is <b>NULL</b>.</li>
<li><i>pReserved</i> is not <b>NULL</b>.</li>
</ul>


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Various RPC and other error codes. Use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.


</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/NativeWiFi/wlan-reason-code">WLAN_REASON_CODE</a>