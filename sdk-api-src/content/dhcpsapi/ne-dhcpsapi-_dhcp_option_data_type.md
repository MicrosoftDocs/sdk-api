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

# _DHCP_OPTION_DATA_TYPE enumeration


## -description



      The <b>DHCP_OPTION_DATA_TYPE</b> enumeration defines the set of formats that represent DHCP  option data.


## -enum-fields




### -field DhcpByteOption

The option data is stored as a BYTE value.


### -field DhcpWordOption

The option data is stored as a WORD value.


### -field DhcpDWordOption

The option data is stored as a DWORD value.


### -field DhcpDWordDWordOption

The option data is stored as a DWORD_DWORD value.


### -field DhcpIpAddressOption

The option data is an IP address, stored as a <a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value (DWORD).


### -field DhcpStringDataOption

The option data is stored as a Unicode string.


### -field DhcpBinaryDataOption

The option data is stored as a <a href="https://msdn.microsoft.com/0afdddb4-12f9-4c0b-937a-2cc311c126b4">DHCP_BINARY_DATA</a> structure.


### -field DhcpEncapsulatedDataOption

The option data is encapsulated and stored as a <a href="https://msdn.microsoft.com/0afdddb4-12f9-4c0b-937a-2cc311c126b4">DHCP_BINARY_DATA</a> structure.


### -field DhcpIpv6AddressOption

The option data is stored as a Unicode string.


## -see-also




<a href="https://msdn.microsoft.com/0afdddb4-12f9-4c0b-937a-2cc311c126b4">DHCP_BINARY_DATA</a>
 

 

