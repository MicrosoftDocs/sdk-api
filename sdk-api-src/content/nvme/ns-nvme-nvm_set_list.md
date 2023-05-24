---
UID: NS:nvme.NVM_SET_LIST
tech.root: fs
title: NVM_SET_LIST
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains an array of entries for the NVME Set Attributes command.
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: nvme.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: 
req.target-type: 
req.typenames: NVM_SET_LIST, *PNVM_SET_LIST
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVM_SET_LIST
 - NVM_SET_LIST
f1_keywords:
 - PNVM_SET_LIST
 - nvme/PNVM_SET_LIST
 - NVM_SET_LIST
 - nvme/NVM_SET_LIST
dev_langs:
 - c++
---

# NVM_SET_LIST structure


## -description

Contains an array of entries for the NVME Set Attributes command.

## -struct-fields

### -field IdentifierCount

The number of identifiers in the entry.

### -field Reserved

### -field Entry

An array of [NVME_SET_ATTRIBUTES_ENTRY](ns-nvme-nvme_set_attributes_entry.md) structures that specify attribute values to be set by the set list.

## -remarks

## -see-also

