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

# SCOPE_LEVEL enumeration


## -description


The <b>SCOPE_LEVEL</b> enumeration is used with the <a href="https://msdn.microsoft.com/a2df3749-6c75-40c0-8952-1656bbe639a6">IP_ADAPTER_ADDRESSES</a> structure to identify scope levels for IPv6 addresses.


## -enum-fields




### -field ScopeLevelInterface

The scope is interface-level.


### -field ScopeLevelLink

The scope is link-level.


### -field ScopeLevelSubnet

The scope is subnet-level.


### -field ScopeLevelAdmin

The scope is admin-level.


### -field ScopeLevelSite

The scope is site-level.


### -field ScopeLevelOrganization

The scope is organization-level.


### -field ScopeLevelGlobal

The scope is global.


### -field ScopeLevelCount




## -remarks



The <b>SCOPE_LEVEL</b> enumeration is used in the <b>ZoneIndices</b> member of the <a href="https://msdn.microsoft.com/a2df3749-6c75-40c0-8952-1656bbe639a6">IP_ADAPTER_ADDRESSES</a>  structure.

On Windows Vista and later as well as on the Microsoft Windows Software Development Kit (SDK), the organization of header files has changed and the <b>SCOPE_LEVEL</b> enumeration type is defined in the <i>Ws2def.h</i> header file. Note that the <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/a2df3749-6c75-40c0-8952-1656bbe639a6">IP_ADAPTER_ADDRESSES</a>
 

 

