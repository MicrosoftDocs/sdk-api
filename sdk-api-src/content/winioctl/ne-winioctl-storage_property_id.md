---
UID: NE:winioctl._STORAGE_PROPERTY_ID
title: STORAGE_PROPERTY_ID (winioctl.h)
author: windows-sdk-content
description: Enumerates the possible values of the PropertyId member of the STORAGE_PROPERTY_QUERY structure passed as input to the IOCTL_STORAGE_QUERY_PROPERTY request to retrieve the properties of a storage device or adapter.
old-location: fs\storage_property_id.htm
tech.root: FileIO
ms.assetid: 9747be01-7c70-4697-97f7-e3830b54ba0a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PSTORAGE_PROPERTY_ID, PSTORAGE_PROPERTY_ID, PSTORAGE_PROPERTY_ID enumeration pointer [Files], STORAGE_PROPERTY_ID, STORAGE_PROPERTY_ID enumeration [Files], StorageAccessAlignmentProperty, StorageAdapterPhysicalTopologyProperty, StorageAdapterProperty, StorageAdapterProtocolSpecificProperty, StorageAdapterTemperatureProperty, StorageDeviceAttributesProperty, StorageDeviceCopyOffloadProperty, StorageDeviceDeviceTelemetryProperty, StorageDeviceIdProperty, StorageDeviceIoCapabilityProperty, StorageDeviceLBProvisioningProperty, StorageDeviceMediumProductType, StorageDevicePhysicalTopologyProperty, StorageDevicePowerProperty, StorageDeviceProperty, StorageDeviceProtocolSpecificProperty, StorageDeviceResiliencyProperty, StorageDeviceSeekPenaltyProperty, StorageDeviceTemperatureProperty, StorageDeviceTrimProperty, StorageDeviceUniqueIdProperty, StorageDeviceWriteAggregationProperty, StorageDeviceWriteCacheProperty, StorageMiniportProperty, fs.storage_property_id, winioctl/PSTORAGE_PROPERTY_ID, winioctl/STORAGE_PROPERTY_ID, winioctl/StorageAccessAlignmentProperty, winioctl/StorageAdapterPhysicalTopologyProperty, winioctl/StorageAdapterProperty, winioctl/StorageAdapterProtocolSpecificProperty, winioctl/StorageAdapterTemperatureProperty, winioctl/StorageDeviceAttributesProperty, winioctl/StorageDeviceCopyOffloadProperty, winioctl/StorageDeviceDeviceTelemetryProperty, winioctl/StorageDeviceIdProperty, winioctl/StorageDeviceIoCapabilityProperty, winioctl/StorageDeviceLBProvisioningProperty, winioctl/StorageDeviceMediumProductType, winioctl/StorageDevicePhysicalTopologyProperty, winioctl/StorageDevicePowerProperty, winioctl/StorageDeviceProperty, winioctl/StorageDeviceProtocolSpecificProperty, winioctl/StorageDeviceResiliencyProperty, winioctl/StorageDeviceSeekPenaltyProperty, winioctl/StorageDeviceTemperatureProperty, winioctl/StorageDeviceTrimProperty, winioctl/StorageDeviceUniqueIdProperty, winioctl/StorageDeviceWriteAggregationProperty, winioctl/StorageDeviceWriteCacheProperty, winioctl/StorageMiniportProperty"
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - STORAGE_PROPERTY_ID
product: Windows
targetos: Windows
req.typenames: STORAGE_PROPERTY_ID, *PSTORAGE_PROPERTY_ID
req.redist: 
---

# STORAGE_PROPERTY_ID enumeration


## -description


Enumerates the possible values of the <b>PropertyId</b> member of the 
   <a href="https://msdn.microsoft.com/c97a14ab-628c-41f1-96c3-0f47654d0606">STORAGE_PROPERTY_QUERY</a> structure passed as input to 
   the <a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a> request to 
   retrieve the properties of a storage device or adapter.


## -enum-fields




