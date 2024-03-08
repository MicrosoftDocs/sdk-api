---
UID: NF:wlanapi.WFDCloseHandle
title: WFDCloseHandle function (wlanapi.h)
description: Closes a handle to the Wi-Fi Direct service.
helpviewer_keywords: ["WFDCloseHandle","WFDCloseHandle function [NativeWIFI]","nwifi.wfdclosehandle","wlanapi/WFDCloseHandle"]
old-location: nwifi\wfdclosehandle.htm
tech.root: nwifi
ms.assetid: A27C0AE1-1C51-4CAC-8929-63870ADB15A7
ms.date: 12/05/2018
ms.keywords: WFDCloseHandle, WFDCloseHandle function [NativeWIFI], nwifi.wfdclosehandle, wlanapi/WFDCloseHandle
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
 - WFDCloseHandle
 - wlanapi/WFDCloseHandle
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
 - WFDCloseHandle
---

# WFDCloseHandle function


## -description

The <b>WFDCloseHandle</b> function closes a handle to the Wi-Fi Direct service.

## -parameters

### -param hClientHandle [in]

A client handle to the Wi-Fi Direct service. This handle was  obtained by a previous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle">WFDOpenHandle</a> function.

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
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is invalid. 

This error is returned if the handle specified in the <i>hClientHandle</i>  parameter was not found in the handle table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The parameter is incorrect. 

This error is returned if the <i>hClientHandle</i> parameter is <b>NULL</b> or not valid.

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

The <b>WFDCloseHandle</b> function is part of Wi-Fi Direct, a new feature in Windows 8 and Windows Server 2012. Wi-Fi Direct is based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see <a href="https://www.wi-fi.org/file/wi-fi-peer-to-peer-services-technical-specification-package">Wi-Fi Alliance Published Specifications</a>). The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi adhoc (IBSS) mechanism. 



In order to use Wi-Fi Direct, an application must first obtain a handle to the Wi-Fi Direct service by calling the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle">WFDOpenHandle</a> function. The Wi-Fi Direct (WFD) handle returned by the  <b>WFDOpenHandle</b> function is used for subsequent calls made to the Wi-Fi Direct service. Once an application is done using the Wi-Fi Direct service, the application should call the <b>WFDCloseHandle</b> function to signal to the Wi-Fi Direct service that the application is done using the service. This allows the  Wi-Fi Direct service  to release resources used by the application.

## -see-also

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession">WFDCancelOpenSession</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession">WFDCloseSession</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle">WFDOpenHandle</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession">WFDOpenLegacySession</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession">WFDStartOpenSession</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility">WFDUpdateDeviceVisibility</a>



<a href="/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback">WFD_OPEN_SESSION_COMPLETE_CALLBACK</a>