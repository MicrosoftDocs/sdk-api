---
UID: NS:winioctl.USN_RECORD_EXTENT
title: USN_RECORD_EXTENT
description: Contains the offset and length for an update sequence number (USN) record extent.
helpviewer_keywords: ["*PUSN_RECORD_EXTENT","PUSN_RECORD_EXTENT","PUSN_RECORD_EXTENT structure pointer [Files]","USN_RECORD_EXTENT","USN_RECORD_EXTENT structure [Files]","fs.usn_record_extent","winioctl/PUSN_RECORD_EXTENT","winioctl/USN_RECORD_EXTENT"]
old-location: fs\usn_record_extent.htm
tech.root: fs
ms.assetid: 7D569FCB-06D4-4348-B75A-D087D1D37851
ms.date: 12/05/2018
ms.keywords: '*PUSN_RECORD_EXTENT, PUSN_RECORD_EXTENT, PUSN_RECORD_EXTENT structure pointer [Files], USN_RECORD_EXTENT, USN_RECORD_EXTENT structure [Files], fs.usn_record_extent, winioctl/PUSN_RECORD_EXTENT, winioctl/USN_RECORD_EXTENT'
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
req.typenames: USN_RECORD_EXTENT, *PUSN_RECORD_EXTENT
req.redist: 
f1_keywords:
 - PUSN_RECORD_EXTENT
 - winioctl/PUSN_RECORD_EXTENT
 - USN_RECORD_EXTENT
 - winioctl/USN_RECORD_EXTENT
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
 - USN_RECORD_EXTENT
---

# USN_RECORD_EXTENT structure


## -description

Contains the offset and length for an update sequence number (USN) record extent.

## -struct-fields

### -field Offset

The offset of the extent, in bytes.

### -field Length

The length of the extent, in bytes.

## -see-also

[USN_RECORD_V4 structure](ns-winioctl-usn_record_v4.md)



<a href="/windows/desktop/FileIO/volume-management-structures">Volume Management Structures</a>

