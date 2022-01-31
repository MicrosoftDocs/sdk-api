---
UID: NE:winioctl._STORAGE_QUERY_TYPE
title: STORAGE_QUERY_TYPE
description: Used by the STORAGE_PROPERTY_QUERY structure passed to the IOCTL_STORAGE_QUERY_PROPERTY control code to indicate what information is returned about a property of a storage device or adapter.
helpviewer_keywords: ["*PSTORAGE_QUERY_TYPE","PSTORAGE_QUERY_TYPE","PSTORAGE_QUERY_TYPE enumeration pointer [Files]","PropertyExistsQuery","PropertyMaskQuery","PropertyQueryMaxDefined","PropertyStandardQuery","STORAGE_QUERY_TYPE","STORAGE_QUERY_TYPE enumeration [Files]","fs.storage_query_type","winioctl/PSTORAGE_QUERY_TYPE","winioctl/PropertyExistsQuery","winioctl/PropertyMaskQuery","winioctl/PropertyQueryMaxDefined","winioctl/PropertyStandardQuery","winioctl/STORAGE_QUERY_TYPE"]
old-location: fs\storage_query_type.htm
tech.root: fs
ms.assetid: 0bce42d2-9d42-4881-9e33-4b3858a40353
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_QUERY_TYPE, PSTORAGE_QUERY_TYPE, PSTORAGE_QUERY_TYPE enumeration pointer [Files], PropertyExistsQuery, PropertyMaskQuery, PropertyQueryMaxDefined, PropertyStandardQuery, STORAGE_QUERY_TYPE, STORAGE_QUERY_TYPE enumeration [Files], fs.storage_query_type, winioctl/PSTORAGE_QUERY_TYPE, winioctl/PropertyExistsQuery, winioctl/PropertyMaskQuery, winioctl/PropertyQueryMaxDefined, winioctl/PropertyStandardQuery, winioctl/STORAGE_QUERY_TYPE'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: STORAGE_QUERY_TYPE, *PSTORAGE_QUERY_TYPE
req.redist: 
f1_keywords:
 - _STORAGE_QUERY_TYPE
 - winioctl/_STORAGE_QUERY_TYPE
 - PSTORAGE_QUERY_TYPE
 - winioctl/PSTORAGE_QUERY_TYPE
 - STORAGE_QUERY_TYPE
 - winioctl/STORAGE_QUERY_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - STORAGE_QUERY_TYPE
---

# STORAGE_QUERY_TYPE enumeration


## -description

Used by the [STORAGE_PROPERTY_QUERY](ns-winioctl-storage_property_query.md) structure passed to the [IOCTL_STORAGE_QUERY_PROPERTY](ni-winioctl-ioctl_storage_query_property.md) control code to indicate what information is returned about a property of a storage device or adapter.

## -enum-fields

### -field PropertyStandardQuery:0

Instructs the driver to return an appropriate descriptor.

### -field PropertyExistsQuery

Instructs the driver to report whether the descriptor is supported.

### -field PropertyMaskQuery

Not currently supported. Do not use.

### -field PropertyQueryMaxDefined

Specifies the upper limit of the list of query types. This is used to validate the query type.

## -see-also

* [Disk Management Enumeration Types](/windows/desktop/FileIO/disk-management-enumeration-types)
* [IOCTL_STORAGE_QUERY_PROPERTY](ni-winioctl-ioctl_storage_query_property.md)
* [STORAGE_PROPERTY_ID](ne-winioctl-storage_property_id.md)
* [STORAGE_PROPERTY_QUERY](ns-winioctl-storage_property_query.md)
