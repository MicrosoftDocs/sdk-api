---
UID: NS:tbs._TPM_DEVICE_INFO
title: TPM_DEVICE_INFO (tbs.h)
description: Provides information about the version of the TPM.
helpviewer_keywords: ["*PTPM_DEVICE_INFO","PTPM_DEVICE_INFO","PTPM_DEVICE_INFO structure pointer [TBS]","TPM_DEVICE_INFO","TPM_DEVICE_INFO structure [TBS]","tbs.tpm_device_info","tbs/PTPM_DEVICE_INFO","tbs/TPM_DEVICE_INFO"]
old-location: tbs\tpm_device_info.htm
tech.root: TBS
ms.assetid: 59B8AB6D-82D8-4B15-AB62-AB2B9CA7B5E3
ms.date: 12/05/2018
ms.keywords: '*PTPM_DEVICE_INFO, PTPM_DEVICE_INFO, PTPM_DEVICE_INFO structure pointer [TBS], TPM_DEVICE_INFO, TPM_DEVICE_INFO structure [TBS], tbs.tpm_device_info, tbs/PTPM_DEVICE_INFO, tbs/TPM_DEVICE_INFO'
req.header: tbs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: TPM_DEVICE_INFO, *PTPM_DEVICE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TPM_DEVICE_INFO
 - tbs/_TPM_DEVICE_INFO
 - PTPM_DEVICE_INFO
 - tbs/PTPM_DEVICE_INFO
 - TPM_DEVICE_INFO
 - tbs/TPM_DEVICE_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tbs.h
api_name:
 - TPM_DEVICE_INFO
---

# TPM_DEVICE_INFO structure


## -description

Provides information about the version of the TPM.

## -struct-fields

### -field structVersion

The version of the TBS context implementation. This parameter must be set to 	TPM_VERSION_20.

### -field tpmVersion

TPM version. Will be set to TPM_VERSION_12 or TPM_VERSION_20.

### -field tpmInterfaceType

Reserved

### -field tpmImpRevision

Reserved

