---
UID: NS:nvme.__unnamed_struct_139
tech.root: fs 
title: NVME_CDW11_SECURITY_RECEIVE
ms.date: 02/19/2021 
ms.topic: language-reference
targetos: Windows
description: Contains parameters that are used in the Security Receive command.
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
req.typenames: NVME_CDW11_SECURITY_RECEIVE, *PNVME_CDW11_SECURITY_RECEIVE
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW11_SECURITY_RECEIVE
 - NVME_CDW11_SECURITY_RECEIVE
f1_keywords:
 - PNVME_CDW11_SECURITY_RECEIVE
 - nvme/PNVME_CDW11_SECURITY_RECEIVE
 - NVME_CDW11_SECURITY_RECEIVE
 - nvme/NVME_CDW11_SECURITY_RECEIVE
dev_langs:
 - c++
---

# NVME_CDW11_SECURITY_RECEIVE structure

## -description

Contains parameters that are used in the Security Receive command.

## -struct-fields

### -field AL

The value of the Allocation Length (AL) field is specific to the Security Protocol as defined in [SECURITY PROTOCOL IN (SPC-4)](https://nvmexpress.org/wp-content/uploads/NVM_Express_-_SCSI_Translation_Reference-1_5_20150624_Gold.pdf).

This field is supported and specifies the number of bytes to transfer if the INC_512 field is set to `0` in the SPC-4 Security Protocol.

## -remarks

## -see-also

- [NVME_CDW11_SECURITY_SEND](ns-nvme-nvme_cdw11_security_send.md)
- [NVME_CDW10_SECURITY_SEND_RECEIVE](ns-nvme-nvme_cdw10_security_send_receive.md)