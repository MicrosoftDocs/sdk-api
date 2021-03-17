---
UID: NF:dhcpcsdk.DhcpRegisterParamChange
title: DhcpRegisterParamChange function (dhcpcsdk.h)
description: The DhcpRegisterParamChange function enables clients to register for notification of changes in DHCP configuration parameters.
helpviewer_keywords: ["DhcpRegisterParamChange","DhcpRegisterParamChange function [DHCP]","_dhcp_dhcpregisterparamchange","dhcp.dhcpregisterparamchange","dhcpcsdk/DhcpRegisterParamChange"]
old-location: dhcp\dhcpregisterparamchange.htm
tech.root: DHCP
ms.assetid: e0099827-2f88-4309-a5e7-3bc1395de5a2
ms.date: 12/05/2018
ms.keywords: DhcpRegisterParamChange, DhcpRegisterParamChange function [DHCP], _dhcp_dhcpregisterparamchange, dhcp.dhcpregisterparamchange, dhcpcsdk/DhcpRegisterParamChange
req.header: dhcpcsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dhcpcsvc.lib
req.dll: Dhcpcsvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DhcpRegisterParamChange
 - dhcpcsdk/DhcpRegisterParamChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpcsvc.dll
api_name:
 - DhcpRegisterParamChange
---

# DhcpRegisterParamChange function


## -description

The 
<b>DhcpRegisterParamChange</b> function enables clients to register for notification of changes in DHCP configuration parameters.

## -parameters

### -param Flags [in]

Reserved. Must be set to DHCPCAPI_REGISTER_HANDLE_EVENT. If it is not set to this flag value, the API call will not be successful.

### -param Reserved [in]

Reserved. Must be set to <b>NULL</b>.

### -param AdapterName [in]

GUID of the adapter for which event notification is being requested.  Must be under 256 characters.

### -param ClassId [in]

Reserved. Must be set to <b>NULL</b>.

### -param Params [in]

Parameters for which the client is interested in registering for notification, in the form of a <a href="/windows/win32/api/dhcpcsdk/ns-dhcpcsdk-dhcpcapi_params_array">DHCPCAPI_PARAMS_ARRAY</a> structure.

### -param Handle [in, out]

Attributes of <i>Handle</i> are determined by the value of <i>Flags</i>. In version 2 of the DHCP API, <i>Flags</i> must be set to DHCPCAPI_REGISTER_HANDLE_EVENT, and therefore, <i>Handle</i> must be a pointer to a <b>HANDLE</b> variable that will hold the handle to a Windows event that gets signaled when parameters specified in <i>Params</i> change. Note that this <b>HANDLE</b> variable is used in a subsequent call to the 
<b>DhcpDeRegisterParamChange</b> function to deregister event notifications associated with this particular call to the 
<b>DhcpRegisterParamChange</b> function.

## -returns

Returns ERROR_SUCCESS upon successful completion. Otherwise, returns Windows error codes.

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
Returned if the AdapterName parameter is over 256 characters long.

</td>
</tr>
</table>

## -remarks

Version 2 of the DHCP Client API provides only event-based notification. With event-based notification in DHCP, clients enable notification by having <i>Handle</i> point to a variable that, upon successful return, holds the EVENT handles that are signaled whenever changes occur to the parameters requested in <i>Params</i>.

## -see-also

<a href="/previous-versions/windows/desktop/dhcp/dhcp-functions">DHCP Functions</a>



<a href="/windows/win32/api/dhcpcsdk/ns-dhcpcsdk-dhcpcapi_params_array">DHCPCAPI_PARAMS_ARRAY</a>



<a href="/previous-versions/windows/desktop/api/dhcpcsdk/nf-dhcpcsdk-dhcpcapiinitialize">DhcpCApiInitialize</a>



<a href="/previous-versions/windows/desktop/api/dhcpcsdk/nf-dhcpcsdk-dhcpderegisterparamchange">DhcpDeRegisterParamChange</a>