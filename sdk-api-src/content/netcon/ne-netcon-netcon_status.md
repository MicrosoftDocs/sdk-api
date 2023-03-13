---
UID: NE:netcon.tagNETCON_STATUS
title: NETCON_STATUS (netcon.h)
description: The NETCON_STATUS type enumerates possible status conditions for a network connection.
helpviewer_keywords: ["NCS_AUTHENTICATING","NCS_AUTHENTICATION_FAILED","NCS_AUTHENTICATION_SUCCEEDED","NCS_CONNECTED","NCS_CONNECTING","NCS_CREDENTIALS_REQUIRED","NCS_DISCONNECTED","NCS_DISCONNECTING","NCS_HARDWARE_DISABLED","NCS_HARDWARE_MALFUNCTION","NCS_HARDWARE_NOT_PRESENT","NCS_INVALID_ADDRESS","NCS_MEDIA_DISCONNECTED","NETCON_STATUS","NETCON_STATUS enumeration [ICS/ICF]","_ics_netcon_status","ics.netcon_status","netcon/NCS_AUTHENTICATING","netcon/NCS_AUTHENTICATION_FAILED","netcon/NCS_AUTHENTICATION_SUCCEEDED","netcon/NCS_CONNECTED","netcon/NCS_CONNECTING","netcon/NCS_CREDENTIALS_REQUIRED","netcon/NCS_DISCONNECTED","netcon/NCS_DISCONNECTING","netcon/NCS_HARDWARE_DISABLED","netcon/NCS_HARDWARE_MALFUNCTION","netcon/NCS_HARDWARE_NOT_PRESENT","netcon/NCS_INVALID_ADDRESS","netcon/NCS_MEDIA_DISCONNECTED","netcon/NETCON_STATUS"]
old-location: ics\netcon_status.htm
tech.root: ics
ms.assetid: feb0aa60-b873-4536-8ec2-2dce4d355fdb
ms.date: 12/05/2018
ms.keywords: NCS_AUTHENTICATING, NCS_AUTHENTICATION_FAILED, NCS_AUTHENTICATION_SUCCEEDED, NCS_CONNECTED, NCS_CONNECTING, NCS_CREDENTIALS_REQUIRED, NCS_DISCONNECTED, NCS_DISCONNECTING, NCS_HARDWARE_DISABLED, NCS_HARDWARE_MALFUNCTION, NCS_HARDWARE_NOT_PRESENT, NCS_INVALID_ADDRESS, NCS_MEDIA_DISCONNECTED, NETCON_STATUS, NETCON_STATUS enumeration [ICS/ICF], _ics_netcon_status, ics.netcon_status, netcon/NCS_AUTHENTICATING, netcon/NCS_AUTHENTICATION_FAILED, netcon/NCS_AUTHENTICATION_SUCCEEDED, netcon/NCS_CONNECTED, netcon/NCS_CONNECTING, netcon/NCS_CREDENTIALS_REQUIRED, netcon/NCS_DISCONNECTED, netcon/NCS_DISCONNECTING, netcon/NCS_HARDWARE_DISABLED, netcon/NCS_HARDWARE_MALFUNCTION, netcon/NCS_HARDWARE_NOT_PRESENT, netcon/NCS_INVALID_ADDRESS, netcon/NCS_MEDIA_DISCONNECTED, netcon/NETCON_STATUS
req.header: netcon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: NETCON_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNETCON_STATUS
 - netcon/tagNETCON_STATUS
 - NETCON_STATUS
 - netcon/NETCON_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - NetCon.h
api_name:
 - NETCON_STATUS
---

# NETCON_STATUS enumeration


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>NETCON_STATUS</b> type enumerates possible status conditions for a network connection.

## -enum-fields

### -field NCS_DISCONNECTED:0

The connection is disconnected.

### -field NCS_CONNECTING

The connection is in the process of connecting.

### -field NCS_CONNECTED

The connection is in a connected state.

### -field NCS_DISCONNECTING

The connection is in the process of disconnecting.

### -field NCS_HARDWARE_NOT_PRESENT

The hardware for the connection, for example network interface card (NIC), is not present.

### -field NCS_HARDWARE_DISABLED

The hardware for the connection is present, but is not enabled.

### -field NCS_HARDWARE_MALFUNCTION

A malfunction has occurred in the hardware for the connection.

### -field NCS_MEDIA_DISCONNECTED

The media, for example the network cable, is disconnected.

### -field NCS_AUTHENTICATING

The connection is waiting for authentication to occur.

### -field NCS_AUTHENTICATION_SUCCEEDED

Authentication has succeeded on this connection.

### -field NCS_AUTHENTICATION_FAILED

Authentication has failed on this connection.

### -field NCS_INVALID_ADDRESS

The address is invalid.

### -field NCS_CREDENTIALS_REQUIRED

Security credentials are required.

### -field NCS_ACTION_REQUIRED

### -field NCS_ACTION_REQUIRED_RETRY

### -field NCS_CONNECT_FAILED

## -see-also

<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetconnection">INetConnection</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-enumeration-types">Internet Connection Sharing and Internet Connection Firewall Enumeration Types</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>



<a href="/windows/desktop/api/netcon/ns-netcon-netcon_properties">NETCON_PROPERTIES</a>
