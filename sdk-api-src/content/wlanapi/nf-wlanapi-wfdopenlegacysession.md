---
UID: NF:wlanapi.WFDOpenLegacySession
title: WFDOpenLegacySession function (wlanapi.h)
description: Retrieves and applies a stored profile for a Wi-Fi Direct legacy device.
helpviewer_keywords: ["WFDOpenLegacySession","WFDOpenLegacySession function [NativeWIFI]","nwifi.wfdopenlegacysession","wlanapi/WFDOpenLegacySession"]
old-location: nwifi\wfdopenlegacysession.htm
tech.root: nwifi
ms.assetid: D7BE8108-EF18-49FC-8B14-CED45B6C682B
ms.date: 12/05/2018
ms.keywords: WFDOpenLegacySession, WFDOpenLegacySession function [NativeWIFI], nwifi.wfdopenlegacysession, wlanapi/WFDOpenLegacySession
req.header: wlanapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - WFDOpenLegacySession
 - wlanapi/WFDOpenLegacySession
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
 - WFDOpenLegacySession
---

# WFDOpenLegacySession function


## -description

The <b>WFDOpenLegacySession</b> function  retrieves and applies a stored profile for a Wi-Fi Direct legacy device.

## -parameters

### -param hClientHandle

A <b>HANDLE</b> to the Wi-Fi Direct service for this session. This parameter is retrieved using the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle">WFDOpenHandle</a> function.

### -param pLegacyMacAddress

A pointer to Wi-Fi Direct device address of the legacy client device.

### -param phSessionHandle

A pointer to a <b>HANDLE</b> to receive the handle to the Wi-Fi Direct service for this session.

If the <b>WFDOpenLegacySession</b> function is successful, a handle to the Wi-Fi Direct service to use in this session is returned.

### -param pGuidSessionInterface

A pointer to the GUID of the network interface for this session.

If the <b>WFDOpenLegacySession</b> function is successful, a GUID of the network interface on which Wi-Fi Direct session is returned.

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
The parameter is incorrect. 

This error is returned if the <i>phClientHandle</i> or the <i>pLegacyMacAddress</i> parameter is <b>NULL</b>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough storage is available to process this command.

This error is returned if the system was unable to allocate memory to create the client context.

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

The <b>WFDOpenLegacySession</b> function is part of Wi-Fi Direct, a new feature in Windows 8 and Windows Server 2012. Wi-Fi Direct is based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see <a href="https://www.wi-fi.org/file/wi-fi-peer-to-peer-services-technical-specification-package">Wi-Fi Alliance Published Specifications</a>). The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi adhoc (IBSS) mechanism. 



In order to use Wi-Fi Direct, an application must first obtain a handle to the Wi-Fi Direct service by calling the <b>WFDOpenLegacySession</b> or <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle">WFDOpenHandle</a> function. The Wi-Fi Direct (WFD) handle returned by the  <b>WFDOpenHandle</b> function is used for subsequent calls made to the Wi-Fi Direct service. The  <b>WFDOpenLegacySession</b> function is used to retrieve and apply a stored profile for a Wi-Fi Direct legacy device. 

The 	<b>WFDOpenLegacySession</b> function retrieves the stored legacy profile for device from the profile store for the specified legacy device address. This device address must be obtained from a Device Node created as a result of the Inbox pairing experience (Legacy WPS Pairing).

Once an application is done using the Wi-Fi Direct service, the application should call the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession">WFDCloseSession</a> function to close the session and call the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle">WFDCloseHandle</a> function to signal to the Wi-Fi Direct service that the application is done using the service. This allows the  Wi-Fi Direct service  to release resources used by the application.

## -see-also

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession">WFDCancelOpenSession</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle">WFDCloseHandle</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession">WFDCloseSession</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle">WFDOpenHandle</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession">WFDStartOpenSession</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility">WFDUpdateDeviceVisibility</a>



<a href="/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback">WFD_OPEN_SESSION_COMPLETE_CALLBACK</a>