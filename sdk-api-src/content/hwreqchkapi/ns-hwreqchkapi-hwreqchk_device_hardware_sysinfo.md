---
UID: NS:hwreqchkapi.HWREQCHK_DEVICE_HARDWARE_SYSINFO
tech.root: hwreqchk
title: HWREQCHK_DEVICE_HARDWARE_SYSINFO (hwreqchkapi.h)
ms.date: 04/24/2023
targetos: Windows
description: Provides information about the device hardware.
prerelease: true
req.construct-type: structure
req.ddi-compliance: 
req.dll: HWREQCHK.DLL
req.header: hwreqchkapi.h
req.include-header: 
req.kmdf-ver: 
req.lib: HWREQCHK.LIB
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: HWREQCHK_DEVICE_HARDWARE_SYSINFO
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - hwreqchkapi.h
api_name:
 - HWREQCHK_DEVICE_HARDWARE_SYSINFO
f1_keywords:
 - HWREQCHK_DEVICE_HARDWARE_SYSINFO
 - hwreqchkapi/HWREQCHK_DEVICE_HARDWARE_SYSINFO
dev_langs:
 - c++
helpviewer_keywords:
 - HWREQCHK_DEVICE_HARDWARE_SYSINFO
---

## -description

Provides information about the device hardware.

## -struct-fields

### -field SSE2ProcessorSupport

Indicates whether the device supports the SSE2 instruction set.

### -field NXProcessorSupport

Indicates whether the device supports the NX instruction set.

### -field CompareExchange128Support

Indicates whether the device supports the CompareExchange128 instruction.

### -field LahfSahfSupport

Indicates whether the device supports the LAHF/SAHF instruction.

### -field PrefetchWSupport

Indicates whether the device supports the PREFETCHW instruction.

### -field ArmV81ProcessorSupport

Indicates whether the device supports the ARMv8.1 instruction set.

### -field SecureBootCapable

Indicates whether the device is capable of running in Secure Boot mode.

### -field TpmVersion

The version of the Trusted Platform Module (TPM).

### -field RamMB

The amount of RAM in megabytes.

### -field SystemDiskSizeMB

The size of the system disk in megabytes.

### -field CpuMhz

The clock speed of the CPU.

### -field CpuCoreCount

The number of cores in the CPU.

### -field CpuFamily

The family of the CPU.

### -field CpuModel

The model of the CPU.

### -field CpuStepping

The stepping value of the CPU.

### -field Platform

The platform of the CPU.

### -field CpuVendor

The processor vendor.

### -field Architecture

The architecture of the CPU.

### -field ProcessorName

The name of the processor. The maximum size of the *ProcessorName* is 256, as defined by **HWREQCHK_MAX_PROPERTY_VALUE**.

### -field IsServer

Indicates whether the device is a server.

### -field LockdownMode

Inidcates whether the device is in lockdown mode.

### -field ProductOS

Specifies the product's operating system.

### -field ProductName

The product name of the current device. The maximum size of the *ProductName* is 256, as defined by **HWREQCHK_MAX_PROPERTY_VALUE**.

## -remarks

## -see-also
