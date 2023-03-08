---
UID: NS:winioctl._STORAGE_RPMB_DESCRIPTOR
title: STORAGE_RPMB_DESCRIPTOR
description: The STORAGE_RPMB_DESCRIPTOR structure (winioctl.h) describes whether the device contains an RPMB and the max payload size the RPMB supports.
ms.date: 08/09/2022
ms.keywords: _STORAGE_RPMB_DESCRIPTOR, STORAGE_RPMB_DESCRIPTOR
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: winioctl.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: STORAGE_RPMB_DESCRIPTOR, *PSTORAGE_RPMB_DESCRIPTOR
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - _STORAGE_RPMB_DESCRIPTOR
 - winioctl/_STORAGE_RPMB_DESCRIPTOR
 - PSTORAGE_RPMB_DESCRIPTOR
 - winioctl/PSTORAGE_RPMB_DESCRIPTOR
 - STORAGE_RPMB_DESCRIPTOR
 - winioctl/STORAGE_RPMB_DESCRIPTOR
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - winioctl.h
api_name:
 - _STORAGE_RPMB_DESCRIPTOR
 - STORAGE_RPMB_DESCRIPTOR
---

## -description

To interface with the Replay Protected Memory Block (RPMB), applications first need to query whether the device contains an RPMB and the max payload size the RPMB supports. To do this, the application sends [IOCTL_STORAGE_QUERY_PROPERTY IOCTL](ni-winioctl-ioctl_storage_query_property.md) with [STORAGE_PROPERTY_ID enumeration](ne-winioctl-storage_property_id.md) set to StorageAdapterRpmbProperty (defined in STORAGE_PROPERTY_QUERY in ntddstor.h). Storport then responds with the following payload (defined in ntddstor.h) when [STORAGE_QUERY_TYPE enumeration](ne-winioctl-storage_query_type.md) is set to PropertyStandardQuery.

## -struct-fields

### -field Version

Shall be set to STORAGE_RPMB_DESCRIPTOR_VERSION_1

### -field Size

Shall be set to sizeof(STORAGE_RPMB_DESCRIPTOR)

### -field SizeInBytes

The size of the RPMB, in bytes. 0 if not supported, RPMB size in bytes otherwise.

### -field MaxReliableWriteSizeInBytes

The maximum amount of data supported in one transaction in bytes. 0 if not supported, minimum 512 bytes.

### -field FrameFormat

To support different RPMB frame formats, specifies which frame format the payload will be in so the port driver can take the appropriate action.

## -remarks

## -see-also
