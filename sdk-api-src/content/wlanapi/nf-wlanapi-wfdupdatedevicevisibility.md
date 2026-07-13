---
UID: NF:wlanapi.WFDUpdateDeviceVisibility
title: WFDUpdateDeviceVisibility function (wlanapi.h)
description: Updates device visibility for the Wi-Fi Direct device address for a given installed Wi-Fi Direct device node.
helpviewer_keywords: ["WFDUpdateDeviceVisibility","WFDUpdateDeviceVisibility function [NativeWIFI]","nwifi.wfdupdatedevicevisibility","wlanapi/WFDUpdateDeviceVisibility"]
old-location: nwifi\wfdupdatedevicevisibility.htm
tech.root: nwifi
ms.assetid: 696B7466-5ED0-4202-9AAF-CE2544C5A5B8
ms.date: 12/05/2018
ms.keywords: WFDUpdateDeviceVisibility, WFDUpdateDeviceVisibility function [NativeWIFI], nwifi.wfdupdatedevicevisibility, wlanapi/WFDUpdateDeviceVisibility
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
 - WFDUpdateDeviceVisibility
 - wlanapi/WFDUpdateDeviceVisibility
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
 - WFDUpdateDeviceVisibility
---

# WFDUpdateDeviceVisibility function


## -description

The <b>WFDUpdateDeviceVisibility</b> function  updates device visibility for the Wi-Fi Direct device address for a given installed Wi-Fi Direct device node.

## -parameters

### -param pDeviceAddress

A pointer to the Wi-Fi Direct device address of the client device.

This device address must be obtained from a Device Node created as a result of the Inbox pairing experience.

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

This error is returned if the  <i>pDeviceAddress</i> parameter is <b>NULL</b>. 

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

The <b>WFDUpdateDeviceVisibility</b> function is part of Wi-Fi Direct, a new feature in Windows 8 and Windows Server 2012. Wi-Fi Direct is based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see <a href="https://www.wi-fi.org/file/wi-fi-peer-to-peer-services-technical-specification-package">Wi-Fi Alliance Published Specifications</a>). The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi adhoc (IBSS) mechanism. 



The <b>WFDUpdateDeviceVisibility</b> function will perform a targeted Wi-Fi Direct discovery, and will update the DEVPKEY_WiFiDirect_IsVisibile property key on the device node for the given device.

## -see-also

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession">WFDCancelOpenSession</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle">WFDCloseHandle</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession">WFDCloseSession</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle">WFDOpenHandle</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession">WFDOpenLegacySession</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession">WFDStartOpenSession</a>



<a href="/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback">WFD_OPEN_SESSION_COMPLETE_CALLBACK</a>