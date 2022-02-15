---
UID: NE:winioctl._STORAGE_PROPERTY_ID
title: STORAGE_PROPERTY_ID
description: Enumerates the possible values of the PropertyId member of the STORAGE_PROPERTY_QUERY structure passed as input to the IOCTL_STORAGE_QUERY_PROPERTY request to retrieve the properties of a storage device or adapter.
helpviewer_keywords: ["*PSTORAGE_PROPERTY_ID","PSTORAGE_PROPERTY_ID","PSTORAGE_PROPERTY_ID enumeration pointer [Files]","STORAGE_PROPERTY_ID","STORAGE_PROPERTY_ID enumeration [Files]","StorageAccessAlignmentProperty","StorageAdapterPhysicalTopologyProperty","StorageAdapterProperty","StorageAdapterProtocolSpecificProperty","StorageAdapterTemperatureProperty","StorageDeviceAttributesProperty","StorageDeviceCopyOffloadProperty","StorageDeviceDeviceTelemetryProperty","StorageDeviceIdProperty","StorageDeviceIoCapabilityProperty","StorageDeviceLBProvisioningProperty","StorageDeviceMediumProductType","StorageDevicePhysicalTopologyProperty","StorageDevicePowerProperty","StorageDeviceProperty","StorageDeviceProtocolSpecificProperty","StorageDeviceResiliencyProperty","StorageDeviceSeekPenaltyProperty","StorageDeviceTemperatureProperty","StorageDeviceTrimProperty","StorageDeviceUniqueIdProperty","StorageDeviceWriteAggregationProperty","StorageDeviceWriteCacheProperty","StorageMiniportProperty","fs.storage_property_id","winioctl/PSTORAGE_PROPERTY_ID","winioctl/STORAGE_PROPERTY_ID","winioctl/StorageAccessAlignmentProperty","winioctl/StorageAdapterPhysicalTopologyProperty","winioctl/StorageAdapterProperty","winioctl/StorageAdapterProtocolSpecificProperty","winioctl/StorageAdapterTemperatureProperty","winioctl/StorageDeviceAttributesProperty","winioctl/StorageDeviceCopyOffloadProperty","winioctl/StorageDeviceDeviceTelemetryProperty","winioctl/StorageDeviceIdProperty","winioctl/StorageDeviceIoCapabilityProperty","winioctl/StorageDeviceLBProvisioningProperty","winioctl/StorageDeviceMediumProductType","winioctl/StorageDevicePhysicalTopologyProperty","winioctl/StorageDevicePowerProperty","winioctl/StorageDeviceProperty","winioctl/StorageDeviceProtocolSpecificProperty","winioctl/StorageDeviceResiliencyProperty","winioctl/StorageDeviceSeekPenaltyProperty","winioctl/StorageDeviceTemperatureProperty","winioctl/StorageDeviceTrimProperty","winioctl/StorageDeviceUniqueIdProperty","winioctl/StorageDeviceWriteAggregationProperty","winioctl/StorageDeviceWriteCacheProperty","winioctl/StorageMiniportProperty"]
old-location: fs\storage_property_id.htm
tech.root: fs
ms.assetid: 9747be01-7c70-4697-97f7-e3830b54ba0a
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_PROPERTY_ID, PSTORAGE_PROPERTY_ID, PSTORAGE_PROPERTY_ID enumeration pointer [Files], STORAGE_PROPERTY_ID, STORAGE_PROPERTY_ID enumeration [Files], StorageAccessAlignmentProperty, StorageAdapterPhysicalTopologyProperty, StorageAdapterProperty, StorageAdapterProtocolSpecificProperty, StorageAdapterTemperatureProperty, StorageDeviceAttributesProperty, StorageDeviceCopyOffloadProperty, StorageDeviceDeviceTelemetryProperty, StorageDeviceIdProperty, StorageDeviceIoCapabilityProperty, StorageDeviceLBProvisioningProperty, StorageDeviceMediumProductType, StorageDevicePhysicalTopologyProperty, StorageDevicePowerProperty, StorageDeviceProperty, StorageDeviceProtocolSpecificProperty, StorageDeviceResiliencyProperty, StorageDeviceSeekPenaltyProperty, StorageDeviceTemperatureProperty, StorageDeviceTrimProperty, StorageDeviceUniqueIdProperty, StorageDeviceWriteAggregationProperty, StorageDeviceWriteCacheProperty, StorageMiniportProperty, fs.storage_property_id, winioctl/PSTORAGE_PROPERTY_ID, winioctl/STORAGE_PROPERTY_ID, winioctl/StorageAccessAlignmentProperty, winioctl/StorageAdapterPhysicalTopologyProperty, winioctl/StorageAdapterProperty, winioctl/StorageAdapterProtocolSpecificProperty, winioctl/StorageAdapterTemperatureProperty, winioctl/StorageDeviceAttributesProperty, winioctl/StorageDeviceCopyOffloadProperty, winioctl/StorageDeviceDeviceTelemetryProperty, winioctl/StorageDeviceIdProperty, winioctl/StorageDeviceIoCapabilityProperty, winioctl/StorageDeviceLBProvisioningProperty, winioctl/StorageDeviceMediumProductType, winioctl/StorageDevicePhysicalTopologyProperty, winioctl/StorageDevicePowerProperty, winioctl/StorageDeviceProperty, winioctl/StorageDeviceProtocolSpecificProperty, winioctl/StorageDeviceResiliencyProperty, winioctl/StorageDeviceSeekPenaltyProperty, winioctl/StorageDeviceTemperatureProperty, winioctl/StorageDeviceTrimProperty, winioctl/StorageDeviceUniqueIdProperty, winioctl/StorageDeviceWriteAggregationProperty, winioctl/StorageDeviceWriteCacheProperty, winioctl/StorageMiniportProperty'
req.header: winioctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: STORAGE_PROPERTY_ID, *PSTORAGE_PROPERTY_ID
req.redist: 
f1_keywords:
 - _STORAGE_PROPERTY_ID
 - winioctl/_STORAGE_PROPERTY_ID
 - PSTORAGE_PROPERTY_ID
 - winioctl/PSTORAGE_PROPERTY_ID
 - STORAGE_PROPERTY_ID
 - winioctl/STORAGE_PROPERTY_ID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - STORAGE_PROPERTY_ID
