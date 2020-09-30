---
UID: NF:dhcpcsdk.DhcpDeRegisterParamChange
title: DhcpDeRegisterParamChange function (dhcpcsdk.h)
description: The DhcpDeRegisterParamChange function releases resources associated with previously registered event notifications, and closes the associated event handle.
helpviewer_keywords: ["DhcpDeRegisterParamChange","DhcpDeRegisterParamChange function [DHCP]","_dhcp_dhcpderegisterparamchange","dhcp.dhcpderegisterparamchange","dhcpcsdk/DhcpDeRegisterParamChange"]
old-location: dhcp\dhcpderegisterparamchange.htm
tech.root: DHCP
ms.assetid: a3fa7c45-cad3-43be-a6c1-fffe6d025d95
ms.date: 12/05/2018
ms.keywords: DhcpDeRegisterParamChange, DhcpDeRegisterParamChange function [DHCP], _dhcp_dhcpderegisterparamchange, dhcp.dhcpderegisterparamchange, dhcpcsdk/DhcpDeRegisterParamChange
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
 - DhcpDeRegisterParamChange
 - dhcpcsdk/DhcpDeRegisterParamChange
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
 - DhcpDeRegisterParamChange
---

# DhcpDeRegisterParamChange function


## -description

The 
<b>DhcpDeRegisterParamChange</b> function releases resources associated with previously registered event notifications, and closes the associated event handle.

## -parameters

### -param Flags [in]

Reserved. Must be set to zero.

### -param Reserved [in]

Reserved. Must be set to <b>NULL</b>.

### -param Event [in]

Must be the same value as the <b>HANDLE</b> variable in the 
<a href="/previous-versions/windows/desktop/api/dhcpcsdk/nf-dhcpcsdk-dhcpregisterparamchange">DhcpRegisterParamChange</a> function call for which the client is deregistering event notification.

## -returns

Returns ERROR_SUCCESS upon successful completion. Otherwise, returns Windows error codes.

## -remarks

The 
<b>DhcpDeRegisterParamChange</b> function must be made subsequent to an associated 
<a href="/previous-versions/windows/desktop/api/dhcpcsdk/nf-dhcpcsdk-dhcpregisterparamchange">DhcpRegisterParamChange</a> function call, and the <i>Flags</i> parameter and the <b>HANDLE</b> variable passed  
in the <i>Event</i> parameter to <b>DhcpDeRegisterParamChange</b> must match corresponding <i>Flags</i> parameter and the <b>HANDLE</b> variable of the previous and associated 
<b>DhcpRegisterParamChange</b> function call.

## -see-also

<a href="/previous-versions/windows/desktop/dhcp/dhcp-functions">DHCP Functions</a>



<a href="/previous-versions/windows/desktop/api/dhcpcsdk/nf-dhcpcsdk-dhcpcapiinitialize">DhcpCApiInitialize</a>



<a href="/previous-versions/windows/desktop/api/dhcpcsdk/nf-dhcpcsdk-dhcpregisterparamchange">DhcpRegisterParamChange</a>