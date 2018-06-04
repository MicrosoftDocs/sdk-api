---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _DHCP_SERVER_OPTIONS structure


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

