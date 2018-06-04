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

# _DHCP_SUBNET_STATE enumeration


## -description



      The <b>DHCP_SUBNET_STATE</b> enumeration defines the set of possible states for a subnet.


## -enum-fields




### -field DhcpSubnetEnabled

The subnet is enabled; the server will distribute addresses, extend leases, and release addresses within the subnet range to clients.


### -field DhcpSubnetDisabled

The subnet is disabled; the server will not distribute addresses or extend leases within the subnet range to clients. However, the server will still release addresses within the subnet range.


### -field DhcpSubnetEnabledSwitched

The subnet is enabled; the server will distribute addresses, extend leases, and release addresses within the subnet range to clients. The default gateway is set to the local machine itself. 


### -field DhcpSubnetDisabledSwitched

The subnet is disabled; the server will not distribute addresses or extend leases within the subnet range to clients. However, the server will still release addresses within the subnet range. The default gateway is set to the local machine itself.


### -field DhcpSubnetInvalidState

The subnet is in an invalid state.


## -see-also




<a href="https://msdn.microsoft.com/030b4743-7558-493c-931c-1ad28a6b435a">
        DHCP_SUBNET_INFO</a>
 

 

