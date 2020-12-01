---
UID: NF:wlanapi.WlanOpenHandle
title: WlanOpenHandle function (wlanapi.h)
description: Opens a connection to the server.
helpviewer_keywords: ["WlanOpenHandle","WlanOpenHandle function [NativeWIFI]","nwifi.wlanopenhandle","wlanapi/WlanOpenHandle"]
old-location: nwifi\wlanopenhandle.htm
tech.root: nwifi
ms.assetid: 27bfa0c1-4443-47a4-a374-326f553fa3bb
ms.date: 12/05/2018
ms.keywords: WlanOpenHandle, WlanOpenHandle function [NativeWIFI], nwifi.wlanopenhandle, wlanapi/WlanOpenHandle
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
 - WlanOpenHandle
 - wlanapi/WlanOpenHandle
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
 - WlanOpenHandle
---

# WlanOpenHandle function


## -description

The <b>WlanOpenHandle</b> function opens a connection to the server.

## -parameters

### -param dwClientVersion [in]

The highest version of the WLAN API that the client supports. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Client version for Windows XP with SP3 and Wireless LAN API for Windows XP with SP2.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Client version for Windows Vista and Windows Server 2008

</td>
</tr>
</table>

### -param pReserved

Reserved for future use.  Must be set to <b>NULL</b>.

### -param pdwNegotiatedVersion [out]

The version of the WLAN API that will be used in this session.  This value is usually the highest version supported by both the client and server.

### -param phClientHandle [out]

A handle for the client to use in this session.  This handle is used by other functions throughout the session.

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
<i>pdwNegotiatedVersion</i> is <b>NULL</b>, <i>phClientHandle</i> is <b>NULL</b>, or <i>pReserved</i> is not <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate memory to create the client context.

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
<dt><b>ERROR_REMOTE_SESSION_LIMIT_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
Too many handles have been issued by the server.

</td>
</tr>
</table>

## -remarks

The version number specified by <i>dwClientVersion</i> and <i>pdwNegotiatedVersion</i> is a composite version number made up of both major and minor versions. The major version is specified by the low-order word, and the minor version is specified by the high-order word. The macros <code>WLAN_API_VERSION_MAJOR(_v)</code> and <code>WLAN_API_VERSION_MINOR(_v)</code> return the major and minor version numbers respectively. You can construct a version number using the macro <code>WLAN_API_MAKE_VERSION(_major, _minor)</code>.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b><b>WlanOpenHandle</b> will return an error message if the Wireless Zero Configuration (WZC) service has not been started or if the WZC service is not responsive.

## -see-also

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle">WlanCloseHandle</a>