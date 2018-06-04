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

# _STORAGE_OFFLOAD_TOKEN structure


## -description


Contains the token used to represent a portion of a file used in by offload read and write operations specified 
    by <b>DeviceDsmAction_OffloadRead</b> or <b>DeviceDsmAction_OffloadWrite</b> 
    actions for the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff560573">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a> 
    control code.


## -struct-fields




### -field TokenType

A 32-bit unsigned integer which defines the type of <b>Token</b>.



#### STORAGE_OFFLOAD_TOKEN_TYPE_WELL_KNOWN (0xFFFFFFFF)

The <b>Token</b> member uses a well-known format. The first two bytes of the 
        <b>Token</b> member are a 16-bit unsigned integer that describes the region. 
        The possible values are either <b>STORAGE_OFFLOAD_PATTERN_ZERO</b> or 
        <b>STORAGE_OFFLOAD_PATTERN_ZERO_WITH_PROTECTION_INFO</b>. 
        <b>STORAGE_OFFLOAD_PATTERN_ZERO</b> (0x0001) is a well-known token that indicates that the 
        region represented has all bits set to zero. 
        <b>STORAGE_OFFLOAD_PATTERN_ZERO_WITH_PROTECTION_INFO</b> is a well-known token that indicates 
        that the data in the region represented has all bits set to zero and the corresponding protection information 
        is valid.



#### 0x00000000–0xFFFFFFFE

The <b>Token</b> member uses a vendor-specific format.


### -field Reserved

Reserved.


### -field TokenIdLength

The length of the token data in <b>Token</b>.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.StorageOffloadZeroDataToken


### -field DUMMYUNIONNAME.StorageOffloadZeroDataToken.Reserved2

Reserved.


### -field DUMMYUNIONNAME.Token

If the <b>TokenType</b> member is 
       <b>STORAGE_OFFLOAD_TOKEN_TYPE_WELL_KNOWN</b> then the first two bytes are a 16-bit unsigned 
       integer that describes the range. Otherwise this is a vendor-specific format.

