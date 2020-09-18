---
UID: NS:clfs._CLS_ARCHIVE_DESCRIPTOR
title: CLS_ARCHIVE_DESCRIPTOR (clfs.h)
description: Used by the GetNextLogArchiveExtent function to return information about log archive extents.
helpviewer_keywords: ["*PCLFS_ARCHIVE_DESCRIPTOR","*PCLS_ARCHIVE_DESCRIPTOR","CLFS_ARCHIVE_DESCRIPTOR","CLFS_ARCHIVE_DESCRIPTOR structure [Files]","CLS_ARCHIVE_DESCRIPTOR","PCLFS_ARCHIVE_DESCRIPTOR","PCLFS_ARCHIVE_DESCRIPTOR structure pointer [Files]","PPCLFS_ARCHIVE_DESCRIPTOR","PPCLFS_ARCHIVE_DESCRIPTOR structure pointer [Files]","PPCLS_ARCHIVE_DESCRIPTOR","clfs/CLFS_ARCHIVE_DESCRIPTOR","clfs/PCLFS_ARCHIVE_DESCRIPTOR","clfs/PPCLFS_ARCHIVE_DESCRIPTOR","fs.clfs_archive_descriptor"]
old-location: fs\clfs_archive_descriptor.htm
tech.root: fs
ms.assetid: a2d50d1d-f4cb-48de-be73-4858adfa951f
ms.date: 12/05/2018
ms.keywords: '*PCLFS_ARCHIVE_DESCRIPTOR, *PCLS_ARCHIVE_DESCRIPTOR, CLFS_ARCHIVE_DESCRIPTOR, CLFS_ARCHIVE_DESCRIPTOR structure [Files], CLS_ARCHIVE_DESCRIPTOR, PCLFS_ARCHIVE_DESCRIPTOR, PCLFS_ARCHIVE_DESCRIPTOR structure pointer [Files], PPCLFS_ARCHIVE_DESCRIPTOR, PPCLFS_ARCHIVE_DESCRIPTOR structure pointer [Files], PPCLS_ARCHIVE_DESCRIPTOR, clfs/CLFS_ARCHIVE_DESCRIPTOR, clfs/PCLFS_ARCHIVE_DESCRIPTOR, clfs/PPCLFS_ARCHIVE_DESCRIPTOR, fs.clfs_archive_descriptor'
req.header: clfs.h
req.include-header: Clfsw32.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
req.typenames: CLS_ARCHIVE_DESCRIPTOR, *PCLS_ARCHIVE_DESCRIPTOR, PPCLS_ARCHIVE_DESCRIPTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLS_ARCHIVE_DESCRIPTOR
 - clfs/_CLS_ARCHIVE_DESCRIPTOR
 - PCLS_ARCHIVE_DESCRIPTOR
 - clfs/PCLS_ARCHIVE_DESCRIPTOR
 - CLS_ARCHIVE_DESCRIPTOR
 - clfs/CLS_ARCHIVE_DESCRIPTOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Clfs.h
api_name:
 - CLFS_ARCHIVE_DESCRIPTOR
---

# CLS_ARCHIVE_DESCRIPTOR structure


## -description

Used by the <a href="/windows/desktop/api/clfsw32/nf-clfsw32-getnextlogarchiveextent">GetNextLogArchiveExtent</a> function to return information about log archive extents.

## -struct-fields

### -field coffLow

The offset in the container  to the first byte of the archive extent.

### -field coffHigh

The offset in the container to the last byte of the archive extent.

### -field infoContainer

The container information structure  that describes the container associated with the archive extent. For more information, see <a href="/windows/desktop/api/clfs/ns-clfs-cls_container_information">CLFS_CONTAINER_INFORMATION</a>.

## -see-also

<a href="/windows/desktop/api/clfs/ns-clfs-cls_container_information">CLFS_CONTAINER_INFORMATION</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-getnextlogarchiveextent">GetNextLogArchiveExtent</a>