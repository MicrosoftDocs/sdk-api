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

# __MIDL___MIDL_itf_wdstptmgmt_0000_0000_0007 enumeration


## -description


Indicates the source from which the WDS multicast provider obtains a multicast address for a new session.


## -enum-fields




### -field WdsTptIpAddressSourceUnknown

Default value that indicates that the IP address source is not known.


### -field WdsTptIpAddressSourceDhcp

Indicates that the server should use the <a href="https://msdn.microsoft.com/be313f7a-6332-4601-98b2-01561582213b">Multicast Address Dynamic Client Allocation Protocol</a> (MADCAP) to obtain a multicast IP address. MADCAP is a protocol that enables applications to obtain, renew, and release multicast addresses, and its functionality is often included in DHCP servers, such as the Microsoft DHCP Server role.


### -field WdsTptIpAddressSourceRange

Indicates that the server should automatically select an available address from a multicast address range manually configured by the administrator.

