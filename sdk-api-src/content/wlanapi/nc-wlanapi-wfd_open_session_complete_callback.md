---
UID: NC:wlanapi.WFD_OPEN_SESSION_COMPLETE_CALLBACK
title: WFD_OPEN_SESSION_COMPLETE_CALLBACK (wlanapi.h)
description: Defines the callback function that is called by the WFDStartOpenSession function when the WFDStartOpenSession operation completes.
helpviewer_keywords: ["ERROR_INVALID_PARAMETER","ERROR_INVALID_STATE","ERROR_SERVICE_NOT_ACTIVE","RPC_STATUS","WFD_OPEN_SESSION_COMPLETE_CALLBACK","WFD_OPEN_SESSION_COMPLETE_CALLBACK callback","WFD_OPEN_SESSION_COMPLETE_CALLBACK callback function [NativeWIFI]","nwifi.wfd_open_session_complete_callback","wlanapi/WFD_OPEN_SESSION_COMPLETE_CALLBACK"]
old-location: nwifi\wfd_open_session_complete_callback.htm
tech.root: nwifi
ms.assetid: 2CB91D70-920A-4D97-B96D-B264F59150AC
ms.date: 12/05/2018
ms.keywords: ERROR_INVALID_PARAMETER, ERROR_INVALID_STATE, ERROR_SERVICE_NOT_ACTIVE, RPC_STATUS, WFD_OPEN_SESSION_COMPLETE_CALLBACK, WFD_OPEN_SESSION_COMPLETE_CALLBACK callback, WFD_OPEN_SESSION_COMPLETE_CALLBACK callback function [NativeWIFI], nwifi.wfd_open_session_complete_callback, wlanapi/WFD_OPEN_SESSION_COMPLETE_CALLBACK
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WFD_OPEN_SESSION_COMPLETE_CALLBACK
 - wlanapi/WFD_OPEN_SESSION_COMPLETE_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - wlanapi.h
api_name:
 - WFD_OPEN_SESSION_COMPLETE_CALLBACK
---

# WFD_OPEN_SESSION_COMPLETE_CALLBACK callback function


## -description

The  <b>WFD_OPEN_SESSION_COMPLETE_CALLBACK</b> function defines the callback function that is called by the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession">WFDStartOpenSession</a> function when the <b>WFDStartOpenSession</b> operation completes.

## -parameters

### -param hSessionHandle [in]

A session handle to a Wi-Fi Direct session. This is a session handle previously returned by the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession">WFDStartOpenSession</a> function.

### -param pvContext [in]

An context pointer passed to the callback function from the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession">WFDStartOpenSession</a> function.

### -param guidSessionInterface [in]

The interface GUID of the local network interface on which this Wi-Fi Direct device has an open session.
This parameter is useful if higher-layer protocols need to determine which network interface a Wi-Fi Direct session is bound to.
This value is only returned if the <i>dwError</i> parameter is ERROR_SUCCESS.

### -param dwError [in]

A value that specifies whether there was an error encountered during the call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession">WFDStartOpenSession</a> function. If this value is ERROR_SUCCESS, then no error occurred and the operation to open the session completed successfully.

The following other values are possible:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ERROR_INVALID_PARAMETER"></a><a id="error_invalid_parameter"></a><dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The parameter is incorrect. This error is returned if the <i>hClientHandle</i> parameter is <b>NULL</b> or not valid.

</td>
</tr>
<tr>
<td width="40%"><a id="ERROR_INVALID_STATE"></a><a id="error_invalid_state"></a><dl>
<dt><b>ERROR_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The group or resource is not in the correct state to perform the requested operation. This error is returned if the Wi-Fi Direct service is disabled by group policy on a domain.

</td>
</tr>
<tr>
<td width="40%"><a id="ERROR_SERVICE_NOT_ACTIVE"></a><a id="error_service_not_active"></a><dl>
<dt><b>ERROR_SERVICE_NOT_ACTIVE</b></dt>
</dl>
</td>
<td width="60%">
The service has not been started. This error is returned if the WLAN AutoConfig Service is not running.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_STATUS"></a><a id="rpc_status"></a><dl>
<dt><b>RPC_STATUS</b></dt>
</dl>
</td>
<td width="60%">
Various RPC and other error codes. Use <b>FormatMessage</b> to obtain the message string for the returned error. 

</td>
</tr>
</table>

### -param dwReasonCode [in]

A value that specifies the more detail if an error occurred during <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession">WFDStartOpenSession</a>.

## -remarks

The <b>WFD_OPEN_SESSION_COMPLETE_CALLBACK</b> function is part of Wi-Fi Direct, a new feature in Windows 8 and Windows Server 2012. Wi-Fi Direct is based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see <a href="https://www.wi-fi.org/file/wi-fi-peer-to-peer-services-technical-specification-package">Wi-Fi Alliance Published Specifications</a>). The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi adhoc (IBSS) mechanism. 



The  <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession">WFDStartOpenSession</a> function starts an asynchronous operation to start an on-demand connection to  a specific Wi-Fi Direct device. The target Wi-Fi device must previously have been paired through the Windows Pairing experience. When the asynchronous operation to make the Wi-FI Direct connection completes, the callback function specified in the <i>pfnCallback</i> parameter is called.

## -see-also

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession">WFDCancelOpenSession</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle">WFDCloseHandle</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession">WFDCloseSession</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle">WFDOpenHandle</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession">WFDStartOpenSession</a>



<a href="/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback">WFD_OPEN_SESSION_COMPLETE_CALLBACK</a>