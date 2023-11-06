---
UID: NS:projectedfslib.PRJ_PLACEHOLDER_INFO
title: PRJ_PLACEHOLDER_INFO (projectedfslib.h)
description: A buffer of metadata for the placeholder file or directory.
helpviewer_keywords: ["PRJ_PLACEHOLDER_INFO","PRJ_PLACEHOLDER_INFO structure","ProjFS.prj_placeholder_info","projectedfslib/PRJ_PLACEHOLDER_INFO"]
old-location: projfs\prj_placeholder_info.htm
tech.root: ProjFS
ms.assetid: 84F510F6-7192-4B0D-A063-CE99B54ED7DD
ms.date: 12/05/2018
ms.keywords: PRJ_PLACEHOLDER_INFO, PRJ_PLACEHOLDER_INFO structure, ProjFS.prj_placeholder_info, projectedfslib/PRJ_PLACEHOLDER_INFO
req.header: projectedfslib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
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
req.typenames: PRJ_PLACEHOLDER_INFO
req.redist: 
ms.custom: RS5, 19H1
f1_keywords:
 - PRJ_PLACEHOLDER_INFO
 - projectedfslib/PRJ_PLACEHOLDER_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - projectedfslib.h
api_name:
 - PRJ_PLACEHOLDER_INFO
---

## -description

A buffer of metadata for the placeholder file or directory.

## -struct-fields

### -field FileBasicInfo

A structure that supplies basic information about the item: the size of the file in bytes (should be zero if the IsDirectory field is set to TRUE), the item’s timestamps, and its attributes.

### -field EaInformation

A structure that supplies extended attribute (EA) information about the item.

### -field EaInformation.EaBufferSize

The size in bytes of the extended attribute buffer. If there is no extended attribute information, this must be set to 0.

### -field EaInformation.OffsetToFirstEa

The offset, in bytes, from the start of the <b>PRJ_PLACEHOLDER_INFO</b> structure to the first FILE_FULL_EA_INFORMATION entry.

### -field SecurityInformation

Supplies custom security descriptor information about the item.

### -field SecurityInformation.SecurityBufferSize

The size, in bytes, of the custom security descriptor. If there is no custom security descriptor, this must be set to 0.

### -field SecurityInformation.OffsetToSecurityDescriptor

Specifies the offset, in bytes,  from the start of the <b>PRJ_PLACEHOLDER_INFO</b> structure to the SECURITY_DESCRIPTOR structure.

### -field StreamsInformation

Supplies information about alternate data streams for the item.

### -field StreamsInformation.StreamsInfoBufferSize

The size, in bytes, of alternate data stream information for the placeholder. If there are no alternate data streams, this must be set to 0.

### -field StreamsInformation.OffsetToFirstStreamInfo

The offset, in bytes, from the start of the <b>PRJ_PLACEHOLDER_INFO</b> structure to the first FILE_STREAM_INFORMATION entry.

### -field VariableData

Start of the variable-length buffer to hold EAs, a custom security descriptor, and alternate data stream information.

### -field versionInfo

Version information for the placeholder (see <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder">PrjMarkDirectoryAsPlaceholder</a> for more information on PRJ_PLACEHOLDER_VERSION_INFO).
