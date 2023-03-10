---
UID: NS:nvme.NVME_CHANGED_NAMESPACE_LIST_LOG
tech.root: fs
title: NVME_CHANGED_NAMESPACE_LIST_LOG
ms.date: 02/19/2021 Contains data for the Changed Namespace List log page that describes namespaces in the controller that have changed [Identify Namespace](../nvme/ns-nvme-nvme_identify_namespace_data.md) information since the last time the log page was read.
ms.topic: language-reference
targetos: Windows
description: Contains data for the Changed Namespace List log page that describes namespaces in the controller that have changed [Identify Namespace](../nvme/ns-nvme-nvme_identify_namespace_data.md) information since the last time the log page was read.
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
req.typenames: NVME_CHANGED_NAMESPACE_LIST_LOG, *PNVME_CHANGED_NAMESPACE_LIST_LOG
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CHANGED_NAMESPACE_LIST_LOG
 - NVME_CHANGED_NAMESPACE_LIST_LOG
f1_keywords:
 - PNVME_CHANGED_NAMESPACE_LIST_LOG
 - nvme/PNVME_CHANGED_NAMESPACE_LIST_LOG
 - NVME_CHANGED_NAMESPACE_LIST_LOG
 - nvme/NVME_CHANGED_NAMESPACE_LIST_LOG
dev_langs:
 - c++
---

# NVME_CHANGED_NAMESPACE_LIST_LOG structure


## -description

Contains data for the Changed Namespace List log page that describes namespaces in the controller that have changed [Identify Namespace](../nvme/ns-nvme-nvme_identify_namespace_data.md) information since the last time the log page was read.

The Changed Namespace List log page has a size of 4096 bytes and can be retrieved by using the **NVME_ADMIN_COMMAND_GET_LOG_PAGE** [Admin Command](ne-nvme-nvme_admin_commands.md) with an **LID** value of **NVME_LOG_PAGE_CHANGED_NAMESPACE_LIST**.

## -struct-fields

### -field NSID

Specifies a list of Namespace IDs with up to 1024 entries.

If more than 1024 namespaces have changed attributes since the last time the log page was read, the first entry in the log page will be set to `FFFFFFFFh` and the remainder of the list will be zero filled.

## -remarks

## -see-also

- [NVME_LOG_PAGES](ne-nvme-nvme_log_pages.md)
- [NVME_CDW10_GET_LOG_PAGE](ns-nvme-nvme_cdw10_get_log_page.md)
- [NVME_CDW10_GET_LOG_PAGE_V13](ns-nvme-nvme_cdw10_get_log_page_v13.md)
- [NVME_CDW11_GET_LOG_PAGE](ns-nvme-nvme_cdw11_get_log_page.md)
- [NVME_CDW12_GET_LOG_PAGE](ns-nvme-nvme_cdw12_get_log_page.md)

