---
UID: NF:wlanapi.WFDOpenHandle
title: WFDOpenHandle function (wlanapi.h)
description: Opens a handle to the Wi-Fi Direct service and negotiates a version of the Wi-FI Direct API to use.
helpviewer_keywords: ["WFDOpenHandle","WFDOpenHandle function [NativeWIFI]","nwifi.wfdopenhandle","wlanapi/WFDOpenHandle"]
old-location: nwifi\wfdopenhandle.htm
tech.root: nwifi
ms.assetid: D89FAC10-BC33-44BE-ABC8-962241949281
ms.date: 12/05/2018
ms.keywords: WFDOpenHandle, WFDOpenHandle function [NativeWIFI], nwifi.wfdopenhandle, wlanapi/WFDOpenHandle
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
 - WFDOpenHandle
 - wlanapi/WFDOpenHandle
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
 - WFDOpenHandle
---

# WFDOpenHandle function


## -description

The <b>WFDOpenHandle</b> function opens a handle to the Wi-Fi Direct service and negotiates a version of the Wi-FI Direct API to use.

## -parameters

### -param dwClientVersion [in]

The highest version of the Wi-Fi Direct API the client supports.

For Windows 8 and Windows Server 2012, this parameter should be set to <b>WFD_API_VERSION</b>, constant defined in the <i>Wlanapi.h</i> header file.

### -param pdwNegotiatedVersion [out]

A pointer to a <b>DWORD</b> to received the negotiated version.

If the <b>WFDOpenHandle</b> function is successful, the version negotiated with the Wi-Fi Direct Service to be used by this session is returned. This value is usually the highest version supported by both the client and Wi-Fi Direct service.

### -param phClientHandle [out]

A pointer to a <b>HANDLE</b> to receive the handle to the Wi-Fi Direct service for this session.

If the <b>WFDOpenHandle</b> function is successful, a handle to the Wi-Fi Direct service to use in this session is returned.

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

This error is returned if the <i>pdwNegotiatedVersion</i> parameter is <b>NULL</b> or the <i>phClientHandle</i> parameter is <b>NULL</b>. This value is also returned if the <i>dwClientVersion</i> parameter is not equal to <b>WFD_API_VERSION</b>.

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
<dt><b>ERROR_REMOTE_SESSION_LIMIT_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
An attempt was made to establish a session to a network server, but there are already too many sessions established to that server.

This error is returned if too many handles have been issued by the Wi-Fi Direct service.

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

The <b>WFDOpenHandle</b> function is part of Wi-Fi Direct, a new feature in Windows 8 and Windows Server 2012. Wi-Fi Direct is based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see <a href="https://www.wi-fi.org/file/wi-fi-peer-to-peer-services-technical-specification-package">Wi-Fi Alliance Published Specifications</a>). The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi adhoc (IBSS) mechanism. 



In order to use Wi-Fi Direct, an application must first obtain a handle to the Wi-Fi Direct service by calling the <b>WFDOpenHandle</b> function. The Wi-Fi Direct (WFD) handle returned by the  <b>WFDOpenHandle</b> function is used for subsequent calls made to the Wi-Fi Direct service. Once an application is done using the Wi-Fi Direct service, the application should call the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle">WFDCloseHandle</a> function to signal to the Wi-Fi Direct service that the application is done using the service. This allows the  Wi-Fi Direct service  to release resources used by the application.

## -see-also

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession">WFDCancelOpenSession</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle">WFDCloseHandle</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession">WFDCloseSession</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession">WFDOpenLegacySession</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession">WFDStartOpenSession</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility">WFDUpdateDeviceVisibility</a>



<a href="/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback">WFD_OPEN_SESSION_COMPLETE_CALLBACK</a>