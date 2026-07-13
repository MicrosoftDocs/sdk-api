---
UID: NS:nvme._NVME_TELEMETRY_HOST_INITIATED_LOG
tech.root: fs 
title: NVME_TELEMETRY_HOST_INITIATED_LOG
ms.date: 02/19/2021 
ms.topic: language-reference
targetos: Windows
description: Contains fields that specify the information in a Telemetry Host-Initiated Log page.
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
req.typenames: NVME_TELEMETRY_HOST_INITIATED_LOG, *PNVME_TELEMETRY_HOST_INITIATED_LOG
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - _NVME_TELEMETRY_HOST_INITIATED_LOG
 - PNVME_TELEMETRY_HOST_INITIATED_LOG
 - NVME_TELEMETRY_HOST_INITIATED_LOG
f1_keywords:
 - _NVME_TELEMETRY_HOST_INITIATED_LOG
 - nvme/_NVME_TELEMETRY_HOST_INITIATED_LOG
 - PNVME_TELEMETRY_HOST_INITIATED_LOG
 - nvme/PNVME_TELEMETRY_HOST_INITIATED_LOG
 - NVME_TELEMETRY_HOST_INITIATED_LOG
 - nvme/NVME_TELEMETRY_HOST_INITIATED_LOG
dev_langs:
 - c++
---

# NVME_TELEMETRY_HOST_INITIATED_LOG structure

## -description

Contains fields that specify the information in a Telemetry Host-Initiated Log page.

The **NVME_RESERVATION_NOTIFICATION_LOG** structure is returned by the Get Log Page command. For more information, see [NVME_CDW10_GET_LOG_PAGE](ns-nvme-nvme_cdw10_get_log_page.md).

## -struct-fields

### -field LogIdentifier

Indicates the log identifier.

### -field Reserved0

Bytes 1-4 are reserved.

### -field OrganizationID

Indicates an IEEE Organizationally Unique Identifier (OUI) that is the Organization ID.

### -field Area1LastBlock

Bytes 8-9 indicate the last block of Area 1.

### -field Area2LastBlock

Bytes 10-11 indicate the last block of Area 2.

### -field Area3LastBlock

Bytes 12-13 indicate the last block of Area 3.

### -field Reserved1

Bytes 14-381 are reserved.

### -field ControllerInitiatedDataAvailable

Byte 382 indicates whether controller initiated data is available.

### -field ControllerInitiatedDataGenerationNumber

Byte 383 indicates the generation number of controller initiated data when it is available.

### -field ReasonIdentifier

Bytes 384-511 indicate the reason identifier.

## -remarks

All NVMe Telemetry Data Blocks are 512 bytes in size.

## -see-also

