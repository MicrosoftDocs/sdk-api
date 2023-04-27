---
UID: NE:nvme.NVME_SECURE_ERASE_SETTINGS
tech.root: fs
title: NVME_SECURE_ERASE_SETTINGS
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains values that specify whether or what type of a secure erase operation should be performed as part of a Format NVM command.
req.construct-type: enumeration
req.ddi-compliance: 
req.header: nvme.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - NVME_SECURE_ERASE_SETTINGS
f1_keywords:
 - NVME_SECURE_ERASE_SETTINGS
 - nvme/NVME_SECURE_ERASE_SETTINGS
dev_langs:
 - c++
---

# NVME_SECURE_ERASE_SETTINGS enumeration


## -description

Contains values that specify whether or what type of a secure erase operation should be performed as part of a Format NVM command.

The secure erase applies to all user data, regardless of location. For example, user data within an exposed Logical Block Allocation (LBA), within a cache, or within deallocated LBAs.

## -enum-fields

### -field NVME_SECURE_ERASE_NONE

No secure erase operation is requested.

### -field NVME_SECURE_ERASE_USER_DATA

All user data will be erased. Contents of the user data after the erase is indeterminate. For example, the user data may be zero filled or one filled. The controller may perform a cryptographic erase when **NVME_SECURE_ERASE_USER_DATA** is specified, if all user data is encrypted.

### -field NVME_SECURE_ERASE_CRYPTOGRAPHIC

All user data will be erased cryptographically. This is accomplished by deleting the encryption key.

## -remarks

Use this enumeration to specify values in the **SES** field of the [NVME_CDW10_FORMAT_NVM](ns-nvme-nvme_cdw10_format_nvm.md) structure that is used in the [FORMAT NVM (FORMATNVM)](ns-nvme-nvme_command.md) Admin command.

## -see-also

