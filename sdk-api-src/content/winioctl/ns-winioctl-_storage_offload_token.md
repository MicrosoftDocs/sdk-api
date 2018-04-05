---
UID: NS:winioctl._STORAGE_OFFLOAD_TOKEN
title: "_STORAGE_OFFLOAD_TOKEN"
author: windows-driver-content
description: The token used to represent a portion of a file used in by offload read and write operations.
old-location: base\storage_offload_token.htm
old-project: DevIO
ms.assetid: e33550d6-8d98-4fbb-8e61-d309f0e8e867
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PSTORAGE_OFFLOAD_TOKEN, PSTORAGE_OFFLOAD_TOKEN, PSTORAGE_OFFLOAD_TOKEN structure pointer, STORAGE_OFFLOAD_TOKEN, STORAGE_OFFLOAD_TOKEN structure, STORAGE_OFFLOAD_TOKEN_TYPE_WELL_KNOWN, _STORAGE_OFFLOAD_TOKEN, base.storage_offload_token, winioctl/PSTORAGE_OFFLOAD_TOKEN, winioctl/STORAGE_OFFLOAD_TOKEN"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: STORAGE_OFFLOAD_TOKEN, *PSTORAGE_OFFLOAD_TOKEN
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoCtl.h
api_name:
-	STORAGE_OFFLOAD_TOKEN
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _STORAGE_OFFLOAD_TOKEN structure


## -description


Contains the token used to represent a portion of a file used in by offload read and write operations specified 
    by <b>DeviceDsmAction_OffloadRead</b> or <b>DeviceDsmAction_OffloadWrite</b> 
    actions for the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff560573">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a> 
    control code.


## -struct-fields




### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.StorageOffloadZeroDataToken


### -field DUMMYUNIONNAME.StorageOffloadZeroDataToken.Reserved2

Reserved.


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


#### - Token

If the <b>TokenType</b> member is 
       <b>STORAGE_OFFLOAD_TOKEN_TYPE_WELL_KNOWN</b> then the first two bytes are a 16-bit unsigned 
       integer that describes the range. Otherwise this is a vendor-specific format.

