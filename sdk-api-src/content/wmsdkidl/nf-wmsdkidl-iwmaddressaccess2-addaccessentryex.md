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

# IWMAddressAccess2::AddAccessEntryEx


## -description



The <b>AddAccessEntryEx</b> method adds an entry to the IP address access list.




## -parameters




### -param aeType [in]

A member of the <a href="https://msdn.microsoft.com/514e6745-c521-41bd-81c2-b6c24cfb0192">WM_AETYPE</a> enumeration specifying the specifying the access permissions (exclusion or inclusion).


### -param bstrAddress [in]

Specifies an IP address as a <b>BSTR</b>, using standard "dot" notation. Both IPv4 and IPv6 addresses are supported. For example, <code>206.73.118.1</code> is an IPv4 address and <code>fe80::201:3ff:fee8:5058</code> is an IPv6 address.


### -param bstrMask [in]

Bit mask that defines which bits in the IP address are matched against. For example, if the IP address is <code>206.73.118.1</code> and the mask is <code>255.255.255.0</code>, only the first 24 bits of the address are examined. Thus, any IP addresses in the range 206.73.118.<i>XXX</i> would match this entry.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/609a20a7-e1a3-4889-abf3-4a6defc7739a">IWMAddressAccess2 Interface</a>
 

 

