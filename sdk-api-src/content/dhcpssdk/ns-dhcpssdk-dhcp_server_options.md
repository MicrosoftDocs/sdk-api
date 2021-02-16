---
UID: NS:dhcpssdk._DHCP_SERVER_OPTIONS
title: DHCP_SERVER_OPTIONS (dhcpssdk.h)
description: The DHCP_SERVER_OPTIONS structure specifies requested DHCP Server options.
helpviewer_keywords: ["*LPDHCP_SERVER_OPTIONS","*LPDHCP_SERVER_OPTIONS structure [DHCP]","DHCP_SERVER_OPTIONS","DHCP_SERVER_OPTIONS structure [DHCP]","dhcp.dhcp_server_options","dhcpssdk/*LPDHCP_SERVER_OPTIONS","dhcpssdk/DHCP_SERVER_OPTIONS"]
old-location: dhcp\dhcp_server_options.htm
tech.root: DHCP
ms.assetid: 0c43c2ad-ac9a-43b4-b750-a3f52c025ae2
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_SERVER_OPTIONS, *LPDHCP_SERVER_OPTIONS structure [DHCP], DHCP_SERVER_OPTIONS, DHCP_SERVER_OPTIONS structure [DHCP], dhcp.dhcp_server_options, dhcpssdk/*LPDHCP_SERVER_OPTIONS, dhcpssdk/DHCP_SERVER_OPTIONS'
req.header: dhcpssdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DHCP_SERVER_OPTIONS, *LPDHCP_SERVER_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_SERVER_OPTIONS
 - dhcpssdk/_DHCP_SERVER_OPTIONS
 - LPDHCP_SERVER_OPTIONS
 - dhcpssdk/LPDHCP_SERVER_OPTIONS
 - DHCP_SERVER_OPTIONS
 - dhcpssdk/DHCP_SERVER_OPTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpssdk.h
api_name:
 - DHCP_SERVER_OPTIONS
---

# DHCP_SERVER_OPTIONS structure


## -description

The <b>DHCP_SERVER_OPTIONS</b> structure specifies requested DHCP Server options.

## -struct-fields

### -field MessageType

DHCP message type.

### -field SubnetMask

Subnet mask.

### -field RequestedAddress

Requested IP address.

### -field RequestLeaseTime

Requested duration of the IP address lease, in seconds.

### -field OverlayFields

Overlay fields to apply to the request.

### -field RouterAddress

IP address of the default gateway.

### -field Server

IP address of the DHCP Server.

### -field ParameterRequestList

List of requested parameters.

### -field ParameterRequestListLength

Length of <i>ParameterRequestList</i>, in bytes.

### -field MachineName

Machine name (host name) of the computer making the request.

### -field MachineNameLength

Length of <i>MachineName</i>, in bytes.

### -field ClientHardwareAddressType

Type of hardware address expressed in <i>ClientHardwareAddress</i>.

### -field ClientHardwareAddressLength

Length of <i>ClientHardwareAddress</i>, in bytes.

### -field ClientHardwareAddress

Client hardware address.

### -field ClassIdentifier

Class identifier for the client.

### -field ClassIdentifierLength

Length of <i>ClassIdentifier</i>, in bytes.

### -field VendorClass

Vendor class, if applicable.

### -field VendorClassLength

Length of <i>VendorClass</i>, in bytes.

### -field DNSFlags

Flags used for DNS.

### -field DNSNameLength

Length of <i>DNSName</i>, in bytes.

### -field DNSName

Pointer to the DNS name.

### -field DSDomainNameRequested

Specifies whether the domain name is requested.

### -field DSDomainName

Pointer to the domain name.

### -field DSDomainNameLen

Length of <i>DSDomainName</i>, in characters.

### -field ScopeId

Scope identifier for the IP address.

