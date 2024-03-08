---
UID: NF:wlanapi.WFDCloseSession
title: WFDCloseSession function (wlanapi.h)
description: Closes a session after a previously successful call to the WFDStartOpenSession function.
helpviewer_keywords: ["WFDCloseSession","WFDCloseSession function [NativeWIFI]","nwifi.wfdclosesession","wlanapi/WFDCloseSession"]
old-location: nwifi\wfdclosesession.htm
tech.root: nwifi
ms.assetid: DEAF32C9-64A6-419A-A466-DE2313AE534C
ms.date: 12/05/2018
ms.keywords: WFDCloseSession, WFDCloseSession function [NativeWIFI], nwifi.wfdclosesession, wlanapi/WFDCloseSession
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
 - WFDCloseSession
 - wlanapi/WFDCloseSession
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
 - WFDCloseSession
---

# WFDCloseSession function


## -description

The  <b>WFDCloseSession</b> function closes a session after a previously successful call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession">WFDStartOpenSession</a> function.

## -parameters

### -param hSessionHandle [in]

A session handle to a Wi-Fi Direct session. This is a session handle previously returned by the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession">WFDStartOpenSession</a> function.

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

This error is returned if the handle specified in the <i>hSessionHandle</i>  parameter was not found in the handle table.

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

This error is returned if the <i>hSessionHandle</i> parameter is <b>NULL</b> or not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The group or resource is not in the correct state to perform the requested operation.

This error is returned if the Wi-Fi Direct service is disabled by group policy on a domain.

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

The <b>WFDCloseSession</b> function is part of Wi-Fi Direct, a new feature in Windows 8 and Windows Server 2012. Wi-Fi Direct is based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see <a href="https://www.wi-fi.org/file/wi-fi-peer-to-peer-services-technical-specification-package">Wi-Fi Alliance Published Specifications</a>). The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi adhoc (IBSS) mechanism. 



The  <b>WFDCloseSession</b> function queues a future work item to close the session, so disconnection may not be immediate.



Calling the  <b>WFDCloseSession</b> function  while a <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession">WFDStartOpenSession</a> call is pending will not close the session.


It is the responsibility of the caller to pass the <b>WFDCloseSession</b> function a handle in the <i>hSessionHandle </i> parameter that was returned from a successful asynchronous call to the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession">WFDStartOpenSession</a> function.



Calling the  <b>WFDCloseSession</b> function with a handle that was valid and has become invalid will yield undefined results.

## -see-also

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession">WFDCancelOpenSession</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle">WFDCloseHandle</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle">WFDOpenHandle</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession">WFDOpenLegacySession</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession">WFDStartOpenSession</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility">WFDUpdateDeviceVisibility</a>



<a href="/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback">WFD_OPEN_SESSION_COMPLETE_CALLBACK</a>