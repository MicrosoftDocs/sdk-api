---
UID: NS:nvme.NVME_CDW12_GET_LOG_PAGE
tech.root: fs
title: NVME_CDW12_GET_LOG_PAGE
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: 
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
req.typenames: NVME_CDW12_GET_LOG_PAGE, *PNVME_CDW12_GET_LOG_PAGE
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW12_GET_LOG_PAGE
 - NVME_CDW12_GET_LOG_PAGE
f1_keywords:
 - PNVME_CDW12_GET_LOG_PAGE
 - nvme/PNVME_CDW12_GET_LOG_PAGE
 - NVME_CDW12_GET_LOG_PAGE
 - nvme/NVME_CDW12_GET_LOG_PAGE
dev_langs:
 - c++
---

## -description

## -struct-fields

### -field LPOL

Log Page Offset Lower: The log page offset specifies the location within a log page to start returning data from. This field specifies the lower 32 bits of the log page offset. The offset shall be dword aligned, indicated by bits 1:0 being cleared to 00b.

## -remarks

## -see-also

