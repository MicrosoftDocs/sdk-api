---
UID: NS:nvme.NVME_CDW10_FORMAT_NVM
tech.root: fs
title: NVME_CDW10_FORMAT_NVM
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains parameters for the Format NVM command that is used to low level format the NVM media.
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
req.typenames: NVME_CDW10_FORMAT_NVM, *PNVME_CDW10_FORMAT_NVM
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW10_FORMAT_NVM
 - NVME_CDW10_FORMAT_NVM
f1_keywords:
 - PNVME_CDW10_FORMAT_NVM
 - nvme/PNVME_CDW10_FORMAT_NVM
 - NVME_CDW10_FORMAT_NVM
 - nvme/NVME_CDW10_FORMAT_NVM
dev_langs:
 - c++
---

# NVME_CDW10_FORMAT_NVM structure


## -description

Contains parameters for the Format NVM command that is used to low level format the NVM media.

This command is used when the host wants to change the Logical Block Address (LBA) data size and/or metadata size. A low level format may destroy all data and metadata associated with all namespaces or only the specific namespace associated with the command (refer to the Format NVM Attributes in the Optional Admin Command Support (**OACS**) field of the [Identify Controller](ns-nvme-nvme_identify_controller_data.md) data structure). After the Format NVM command successfully completes, the controller will not return any user data that was previously contained in an affected namespace.

The Format NVM command uses the Command Dword 10 **CDW10** field in the **FORMATNVM** parameter of the [Command](ns-nvme-nvme_command.md) structure. All other command specific fields are reserved.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.LBAF

An [NVME_LBA_FORMAT](ns-nvme-nvme_lba_format.md) value that specifies the LBA format to apply to the NVM media. Only supported LBA formats can be selected. This value corresponds to the **LBAF** field in the [NVME_IDENTIFY_NAMESPACE_DATA](../nvme/ns-nvme-nvme_identify_namespace_data.md) structure for the Identify command.

### -field DUMMYSTRUCTNAME.MS

Specifies the metadata settings.

When this field set to `1` if the metadata is transferred as part of an extended data LBA. This field is cleared to `0` if the metadata is transferred as part of a separate buffer. The metadata may include protection information, based on the Protection Information (**PI**) field. If the Metadata Size **MS** field of the [LBA Format](ns-nvme-nvme_lba_format.md) selected is `0h`, then this field is not applicable.

### -field DUMMYSTRUCTNAME.PI

An [NVME_PROTECTION_INFORMATION_TYPES](ne-nvme-nvme_protection_information_types.md) enumeration value that specifies whether end-to-end data protection is enabled and the type of protection information.

### -field DUMMYSTRUCTNAME.PIL

Specifies the protection information location.

If this value is set to `1` and protection information is enabled, then protection information is transferred as the first eight bytes of metadata. If cleared to `0` and protection information is enabled, then protection information is transferred as the last eight bytes of metadata. This setting is reported in the Formatted LBA Size **LBAF** field of the [Identify Namespace data structure](../nvme/ns-nvme-nvme_identify_namespace_data.md).

### -field DUMMYSTRUCTNAME.SES

An [NVME_SECURE_ERASE_SETTINGS](ne-nvme-nvme_secure_erase_settings.md) enumeration value that specifies whether a secure erase should be performed as part of the format and the type of the secure erase operation. The erase applies to all user data, regardless of location. For example, within an exposed LBA, within a cache, or within deallocated LBAs.

### -field DUMMYSTRUCTNAME.Reserved

### -field AsUlong

## -remarks

## -see-also

- [NVME_IDENTIFY_NAMESPACE_DATA](../nvme/ns-nvme-nvme_identify_namespace_data.md)
- [NVME_LBA_FORMAT](ns-nvme-nvme_lba_format.md)

