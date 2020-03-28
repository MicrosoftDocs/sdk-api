---
UID: NE:winioctl._STORAGE_QUERY_TYPE
title: STORAGE_QUERY_TYPE
description: Used by the STORAGE_PROPERTY_QUERY structure passed to the IOCTL_STORAGE_QUERY_PROPERTY control code to indicate what information is returned about a property of a storage device or adapter.
old-location: fs\storage_query_type.htm
tech.root: FileIO
ms.assetid: 0bce42d2-9d42-4881-9e33-4b3858a40353
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_QUERY_TYPE, PSTORAGE_QUERY_TYPE, PSTORAGE_QUERY_TYPE enumeration pointer [Files], PropertyExistsQuery, PropertyMaskQuery, PropertyQueryMaxDefined, PropertyStandardQuery, STORAGE_QUERY_TYPE, STORAGE_QUERY_TYPE enumeration [Files], fs.storage_query_type, winioctl/PSTORAGE_QUERY_TYPE, winioctl/PropertyExistsQuery, winioctl/PropertyMaskQuery, winioctl/PropertyQueryMaxDefined, winioctl/PropertyStandardQuery, winioctl/STORAGE_QUERY_TYPE'
f1_keywords:
- winioctl/STORAGE_QUERY_TYPE
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- WinIoCtl.h
api_name:
- STORAGE_QUERY_TYPE
targetos: Windows
req.typenames: STORAGE_QUERY_TYPE, *PSTORAGE_QUERY_TYPE
req.redist: 
---

# STORAGE_QUERY_TYPE enumeration

## -description

Used by the [STORAGE_PROPERTY_QUERY](./ns-winioctl-storage_property_query.md) structure passed to the [IOCTL_STORAGE_QUERY_PROPERTY](./ni-winioctl-ioctl_storage_query_property.md) control code to indicate what information is returned about a property of a storage device or adapter.


## -enum-fields


### -field PropertyStandardQuery

Instructs the driver to return an appropriate descriptor.


### -field PropertyExistsQuery

Instructs the driver to report whether the descriptor is supported.


### -field PropertyMaskQuery

Not currently supported. Do not use.


### -field PropertyQueryMaxDefined

Specifies the upper limit of the list of query types. This is used to validate the query type.


## -see-also

* [Disk Management Enumeration Types](https://docs.microsoft.com/windows/desktop/FileIO/disk-management-enumeration-types)
* [IOCTL_STORAGE_QUERY_PROPERTY](https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property)
* [STORAGE_PROPERTY_ID](https://docs.microsoft.com/windows/desktop/api/winioctl/ne-winioctl-storage_property_id)
* [STORAGE_PROPERTY_QUERY](https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-storage_property_query)
