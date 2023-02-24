---
UID: NS:nvme.NVME_CDW11_FIRMWARE_DOWNLOAD
tech.root: fs
title: NVME_CDW11_FIRMWARE_DOWNLOAD
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains parameters for the Firmware Image Download command that is used to copy a new firmware image (in whole or in part) to the controller.
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
req.typenames: NVME_CDW11_FIRMWARE_DOWNLOAD, *PNVME_CDW11_FIRMWARE_DOWNLOAD
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW11_FIRMWARE_DOWNLOAD
 - NVME_CDW11_FIRMWARE_DOWNLOAD
f1_keywords:
 - PNVME_CDW11_FIRMWARE_DOWNLOAD
 - nvme/PNVME_CDW11_FIRMWARE_DOWNLOAD
 - NVME_CDW11_FIRMWARE_DOWNLOAD
 - nvme/NVME_CDW11_FIRMWARE_DOWNLOAD
dev_langs:
 - c++
---

# NVME_CDW11_FIRMWARE_DOWNLOAD structure


## -description

Contains parameters for the Firmware Image Download command that is used to copy a new firmware image (in whole or in part) to the controller.

The Firmware Image Download command uses the PRP Entry 1 **PRP1** and PRP Entry 2 **PRP2** fields, and the Command Dword 10 **CDW10** and Command Dword 11 **CDW11** fields in the **FIRMWAREDOWNLOAD** parameter of the [Command](ns-nvme-nvme_command.md) structure. All other command specific fields in the **FIRMWAREDOWNLOAD** parameter are reserved.

The **NVME_CDW11_FIRMWARE_DOWNLOAD** structure is used as the value of the **CDW11** parameter in the **FIRMWAREDOWNLOAD** field of the [Command](ns-nvme-nvme_command.md) structure.

## -struct-fields

### -field OFST

The Offset (OFST) field specifies the number of Dwords offset from the start of the firmware image being downloaded to the controller. The offset is used to construct the complete firmware image when the firmware is downloaded in multiple pieces. The piece corresponding to the start of the firmware image has an Offset of `0h`.

## -remarks

## -see-also

- [NVME_CDW10_FIRMWARE_DOWNLOAD](ns-nvme-nvme_cdw10_firmware_download.md)

