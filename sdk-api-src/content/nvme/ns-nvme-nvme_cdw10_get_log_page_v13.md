---
UID: NS:nvme.NVME_CDW10_GET_LOG_PAGE_V13
tech.root: fs
title: NVME_CDW10_GET_LOG_PAGE_V13
ms.date: 08/09/2022
ms.topic: language-reference
targetos: Windows
description: The NVME_CDW10_GET_LOG_PAGE_V13 structure contains parameters for the Get Log Page command that returns a data buffer containing the requested log page.
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
req.typenames: NVME_CDW10_GET_LOG_PAGE_V13, *PNVME_CDW10_GET_LOG_PAGE_V13
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW10_GET_LOG_PAGE_V13
 - NVME_CDW10_GET_LOG_PAGE_V13
f1_keywords:
 - PNVME_CDW10_GET_LOG_PAGE_V13
 - nvme/PNVME_CDW10_GET_LOG_PAGE_V13
 - NVME_CDW10_GET_LOG_PAGE_V13
 - nvme/NVME_CDW10_GET_LOG_PAGE_V13
dev_langs:
 - c++
---

# NVME_CDW10_GET_LOG_PAGE_V13 structure


## -description

Contains parameters for the Get Log Page command that returns a data buffer containing the requested log page. 

> [!NOTE] The format of the **NVME_CDW10_GET_LOG_PAGE_V13** structure conforms to NVMe Specification version 1.3 or later. For NVMe Specifications prior to version 1.3, use the [**NVME_CDW10_GET_LOG_PAGE**](ns-nvme-nvme_cdw10_get_log_page.md) structure.

This structure is used in the **CDW10_V13** field of the **GETLOGPAGE** parameter in the [Command](ns-nvme-nvme_command.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.LID

Specifies an [NVME_LOG_PAGES](ne-nvme-nvme_log_pages.md) value that identifies the log page to retrieve.

### -field DUMMYSTRUCTNAME.LSP

Specifies log specific information.

### -field DUMMYSTRUCTNAME.Reserved0

### -field DUMMYSTRUCTNAME.RAE

The Reset Asynchronous Event (RAE) field.

### -field DUMMYSTRUCTNAME.NUMDL

Specifies the number of Lower Dwords to return.

### -field AsUlong

## -remarks

## -see-also

- [NVME_CDW10_GET_LOG_PAGE](ns-nvme-nvme_cdw10_get_log_page.md)
- [NVME_CDW11_GET_LOG_PAGE](ns-nvme-nvme_cdw11_get_log_page.md)
- [NVME_CDW12_GET_LOG_PAGE](ns-nvme-nvme_cdw12_get_log_page.md)
- [NVME_CDW13_GET_LOG_PAGE](ns-nvme-nvme_cdw13_get_log_page.md)

