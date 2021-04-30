---
UID: NE:dxcore_interface.DXCoreAdapterProperty
title: DXCoreAdapterProperty
description: Defines constants that specify DXCore adapter properties.
author: windows-sdk-content
tech.root: dxcore
ms.author: windowssdkdev
ms.date: 06/11/2019
ms.keywords: DXCoreAdapterProperty enumeration, dxcore_interface.dxcoreadapterproperty
ms.localizationpriority: low
ms.topic: enumeration
targetos: Windows
ms.prod: windows
req.assembly: 
req.construct-type: enumeration
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
 - DXCoreAdapterProperty
---

## -description

Defines constants that specify DXCore adapter properties. Pass one of these constants to the [IDXCoreAdapter::GetPropertySize](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getpropertysize) method to retrieve the buffer size necessary to receive the value of the corresponding property; then pass the same constant to the [IDXCoreAdapter::GetProperty](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty) method to retrieve the property's value in a buffer that you allocate.

## -enum-fields

### -field InstanceLuid

Specifies the <em>InstanceLuid</em> adapter property, which contains a locally unique identifier representing the adapter. This value remains constant for the lifetime of this adapter. The LUID of an adapter changes on reboot, driver upgrade, or device disablement/enablement.

The <em>InstanceLuid</em> adapter property has type <a href="/windows/win32/api/winnt/ns-winnt-_luid">LUID</a>.

### -field DriverVersion

Specifies the <em>DriverVersion</em> adapter property, which contains the driver version, represented in <b>WORD</b>s as a <b>LARGE_INTEGER</b>.

The <em>DriverVersion</em> adapter property has type <b>uint64_t</b>, representing a Boolean value.

### -field DriverDescription

Specifies the <em>DriverDescription</em> adapter property, which contains a NULL-terminated array of <b>CHAR</b>s describing the driver, as specified by the driver, in <a href="/windows/win32/intl/unicode">UTF-8</a> encoding.

The <em>DriverDescription</em> adapter property has type <b>char*</b>.

### -field HardwareID

Specifies the <em>HardwareID</em> adapter property, which represents the PnP hardware ID parts.

The <em>HardwareID</em> adapter property has type <a href="/windows/win32/api/dxcore_interface/ns-dxcore_interface-dxcorehardwareid">DXCoreHardwareID</a>.

### -field KmdModelVersion

Specifies the <em>KmdModelVersion</em> adapter property, which represents the driver model.

The <em>KmdModelVersion</em> adapter property has type <a href="/windows-hardware/drivers/ddi/content/d3dkmthk/ne-d3dkmthk-_qai_driverversion">D3DKMT_DRIVERVERSION</a>.

### -field ComputePreemptionGranularity

Specifies the <em>ComputePreemptionGranularity</em> adapter property, which represents the compute preemption granularity.

The <em>ComputePreemptionGranularity</em> adapter property has type <b>uint16_t</b>, representing a <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_compute_preemption_granularity">D3DKMDT_COMPUTE_PREEMPTION_GRANULARITY</a> value.

### -field GraphicsPreemptionGranularity

Specifies the <em>GraphicsPreemptionGranularity</em> adapter property, which represents the graphics preemption granularity.

The <em>GraphicsPreemptionGranularity</em> adapter property has type <b>uint16_t</b>, representing a <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_graphics_preemption_granularity">D3DKMDT_GRAPHICS_PREEMPTION_GRANULARITY</a> value.

### -field DedicatedAdapterMemory

Specifies the <em>DedicatedAdapterMemory</em> adapter property, which represents the number of bytes of dedicated adapter memory that are not shared with the CPU.

The <em>DedicatedVideoMemory</em> adapter property has type <b>uint64_t</b>.

### -field DedicatedSystemMemory

Specifies the <em>DedicatedSystemMemory</em> adapter property, which represents the number of bytes of dedicated system memory that are not shared with the CPU. This memory is allocated from available system memory at boot time.

The <em>DedicatedSystemMemory</em> adapter property has type <b>uint64_t</b>.

### -field SharedSystemMemory

Specifies the <em>SharedSystemMemory</em> adapter property, which represents the number of bytes of shared system memory. This is the maximum value of system memory that may be consumed by the adapter during operation. Any incidental memory consumed by the driver as it manages and uses video memory is additional.

The <em>SharedSystemMemory</em> adapter property has type <b>uint64_t</b>.

### -field AcgCompatible

Specifies the <em>AcgCompatible</em> adapter property, which indicates whether the adapter is compatible with processes that enforce Arbitrary Code Guard.

The <em>AcgCompatible</em> adapter property has type <b>bool</b>.

### -field IsHardware

Specifies the <em>IsHardware</em> adapter property, which determines whether or not this is a hardware adapter. An adapter that's not a hardware adapter is a software adapter.

The <em>IsHardware</em> adapter property has type <b>bool</b>.

### -field IsIntegrated

Specifies the <em>IsIntegrated</em> adapter property, which determines whether the adapter is reported to be an integrated graphics processor (iGPU).

The <em>IsIntegrated</em> adapter property has type <b>bool</b>.

### -field IsDetachable

Specifies the <em>IsDetachable</em> adapter property, which determines whether the adapter has been reported to be detachable, or removable.

The <em>IsDetachable</em> adapter property has type <b>bool</b>.

<b>Note</b>. Even if <a href="/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty">IDXCoreAdapter::GetProperty</a> indicates `false` for this property, the adapter still has the ability to be reported as removed, such as in the case of malfunction, or driver update.

## -see-also

[IDXCoreAdapter::GetPropertySize](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getpropertysize), [IDXCoreAdapter::GetProperty](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty), [DXCore Reference](/windows/win32/dxcore/dxcore-reference), [Using DXCore to enumerate adapters](/windows/win32/dxcore/dxcore-enum-adapters)
