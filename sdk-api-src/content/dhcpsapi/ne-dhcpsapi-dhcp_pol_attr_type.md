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

# DHCP_POL_ATTR_TYPE enumeration


## -description


The <b>DHCP_POL_ATTR_TYPE</b> enumeration defines the attribute type for a condition in a DHCP server policy.


## -enum-fields




### -field DhcpAttrHWAddr

The condition is based on the hardware address (MAC address) present in the <b>chaddr</b> field of the DHCP message header as defined in <a href="http://www.ietf.org/rfc/rfc2131.txt">RFC2131</a>.


### -field DhcpAttrOption

The condition is based on a DHCP option.


### -field DhcpAttrSubOption

The condition is based on a DHCP sub-option


### -field DhcpAttrFqdn


### -field DhcpAttrFqdnSingleLabel




## -see-also




<a href="https://msdn.microsoft.com/99A36029-1CBD-4A93-B25A-A0239D1C08D7">DHCP_POL_COND</a>



<a href="https://msdn.microsoft.com/7c90625c-e6b5-475f-a9ea-0dfd27810f03">DhcpHlprAddV4PolicyCondition</a>
 

 

