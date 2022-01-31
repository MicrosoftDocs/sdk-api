---
UID: NE:iscsidsc.__unnamed_enum_0
title: ISCSI_DIGEST_TYPES (iscsidsc.h)
description: ISCSI_DIGEST_TYPES enumeration indicates the digest type.
helpviewer_keywords: ["*PISCSI_DIGEST_TYPES","ISCSI_DIGEST_TYPES","ISCSI_DIGEST_TYPES enumeration [iSCSI Discovery Library API]","ISCSI_DIGEST_TYPE_CRC32C","ISCSI_DIGEST_TYPE_NONE","iscsidisc.iscsi_digest_types","iscsidsc/ISCSI_DIGEST_TYPES","iscsidsc/ISCSI_DIGEST_TYPE_CRC32C","iscsidsc/ISCSI_DIGEST_TYPE_NONE"]
old-location: iscsidisc\iscsi_digest_types.htm
tech.root: iSCSIDisc
ms.assetid: 7c89cc19-28ae-472f-9400-9bd8d0f10c63
ms.date: 12/05/2018
ms.keywords: '*PISCSI_DIGEST_TYPES, ISCSI_DIGEST_TYPES, ISCSI_DIGEST_TYPES enumeration [iSCSI Discovery Library API], ISCSI_DIGEST_TYPE_CRC32C, ISCSI_DIGEST_TYPE_NONE, iscsidisc.iscsi_digest_types, iscsidsc/ISCSI_DIGEST_TYPES, iscsidsc/ISCSI_DIGEST_TYPE_CRC32C, iscsidsc/ISCSI_DIGEST_TYPE_NONE'
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: ISCSI_DIGEST_TYPES, *PISCSI_DIGEST_TYPES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PISCSI_DIGEST_TYPES
 - iscsidsc/PISCSI_DIGEST_TYPES
 - ISCSI_DIGEST_TYPES
 - iscsidsc/ISCSI_DIGEST_TYPES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iscsidsc.h
api_name:
 - ISCSI_DIGEST_TYPES
---

# ISCSI_DIGEST_TYPES enumeration


## -description

The <b>ISCSI_DIGEST_TYPES</b> enumeration indicates the digest type.

## -enum-fields

### -field ISCSI_DIGEST_TYPE_NONE:0

No digest is in use for guaranteeing data integrity.

### -field ISCSI_DIGEST_TYPE_CRC32C:1

The digest for guaranteeing data integrity uses a 32-bit cyclic redundancy check.

