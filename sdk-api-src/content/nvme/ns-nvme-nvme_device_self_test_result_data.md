---
UID: NS:nvme.NVME_DEVICE_SELF_TEST_RESULT_DATA
tech.root: fs
title: NVME_DEVICE_SELF_TEST_RESULT_DATA
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains data about the results of a Device Self-Test operation.
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
req.typenames: NVME_DEVICE_SELF_TEST_RESULT_DATA, *PNVME_DEVICE_SELF_TEST_RESULT_DATA
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_DEVICE_SELF_TEST_RESULT_DATA
 - NVME_DEVICE_SELF_TEST_RESULT_DATA
f1_keywords:
 - PNVME_DEVICE_SELF_TEST_RESULT_DATA
 - nvme/PNVME_DEVICE_SELF_TEST_RESULT_DATA
 - NVME_DEVICE_SELF_TEST_RESULT_DATA
 - nvme/NVME_DEVICE_SELF_TEST_RESULT_DATA
dev_langs:
 - c++
---

# NVME_DEVICE_SELF_TEST_RESULT_DATA structure


## -description

Contains data about the results of a Device Self-Test operation.

This structure is used in the **ResultData** field of the [NVME_DEVICE_SELF_TEST_LOG](ns-nvme-nvme_device_self_test_log.md) structure.

## -struct-fields

### -field Status

A **Status** structure containing fields that describe the status of a Device Self-Test operation.

### -field Status.Result

Indicates the result of the Device Self-Test operation.

### -field Status.CodeValue

Indicates the Self-Test code value that was specified in the command.

### -field SegmentNumber

Indicates the first segment in which a failure occurred during the Device Self-Test operation.

### -field ValidDiagnostics

A **ValidDiagnostics** structure containing fields that indicate the validity of certain parameters in a Device Self-Test operation.

### -field ValidDiagnostics.NSIDValid

A **ValidDiagnostics** field that indicates whether the contents of the Namespace Identifier (**NSID**) field is valid.

When this value is set to `1`, the contents of the **NSID** field are valid.

### -field ValidDiagnostics.FLBAValid

A **ValidDiagnostics** field that indicates whether the contents of the Failing Logical Block Address (**FLBA**) field is valid.

When this value is set to `1`, the contents of the **FLBA** field are valid.

### -field ValidDiagnostics.SCTValid

A **ValidDiagnostics** field that indicates whether the contents of the Status Code Type (**StatusCodeType**) field is valid.

When this value is set to `1`, the contents of the **StatusCodeType** field is valid.

### -field ValidDiagnostics.SCValid

A **ValidDiagnostics** field that indicates whether the contents of the Status Code (**StatusCode**) field is valid.

When this value is set to `1`, the contents of the **StatusCode** field is valid.

### -field ValidDiagnostics.Reserved

A reserved field in the **ValidDiagnostics**  structure.

### -field Reserved

A reserved field.

### -field POH

Indicates the number of Power On Hours (POH) when the test operation was completed or aborted.

### -field NSID

Contains the Namespace Identifier (NSID). This field is only valid if **NSIDValid** is set to `1`.

### -field FailingLBA

The Logical Block Address (LBA) which caused the test to fail. This field is only valid if **FLBAValid** is set to `1`.

### -field StatusCodeType

A Status Code Type (**StatusCodeType**) structure containing fields that contain information about errors and conditions.

### -field StatusCodeType.AdditionalInfo

A **StatusCodeType** field that contains additional information related to errors and conditions of the Device Self-Test operation based on the [Status Code Type](ne-nvme-nvme_status_types.md).

This field is only valid if **SCTValid** is set to `1`.

### -field StatusCodeType.Reserved

A reserved field in the **StatusCodeType**  structure.

### -field StatusCode

A **StatusCodeType** field that contains additional information related to errors and conditions of the Device Self-Test operation based on the Status Code.

This field is only valid if **SCValid** is set to `1`.

### -field VendorSpecific

A vendor specific field.

## -remarks

## -see-also

