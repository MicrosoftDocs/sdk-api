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

# _DHCP_CLASS_INFO_V6 structure


## -description


The <b>DHCP_CLASS_INFO_V6</b> structure contains the information for a particular DHCPv6 user class or vendor class.


## -struct-fields




### -field ClassName

A pointer to a null-terminated Unicode string that contains the class name.


### -field ClassComment

A pointer to a null-terminated Unicode string that contains the comment for the class.


### -field ClassDataLength

The length of data as pointed to by <b>ClassData</b>.


### -field IsVendor

If <b>TRUE</b>, this information applies to a vendor class; if <b>FALSE</b>, it applies to a user class.


### -field EnterpriseNumber

 The vendor class identifier. It is default (0x00000000) for user class.


### -field Flags

This field MUST be set to zero (0x00000000) when sending and ignored on receipt.


### -field ClassData

Pointer to a BYTE blob that contains an array of bytes of length specified by <b>ClassDataLength</b>. This contains opaque data regarding a user class or a vendor class.


### -field ClassData.size_is

 


### -field ClassData.size_is.ClassDataLength

 



