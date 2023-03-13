---
UID: NS:nvme.NVME_SCSI_NAME_STRING
tech.root: fs
title: NVME_SCSI_NAME_STRING
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains information that is used to construct the SCSI name string identifier.
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
req.typenames: NVME_SCSI_NAME_STRING, *PNVME_SCSI_NAME_STRING
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_SCSI_NAME_STRING
 - NVME_SCSI_NAME_STRING
f1_keywords:
 - PNVME_SCSI_NAME_STRING
 - nvme/PNVME_SCSI_NAME_STRING
 - NVME_SCSI_NAME_STRING
 - nvme/NVME_SCSI_NAME_STRING
dev_langs:
 - c++
---

# NVME_SCSI_NAME_STRING structure


## -description

Contains information that is used to construct the SCSI name string identifier.

The SCSI name string identifier is used for the descriptor in NVMe to SCSI translation for NVMe devices compliant with revision 1.0.

## -struct-fields

### -field PCIVendorID

The company vendor identifier that is assigned by the [Peripheral Component Interconnect - Special Interest Group (PCI-SIG)](https://pcisig.com/).

This value is also in the **VID** field of the [NVME_IDENTIFY_CONTROLLER_DATA](ns-nvme-nvme_identify_controller_data.md) data structure.

### -field ModelNumber

The model number for the NVM subsystem that is assigned by the vendor as an ASCII string.

This value is also in the **MN** field of the [NVME_IDENTIFY_CONTROLLER_DATA](ns-nvme-nvme_identify_controller_data.md) data structure.

### -field NamespaceID

The namespace identifier.

This value is also in the **NSID** field of the [NVME_COMMAND](ns-nvme-nvme_command.md) structure.

### -field SerialNumber

The serial number for the NVM subsystem that is assigned by the vendor as an ASCII string.

This value is also in the **SN** field of the [NVME_IDENTIFY_CONTROLLER_DATA](ns-nvme-nvme_identify_controller_data.md) data structure.

## -remarks

## -see-also

- [NVME_IDENTIFY_CONTROLLER_DATA](ns-nvme-nvme_identify_controller_data.md)
- [NVME_COMMAND](ns-nvme-nvme_command.md)

