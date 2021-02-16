---
UID: NS:winioctl._STORAGE_MEDIUM_PRODUCT_TYPE_DESCRIPTOR
title: STORAGE_MEDIUM_PRODUCT_TYPE_DESCRIPTOR
description: Used in conjunction with the IOCTL_STORAGE_QUERY_PROPERTY request to describe the product type of a storage device.
helpviewer_keywords: ["*PSTORAGE_MEDIUM_PRODUCT_TYPE_DESCRIPTOR","PSTORAGE_MEDIUM_PRODUCT_TYPE_DESCRIPTOR","PSTORAGE_MEDIUM_PRODUCT_TYPE_DESCRIPTOR structure pointer [Files]","STORAGE_MEDIUM_PRODUCT_TYPE_DESCRIPTOR","STORAGE_MEDIUM_PRODUCT_TYPE_DESCRIPTOR structure [Files]","fs.storage_medium_product_type_descriptor","winioctl/PSTORAGE_MEDIUM_PRODUCT_TYPE_DESCRIPTOR","winioctl/STORAGE_MEDIUM_PRODUCT_TYPE_DESCRIPTOR"]
old-location: fs\storage_medium_product_type_descriptor.htm
tech.root: fs
ms.assetid: 4845F541-D822-4DD0-8F52-9923B067A4F8
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_MEDIUM_PRODUCT_TYPE_DESCRIPTOR, PSTORAGE_MEDIUM_PRODUCT_TYPE_DESCRIPTOR, PSTORAGE_MEDIUM_PRODUCT_TYPE_DESCRIPTOR structure pointer [Files], STORAGE_MEDIUM_PRODUCT_TYPE_DESCRIPTOR, STORAGE_MEDIUM_PRODUCT_TYPE_DESCRIPTOR structure [Files], fs.storage_medium_product_type_descriptor, winioctl/PSTORAGE_MEDIUM_PRODUCT_TYPE_DESCRIPTOR, winioctl/STORAGE_MEDIUM_PRODUCT_TYPE_DESCRIPTOR'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.typenames: STORAGE_MEDIUM_PRODUCT_TYPE_DESCRIPTOR, *PSTORAGE_MEDIUM_PRODUCT_TYPE_DESCRIPTOR
req.redist: 
f1_keywords:
 - _STORAGE_MEDIUM_PRODUCT_TYPE_DESCRIPTOR
 - winioctl/_STORAGE_MEDIUM_PRODUCT_TYPE_DESCRIPTOR
 - PSTORAGE_MEDIUM_PRODUCT_TYPE_DESCRIPTOR
 - winioctl/PSTORAGE_MEDIUM_PRODUCT_TYPE_DESCRIPTOR
 - STORAGE_MEDIUM_PRODUCT_TYPE_DESCRIPTOR
 - winioctl/STORAGE_MEDIUM_PRODUCT_TYPE_DESCRIPTOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winioctl.h
api_name:
 - STORAGE_MEDIUM_PRODUCT_TYPE_DESCRIPTOR
---

# STORAGE_MEDIUM_PRODUCT_TYPE_DESCRIPTOR structure


## -description

Used in conjunction with the <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a> request to describe the product type of a storage device.

## -struct-fields

### -field Version

Contains the size of this structure, in bytes, as defined by <code>Sizeof(STORAGE_MEDIUM_PRODUCT_TYPE_DESCRIPTOR)</code>. The value of this member will change as members are added to 
      the structure.

### -field Size

Specifies the total size of the data returned, in bytes. This may include data that follows this 
      structure.

### -field MediumProductType

Specifies the product type of the storage device.

<table>
<tr>
<th><b>MediumProductType</b> value</th>
<th>Description</th>
</tr>
<tr>
<td><code>00h</code></td>
<td>Not indicated</td>
</tr>
<tr>
<td><code>01h</code></td>
<td>CFast</td>
</tr>
<tr>
<td><code>02h</code></td>
<td>CompactFlash</td>
</tr>
<tr>
<td><code>03h</code></td>
<td>Memory Stick</td>
</tr>
<tr>
<td><code>04h</code></td>
<td>MultiMediaCard</td>
</tr>
<tr>
<td><code>05h</code></td>
<td>Secure Digital Card (SD Card)</td>
</tr>
<tr>
<td><code>06h</code></td>
<td>QXD</td>
</tr>
<tr>
<td><code>07h</code></td>
<td>Universal Flash Storage</td>
</tr>
<tr>
<td><code>08h</code> to <code>EFh</code></td>
<td>Reserved</td>
</tr>
<tr>
<td><code>F0h</code> to <code>FFh</code></td>
<td>Vendor-specific</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a>