### -field StorageDeviceProperty

Indicates that the caller is querying for the device descriptor, <a href="https://msdn.microsoft.com/f84f8a88-b6fc-4b22-b858-52955c8d537d">STORAGE_DEVICE_DESCRIPTOR</a>.


### -field StorageAdapterProperty

Indicates that the caller is querying for the adapter descriptor, <a href="https://msdn.microsoft.com/8a5059d3-09a4-4411-8d86-d1257edb409a">STORAGE_ADAPTER_DESCRIPTOR</a>.


### -field StorageDeviceIdProperty

Indicates that the caller is querying for the device identifiers provided with the SCSI vital product data pages. Data is returned using the  <a href="https://msdn.microsoft.com/67b346fd-8976-4cd7-bb2f-a44ef6d56bc4">STORAGE_DEVICE_ID_DESCRIPTOR</a> structure.


### -field StorageDeviceUniqueIdProperty

<b>Intended for driver usage.</b> Indicates that the caller is querying for the unique device identifiers. Data is returned using the <b>STORAGE_DEVICE_UNIQUE_IDENTIFIER</b> structure (see the storduid.h header in the DDK).

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported before Windows Vista and Windows Server 2008.


### -field StorageDeviceWriteCacheProperty

Indicates that the caller is querying for the write cache property. Data is returned using the  <a href="https://msdn.microsoft.com/5248be70-229d-42e6-923a-5a6ffd5268b1">STORAGE_WRITE_CACHE_PROPERTY</a> structure.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported before Windows Vista and Windows Server 2008.


### -field StorageMiniportProperty

Reserved for system use.


### -field StorageAccessAlignmentProperty

Indicates that the caller is querying for the access alignment descriptor, <a href="https://msdn.microsoft.com/en-us/library/Ff800831(v=VS.85).aspx">STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR</a>.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported before Windows Vista and Windows Server 2008.


### -field StorageDeviceSeekPenaltyProperty

Indicates that the caller is querying for the seek penalty descriptor, <a href="https://msdn.microsoft.com/b3fbf27a-dac8-4fd2-8c0d-f621f0123c98">DEVICE_SEEK_PENALTY_DESCRIPTOR</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported before Windows 7 and Windows Server 2008 R2.


### -field StorageDeviceTrimProperty

Indicates that the caller is querying for the trim descriptor, <a href="https://msdn.microsoft.com/60b38d08-5869-442f-845b-b3d8667d069f">DEVICE_TRIM_DESCRIPTOR</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported before Windows 7 and Windows Server 2008 R2.


### -field StorageDeviceWriteAggregationProperty

Reserved for system use.


### -field StorageDeviceDeviceTelemetryProperty

Reserved for system use.


### -field StorageDeviceLBProvisioningProperty

Indicates that the caller is querying for the logical block provisioning property. Data is returned using the <a href="https://msdn.microsoft.com/en-us/library/Hh449432(v=VS.85).aspx">DEVICE_LB_PROVISIONING_DESCRIPTOR</a> structure.

<b>Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported before Windows 8 and Windows Server 2012.


### -field StorageDevicePowerProperty

Indicates that the caller is querying for the device power descriptor. Data is returned using the <a href="https://msdn.microsoft.com/63e51485-db3f-45ed-925e-0abf105c8aef">DEVICE_POWER_DESCRIPTOR</a> structure.

<b>Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported before Windows 8 and Windows Server 2012.


### -field StorageDeviceCopyOffloadProperty

Indicates that the caller is querying for the copy offload  parameters property. Data is returned using the <a href="https://msdn.microsoft.com/ff100db5-f244-4d34-8b55-9b6b21b9e382">DEVICE_COPY_OFFLOAD_DESCRIPTOR</a> structure.

<b>Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported before Windows 8 and Windows Server 2012.


### -field StorageDeviceResiliencyProperty

Reserved for system use.


### -field StorageDeviceMediumProductType