---

# STORAGE_PROPERTY_ID enumeration


## -description

Enumerates the possible values of the **PropertyId** member of the [STORAGE_PROPERTY_QUERY](ns-winioctl-storage_property_query.md) structure passed as input to the [IOCTL_STORAGE_QUERY_PROPERTY](ni-winioctl-ioctl_storage_query_property.md) request to retrieve the properties of a storage device or adapter.

## -enum-fields

### -field StorageDeviceProperty:0

Indicates that the caller is querying for the device descriptor, [STORAGE_DEVICE_DESCRIPTOR](ns-winioctl-storage_device_descriptor.md).

### -field StorageAdapterProperty

Indicates that the caller is querying for the adapter descriptor, [STORAGE_ADAPTER_DESCRIPTOR](ns-winioctl-storage_adapter_descriptor.md).

### -field StorageDeviceIdProperty

Indicates that the caller is querying for the device identifiers provided with the SCSI vital product data pages. Data is returned using the  [STORAGE_DEVICE_ID_DESCRIPTOR](ns-winioctl-storage_device_id_descriptor.md) structure.

### -field StorageDeviceUniqueIdProperty

**Intended for driver usage.** Indicates that the caller is querying for the unique device identifiers. Data is returned using the **STORAGE_DEVICE_UNIQUE_IDENTIFIER** structure (see the storduid.h header in the DDK).

**Windows Server 2003 and Windows XP:**  This value is not supported before Windows Vista and Windows Server 2008.

### -field StorageDeviceWriteCacheProperty

Indicates that the caller is querying for the write cache property. Data is returned using the [STORAGE_WRITE_CACHE_PROPERTY](ns-winioctl-storage_write_cache_property.md) structure.

**Windows Server 2003 and Windows XP:**  This value is not supported before Windows Vista and Windows Server 2008.

### -field StorageMiniportProperty

Reserved for system use.

### -field StorageAccessAlignmentProperty

Indicates that the caller is querying for the access alignment descriptor, [STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR](ns-winioctl-storage_access_alignment_descriptor.md).

**Windows Server 2003 and Windows XP:**  This value is not supported before Windows Vista and Windows Server 2008.

### -field StorageDeviceSeekPenaltyProperty

Indicates that the caller is querying for the seek penalty descriptor, [DEVICE_SEEK_PENALTY_DESCRIPTOR](ns-winioctl-device_seek_penalty_descriptor.md).

**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:**  This value is not supported before Windows 7 and Windows Server 2008 R2.

### -field StorageDeviceTrimProperty

Indicates that the caller is querying for the trim descriptor, [DEVICE_TRIM_DESCRIPTOR](ns-winioctl-device_trim_descriptor.md).

**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:**  This value is not supported before Windows 7 and Windows Server 2008 R2.

### -field StorageDeviceWriteAggregationProperty

Reserved for system use.

### -field StorageDeviceDeviceTelemetryProperty

Reserved for system use.

### -field StorageDeviceLBProvisioningProperty

Indicates that the caller is querying for the logical block provisioning property. Data is returned using the [DEVICE_LB_PROVISIONING_DESCRIPTOR](ns-winioctl-device_lb_provisioning_descriptor.md) structure.

**Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:**  This value is not supported before Windows 8 and Windows Server 2012.

### -field StorageDevicePowerProperty

Indicates that the caller is querying for the device power descriptor. Data is returned using the [DEVICE_POWER_DESCRIPTOR](ns-winioctl-device_power_descriptor.md) structure.

**Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:**  This value is not supported before Windows 8 and Windows Server 2012.

### -field StorageDeviceCopyOffloadProperty

Indicates that the caller is querying for the copy offload  parameters property. Data is returned using the [DEVICE_COPY_OFFLOAD_DESCRIPTOR](ns-winioctl-device_copy_offload_descriptor.md) structure.

**Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:**  This value is not supported before Windows 8 and Windows Server 2012.

### -field StorageDeviceResiliencyProperty

Reserved for system use.

### -field StorageDeviceMediumProductType

Indicates that the caller is querying for the medium product type. Data is returned using the [STORAGE_MEDIUM_PRODUCT_TYPE_DESCRIPTOR](./ns-winioctl-storage_medium_product_type_descriptor.md) structure.

### -field StorageAdapterRpmbProperty

Indicates that the caller is querying for RPMB support and properties. Data is returned using the [STORAGE_RPMB_DESCRIPTOR](ns-winioctl-storage_rpmb_descriptor.md) structure.

### -field StorageAdapterCryptoProperty

Provides info on the storage adapter encryption capabilities. This is currently supported on UFS (Universal Flash Storage) adapters.

### -field StorageDeviceIoCapabilityProperty:48

Indicates that the caller is querying for the device I/O capability property. Data is returned using the [DEVICE_IO_CAPABILITY_DESCRIPTOR](ns-winioctl-storage_device_io_capability_descriptor.md) structure.

### -field StorageAdapterProtocolSpecificProperty

Indicates that the caller is querying for protocol-specific data from the  adapter. Data is returned using the [STORAGE_PROTOCOL_DATA_DESCRIPTOR](ns-winioctl-storage_protocol_data_descriptor.md) structure. See the remarks for more info.

### -field StorageDeviceProtocolSpecificProperty

Indicates that the caller is querying for protocol-specific data from the device. Data is returned using the [STORAGE_PROTOCOL_DATA_DESCRIPTOR](ns-winioctl-storage_protocol_data_descriptor.md) structure. See the remarks for more info.

### -field StorageAdapterTemperatureProperty

Indicates that the caller is querying temperature data from the adapter. Data is returned using the [STORAGE_TEMPERATURE_DATA_DESCRIPTOR](ns-winioctl-storage_temperature_data_descriptor.md) structure.

### -field StorageDeviceTemperatureProperty

Indicates that the caller is querying for temperature data from the device.  Data is returned using the [STORAGE_TEMPERATURE_DATA_DESCRIPTOR](ns-winioctl-storage_temperature_data_descriptor.md) structure.

### -field StorageAdapterPhysicalTopologyProperty

Indicates that the caller is querying for topology information from the adapter. Data is returned using the [STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR](ns-winioctl-storage_physical_topology_descriptor.md) structure.

### -field StorageDevicePhysicalTopologyProperty

Indicates that the caller is querying for topology information from the device. Data is returned using the [STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR](ns-winioctl-storage_physical_topology_descriptor.md) structure.

### -field StorageDeviceAttributesProperty

Reserved for future use.

### -field StorageDeviceManagementStatus

Provides health information about the storage device (specifically for the persistent memory stack).

### -field StorageAdapterSerialNumberProperty

Indicates that the caller is querying for the adapter serial number. Data is returned using the [STORAGE_ADAPTER_SERIAL_NUMBER](ns-winioctl-storage_adapter_serial_number.md) structure.

### -field StorageDeviceLocationProperty

Reserved for system use.

### -field StorageDeviceNumaProperty

Provides the non-uniform memory access (NUMA) node of the storage device.

### -field StorageDeviceZonedDeviceProperty

Reserved for system use.

### -field StorageDeviceUnsafeShutdownCount

Provides the unsafe shutdown count value used to determine if the device data might have been lost during a power loss event (specifically for the persistent memory stack).

### -field StorageDeviceEnduranceProperty

Provides info on how many bytes have been read/write from a solid-state drive (SSD). This property is supported only for Non-Volatile Memory Express (NVMe) devices that implement a certain NVMe feature.

### -field StorageDeviceLedStateProperty

Provides info on the state of the LED associated with a storage device. This is a server-oriented feature.

### -field StorageDeviceSelfEncryptionProperty:64

Reserved for system use.

### -field StorageFruIdProperty

Provides identification info for a storage device that can be physically replaced with a Field Replacement Unit (FRU).

## -remarks

The optional output buffer returned through the *lpOutBuffer* parameter of the [IOCTL_STORAGE_QUERY_PROPERTY](ni-winioctl-ioctl_storage_query_property.md) control code request can be one of several structures depending on the value of the **PropertyId** member of the [STORAGE_PROPERTY_QUERY](ns-winioctl-storage_property_query.md) structure pointed to by the *lpInBuffer* parameter. If the **QueryType** member of the **STORAGE_PROPERTY_QUERY** is set to **PropertyExistsQuery**, then no structure is returned.

## -see-also

* [Disk Management Enumeration Types](/windows/desktop/FileIO/disk-management-enumeration-types)
* [IOCTL_STORAGE_QUERY_PROPERTY](ni-winioctl-ioctl_storage_query_property.md)
* [STORAGE_PROPERTY_QUERY](ns-winioctl-storage_property_query.md)
* [STORAGE_QUERY_TYPE](ne-winioctl-storage_query_type.md)
