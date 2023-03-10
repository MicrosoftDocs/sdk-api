---
UID: NS:nvme.NVME_CDW10_GET_LOG_PAGE
tech.root: fs
title: NVME_CDW10_GET_LOG_PAGE
ms.date: 08/09/2022
ms.topic: language-reference
targetos: Windows
description: The NVME_CDW10_GET_LOG_PAGE structure contains parameters for the Get Log Page command that returns a data buffer containing the requested log page.
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
req.typenames: NVME_CDW10_GET_LOG_PAGE, *PNVME_CDW10_GET_LOG_PAGE
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW10_GET_LOG_PAGE
 - NVME_CDW10_GET_LOG_PAGE
f1_keywords:
 - PNVME_CDW10_GET_LOG_PAGE
 - nvme/PNVME_CDW10_GET_LOG_PAGE
 - NVME_CDW10_GET_LOG_PAGE
 - nvme/NVME_CDW10_GET_LOG_PAGE
dev_langs:
 - c++
---

# NVME_CDW10_GET_LOG_PAGE structure


## -description

Contains parameters for the Get Log Page command that returns a data buffer containing the requested log page.

> [!NOTE]
> The format of the **NVME_CDW10_GET_LOG_PAGE** structure conforms to NVMe Specifications prior to version 1.3. For NVMe Specification 1.3 or later, use the [**NVME_CDW10_GET_LOG_PAGE_V13**](ns-nvme-nvme_cdw10_get_log_page_v13.md) structure.

This structure is used in the **CDW10** field of the **GETLOGPAGE** parameter in the [Command](ns-nvme-nvme_command.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.LID

Specifies an [NVME_LOG_PAGES](ne-nvme-nvme_log_pages.md) value that identifies the log page to retrieve.

### -field DUMMYSTRUCTNAME.Reserved0

### -field DUMMYSTRUCTNAME.NUMD

Specifies the number of Dwords to return. 

If the host software specifies a size larger than the requested log page, the controller returns the complete log page with undefined results for Dwords beyond the end of the log page. This is a 0’s based value.

### -field DUMMYSTRUCTNAME.Reserved1

### -field AsUlong

## -remarks

## -see-also

- [NVME_CDW10_GET_LOG_PAGE_V13](ns-nvme-nvme_cdw10_get_log_page_v13.md)
- [NVME_CDW11_GET_LOG_PAGE](ns-nvme-nvme_cdw11_get_log_page.md)
- [NVME_CDW12_GET_LOG_PAGE](ns-nvme-nvme_cdw12_get_log_page.md)
- [NVME_CDW13_GET_LOG_PAGE](ns-nvme-nvme_cdw13_get_log_page.md)