Indicates that the caller is querying for the medium product type. Data is returned using the <a href="https://msdn.microsoft.com/en-us/library/Mt718122(v=VS.85).aspx">STORAGE_MEDIUM_PRODUCT_TYPE_DESCRIPTOR</a> structure.


### -field StorageAdapterRpmbProperty


### -field StorageAdapterCryptoProperty


### -field StorageDeviceIoCapabilityProperty

Indicates that the caller is querying for the device I/O capability property. Data is returned using the <a href="https://msdn.microsoft.com/en-us/library/Mt718114(v=VS.85).aspx">DEVICE_IO_CAPABILITY_DESCRIPTOR</a> structure.


### -field StorageAdapterProtocolSpecificProperty

Indicates that the caller is querying for protocol-specific data from the  adapter. Data is returned using the <a href="https://msdn.microsoft.com/BCA56343-9FB4-4079-9DB1-5DD55529B586">STORAGE_PROTOCOL_DATA_DESCRIPTOR</a> structure. See the remarks for more info.


### -field StorageDeviceProtocolSpecificProperty

Indicates that the caller is querying for protocol-specific data from the device. Data is returned using the <a href="https://msdn.microsoft.com/BCA56343-9FB4-4079-9DB1-5DD55529B586">STORAGE_PROTOCOL_DATA_DESCRIPTOR</a> structure. See the remarks for more info.


### -field StorageAdapterTemperatureProperty

Indicates that the caller is querying temperature data from the adapter. Data is returned using the <a href="https://msdn.microsoft.com/en-us/library/Mt718128(v=VS.85).aspx">STORAGE_TEMPERATURE_DATA_DESCRIPTOR</a> structure.


### -field StorageDeviceTemperatureProperty

Indicates that the caller is querying for temperature data from the device.  Data is returned using the <a href="https://msdn.microsoft.com/en-us/library/Mt718128(v=VS.85).aspx">STORAGE_TEMPERATURE_DATA_DESCRIPTOR</a> structure.


### -field StorageAdapterPhysicalTopologyProperty

Indicates that the caller is querying for topology information from the adapter. Data is returned using the <a href="https://msdn.microsoft.com/en-us/library/Dn933274(v=VS.85).aspx">STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR</a> structure.


### -field StorageDevicePhysicalTopologyProperty

Indicates that the caller is querying for topology information from the device. Data is returned using the <a href="https://msdn.microsoft.com/en-us/library/Dn933274(v=VS.85).aspx">STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR</a> structure.


### -field StorageDeviceAttributesProperty

Reserved for future use.


### -field StorageDeviceManagementStatus


### -field StorageAdapterSerialNumberProperty


### -field StorageDeviceLocationProperty


### -field StorageDeviceNumaProperty


### -field StorageDeviceZonedDeviceProperty


### -field StorageDeviceUnsafeShutdownCount




## -remarks



The optional output buffer returned through the <i>lpOutBuffer</i> parameter of the 
     <a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a> control code 
     request can be one of several structures depending on the value of the <b>PropertyId</b> 
     member of the <a href="https://msdn.microsoft.com/c97a14ab-628c-41f1-96c3-0f47654d0606">STORAGE_PROPERTY_QUERY</a> structure 
     pointed to by the <i>lpInBuffer</i> parameter. If the <b>QueryType</b> 
     member of the <b>STORAGE_PROPERTY_QUERY</b> is set to 
     <b>PropertyExistsQuery</b>, then no structure is returned.




## -see-also




<a href="https://msdn.microsoft.com/ed8fe5c1-dbdf-43bc-a0a7-17e541eba950">Disk Management Enumeration Types</a>



<a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="https://msdn.microsoft.com/c97a14ab-628c-41f1-96c3-0f47654d0606">STORAGE_PROPERTY_QUERY</a>



<a href="https://msdn.microsoft.com/0bce42d2-9d42-4881-9e33-4b3858a40353">STORAGE_QUERY_TYPE</a>
 

 

