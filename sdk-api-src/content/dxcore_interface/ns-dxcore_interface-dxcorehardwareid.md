---
UID: NS:dxcore_interface.DXCoreHardwareID
title: DXCoreHardwareID
description: Represents the PnP hardware ID parts for an adapter.
tech.root: dxcore
ms.date: 06/06/2019
ms.keywords: DXCoreHardwareID structure, dxcore_interface.dxcorehardwareid
ms.localizationpriority: low
targetos: Windows
req.assembly: 
req.construct-type: structure
req.ddi-compliance: 
req.dll: dxcore.dll
req.header: dxcore_interface.h
req.idl: 
req.include-header: dxcore.h
req.irql: 
req.kmdf-ver: 
req.lib: dxcore.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 (Build 18936)
req.target-min-winversvr: 
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
 - kbsyntax
api_type:
 - HeaderDef
api_location:
 - dxcore.dll
api_name:
 - DXCoreHardwareID
---

## -description

Represents the PnP hardware ID parts for an adapter.

## -struct-fields

### -field vendorID

Type: **uint32_t\***

The PCI ID or ACPI ID of the adapter's hardware vendor. If this value is less than or equal to 0xFFFF, it is a PCI ID; otherwise, it is an ACPI ID.

### -field deviceID

Type: **uint32_t\***

The PCI ID or ACPI ID of the adapter's hardware device. If <b>vendorID</b> is a PCI ID, it is also a PCI ID; otherwise, it is an ACPI ID.

### -field subSysID

Type: **uint32_t\***

The PCI ID or ACPI ID of the adapter's hardware subsystem. If <b>vendorID</b> is a PCI ID, it is also a PCI ID; otherwise, it is an ACPI ID.

### -field revision

Type: **uint32_t\***

The adapter's PCI or ACPI revision number. If <b>vendorID</b> is a PCI ID, it is a PCI device revision number; otherwise, it is an ACPI device revision number.

## -see-also

[DXCore reference](/windows/win32/dxcore/dxcore-reference), [Using DXCore to enumerate adapters](/windows/win32/dxcore/dxcore-enum-adapters)
