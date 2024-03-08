---
UID: NS:ntenclv.VBS_ENCLAVE_REPORT_VARDATA_HEADER
title: VBS_ENCLAVE_REPORT_VARDATA_HEADER (ntenclv.h)
description: Describes the format of a variable data block contained in a report that the EnclaveGetAttestationReport function generates.
helpviewer_keywords: ["VBS_ENCLAVE_REPORT_VARDATA_HEADER","VBS_ENCLAVE_REPORT_VARDATA_HEADER structure","VBS_ENCLAVE_VARDATA_INVALID","VBS_ENCLAVE_VARDATA_MODULE","base.vbs_enclave_report_vardata_header","ntenclv/VBS_ENCLAVE_REPORT_VARDATA_HEADER"]
old-location: base\vbs_enclave_report_vardata_header.htm
tech.root: base
ms.assetid: A0B02839-E8F4-45A1-B2BA-73E6EF9DA7C8
ms.date: 02/02/2024
ms.keywords: VBS_ENCLAVE_REPORT_VARDATA_HEADER, VBS_ENCLAVE_REPORT_VARDATA_HEADER structure, VBS_ENCLAVE_VARDATA_INVALID, VBS_ENCLAVE_VARDATA_MODULE, base.vbs_enclave_report_vardata_header, ntenclv/VBS_ENCLAVE_REPORT_VARDATA_HEADER
req.header: ntenclv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: VBS_ENCLAVE_REPORT_VARDATA_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VBS_ENCLAVE_REPORT_VARDATA_HEADER
 - ntenclv/VBS_ENCLAVE_REPORT_VARDATA_HEADER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntenclv.h
api_name:
 - VBS_ENCLAVE_REPORT_VARDATA_HEADER
---

# VBS_ENCLAVE_REPORT_VARDATA_HEADER structure

## -description

Describes the format of a variable data block contained in a report that the [EnclaveGetAttestationReport](../winenclaveapi/nf-winenclaveapi-enclavegetattestationreport.md) function generates.

## -struct-fields

### -field DataType

The type of the variable data block.

| Value | Meaning |
|-------|---------|
| **VBS_ENCLAVE_VARDATA_INVALID**<br/>`0x00000000` | The variable data block is not valid. |
| **VBS_ENCLAVE_VARDATA_MODULE**<br/>`0x00000001` | The variable data block is a module. |

### -field Size

The size of this variable data block, including the header, in bytes.

## -remarks

An enclave attestation report includes zero or  variable data blocks. These variable data blocks consist of the following items:

- A **VBS_ENCLAVE_REPORT_VARDATA_HEADER** structure that describes the format of the variable data block.
- The data described by the **VBS_ENCLAVE_REPORT_VARDATA_HEADER** structure. If the value of the **DataType** member of the **VBS_ENCLAVE_REPORT_VARDATA_HEADER** structure is **VBS_ENCLAVE_VARDATA_MODULE**, this data is a [VBS_ENCLAVE_REPORT_MODULE](ns-ntenclv-vbs_enclave_report_module.md) structure.

## -see-also

[Enclave Structures](/windows/win32/trusted-execution/enclaves-structures)

[EnclaveGetAttestationReport](../winenclaveapi/nf-winenclaveapi-enclavegetattestationreport.md)

[VBS_ENCLAVE_REPORT](ns-ntenclv-vbs_enclave_report.md)

[VBS_ENCLAVE_REPORT_MODULE](ns-ntenclv-vbs_enclave_report_module.md)
