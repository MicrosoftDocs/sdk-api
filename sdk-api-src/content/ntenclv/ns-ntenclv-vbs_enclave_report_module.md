---
UID: NS:ntenclv.VBS_ENCLAVE_REPORT_MODULE
title: VBS_ENCLAVE_REPORT_MODULE (ntenclv.h)
description: Describes a module loaded for the enclave.
helpviewer_keywords: ["VBS_ENCLAVE_REPORT_MODULE","VBS_ENCLAVE_REPORT_MODULE structure","base.vbs_enclave_report_module","ntenclv/VBS_ENCLAVE_REPORT_MODULE"]
old-location: base\vbs_enclave_report_module.htm
tech.root: base
ms.assetid: FB72B01D-B3FE-4FD7-8766-B209C6BC105E
ms.date: 02/02/2024
ms.keywords: VBS_ENCLAVE_REPORT_MODULE, VBS_ENCLAVE_REPORT_MODULE structure, base.vbs_enclave_report_module, ntenclv/VBS_ENCLAVE_REPORT_MODULE
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
req.typenames: VBS_ENCLAVE_REPORT_MODULE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VBS_ENCLAVE_REPORT_MODULE
 - ntenclv/VBS_ENCLAVE_REPORT_MODULE
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
 - VBS_ENCLAVE_REPORT_MODULE
---

# VBS_ENCLAVE_REPORT_MODULE structure

## -description

Describes a module loaded for the enclave. The report contains one **VBS_ENCLAVE_REPORT_MODULE** structure for every module loaded for the enclave except the primary module for the enclave, which is described in the **EnclaveIdentity** member of the [VBS_ENCLAVE_REPORT](ns-ntenclv-vbs_enclave_report.md) structure.

## -struct-fields

### -field Header

The variable data header for the report.

### -field UniqueId

The enclave unique identifier of the module.

### -field AuthorId

The author identifier of the module.

### -field FamilyId

The family identifier of the module.

### -field ImageId

The image identifier of the module.

### -field Svn

The security version number of the module.

### -field ModuleName

A NULL-terminated string that contains the name of the module as it was loaded into the enclave.

## -see-also

[Enclave Structures](/windows/win32/trusted-execution/enclaves-structures)

[VBS_ENCLAVE_REPORT](ns-ntenclv-vbs_enclave_report.md)

[VBS_ENCLAVE_REPORT_VARDATA_HEADER](ns-ntenclv-vbs_enclave_report_vardata_header.md)
