---
UID: NS:winefs._EFS_HASH_BLOB
title: EFS_HASH_BLOB (winefs.h)
description: Contains a certificate hash.
helpviewer_keywords: ["*PEFS_HASH_BLOB","EFS_HASH_BLOB","EFS_HASH_BLOB structure [Files]","PEFS_HASH_BLOB","PEFS_HASH_BLOB structure pointer [Files]","_win32_efs_hash_blob_str","base.efs_hash_blob_str","fs.efs_hash_blob_str","winefs/EFS_HASH_BLOB","winefs/PEFS_HASH_BLOB"]
old-location: fs\efs_hash_blob_str.htm
tech.root: fs
ms.assetid: 23a172be-6e94-4a1f-afde-fc9437443c7a
ms.date: 12/05/2018
ms.keywords: '*PEFS_HASH_BLOB, EFS_HASH_BLOB, EFS_HASH_BLOB structure [Files], PEFS_HASH_BLOB, PEFS_HASH_BLOB structure pointer [Files], _win32_efs_hash_blob_str, base.efs_hash_blob_str, fs.efs_hash_blob_str, winefs/EFS_HASH_BLOB, winefs/PEFS_HASH_BLOB'
req.header: winefs.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP Professional [desktop apps only]
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
req.typenames: EFS_HASH_BLOB, *PEFS_HASH_BLOB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EFS_HASH_BLOB
 - winefs/_EFS_HASH_BLOB
 - PEFS_HASH_BLOB
 - winefs/PEFS_HASH_BLOB
 - EFS_HASH_BLOB
 - winefs/EFS_HASH_BLOB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winefs.h
api_name:
 - EFS_HASH_BLOB
---

# EFS_HASH_BLOB structure


## -description

Contains a certificate hash.

## -struct-fields

### -field cbData

The number of bytes in the <b>pbData</b> buffer.

### -field cbData.range

### -field cbData.range.0

### -field cbData.range.100

### -field pbData

The certificate hash.

### -field pbData.size_is

### -field pbData.size_is.cbData

## -see-also

<a href="/windows/desktop/api/winefs/ns-winefs-encryption_certificate_hash">ENCRYPTION_CERTIFICATE_HASH</a>



<a href="/windows/desktop/FileIO/file-encryption">File Encryption</a>