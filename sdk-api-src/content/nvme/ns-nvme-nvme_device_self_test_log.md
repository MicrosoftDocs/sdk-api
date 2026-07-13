---
UID: NS:nvme.NVME_DEVICE_SELF_TEST_LOG
tech.root: fs
title: NVME_DEVICE_SELF_TEST_LOG
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains fields that specify the information in a Device Self Test log page that describes the status, completion percentage, and results of a device self-test.
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
req.typenames: NVME_DEVICE_SELF_TEST_LOG, *PNVME_DEVICE_SELF_TEST_LOG
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_DEVICE_SELF_TEST_LOG
 - NVME_DEVICE_SELF_TEST_LOG
f1_keywords:
 - PNVME_DEVICE_SELF_TEST_LOG
 - nvme/PNVME_DEVICE_SELF_TEST_LOG
 - NVME_DEVICE_SELF_TEST_LOG
 - nvme/NVME_DEVICE_SELF_TEST_LOG
dev_langs:
 - c++
---

# NVME_DEVICE_SELF_TEST_LOG structure


## -description

Contains fields that specify the information in a Device Self Test log page that describes the status, completion percentage, and results of a device self-test.

This structure is returned by the Get Log Page command. For more information, see [NVME_CDW10_GET_LOG_PAGE](ns-nvme-nvme_cdw10_get_log_page.md).

## -struct-fields

### -field CurrentOperation

A **CurrentOperation** structure containing fields that describe the current Device Self-Test operation.

### -field CurrentOperation.Status

Indicates the status of the current Device Self-Test operation.

### -field CurrentOperation.Reserved

A reserved field in the **CurrentOperation** structure.

### -field CurrentCompletion

A **CurrentCompletion** structure containing fields that describe the completion of a Device Self-Test operation.

### -field CurrentCompletion.CompletePercent

Indicates the percentage of completion of the Device Self-Test operation. This field is valid if the **CurrentOperation.Status** field is non-zero.

### -field CurrentCompletion.Reserved

A reserved field in the **CurrentCompletion** structure.

### -field Reserved

A reserved field.

### -field ResultData

An array of 20 [NVME_DEVICE_SELF_TEST_RESULT_DATA](ns-nvme-nvme_device_self_test_result_data.md) structures that contain result data for the last 20 Device Self-Test operations, sorted in order from the most recent to the oldest available.

## -remarks

## -see-also

