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

The PCI ID of the adapter's hardware vendor.

### -field deviceID

Type: **uint32_t\***

The PCI ID of the adapter's hardware device.

### -field subSysID

Type: **uint32_t\***

The PCI ID of the adapter's hardware subsystem.

### -field revision

Type: **uint32_t\***

The PCI ID of the adapter's revision number.

## -see-also

[DXCore Reference](/windows/win32/dxcore/dxcore-reference), [Using DXCore to enumerate adapters](/windows/win32/dxcore/dxcore-enum-adapters)
