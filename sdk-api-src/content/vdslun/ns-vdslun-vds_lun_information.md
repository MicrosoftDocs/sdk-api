---
UID: NS:vdslun._VDS_LUN_INFORMATION
title: VDS_LUN_INFORMATION (vdslun.h)
description: Defines information about a LUN or disk. Applications can use this structure to uniquely identify a LUN at all times.
helpviewer_keywords: ["VDS_LUN_INFORMATION","VDS_LUN_INFORMATION structure [VDS]","base.vds_lun_information","vdslun/_VDS_LUN_INFORMATION"]
old-location: base\vds_lun_information.htm
tech.root: base
ms.assetid: 6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9
ms.date: 12/05/2018
ms.keywords: VDS_LUN_INFORMATION, VDS_LUN_INFORMATION structure [VDS], base.vds_lun_information, vdslun/_VDS_LUN_INFORMATION
req.header: vdslun.h
req.include-header: Vds.h, VdsHwPrv.h for hardware providers
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: VDS_LUN_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_LUN_INFORMATION
 - vdslun/_VDS_LUN_INFORMATION
 - VDS_LUN_INFORMATION
 - vdslun/VDS_LUN_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VdsLun.h
api_name:
 - VDS_LUN_INFORMATION
---

# VDS_LUN_INFORMATION structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines 
   information about a LUN or disk. Applications can use this structure to uniquely identify a LUN at all times.

## -struct-fields

### -field m_version

The version of this structure. The current value is the constant 
      <b>VER_VDS_LUN_INFORMATION</b>.

### -field m_DeviceType

The SCSI-2 device type of the LUN.

### -field m_DeviceTypeModifier

The SCSI-2 device type modifier of the LUN. For LUNs that have no device type modifier, the value is 
      zero.

### -field m_bCommandQueueing

If <b>TRUE</b>, the LUN supports multiple outstanding commands; otherwise, 
      <b>FALSE</b>. The synchronization of the queue is the responsibility of the port 
      driver.

### -field m_BusType

The bus type of the LUN enumerated by 
      <a href="/windows/desktop/api/vdslun/ne-vdslun-vds_storage_bus_type">VDS_STORAGE_BUS_TYPE</a>.

### -field m_szVendorId

Pointer to the LUN vendor identifier; a zero-terminated, human-readable string. For devices that have no 
      vendor identifier, the value is zero.

### -field m_szProductId

Pointer to the LUN product identifier, typically a model number; a zero-terminated, human-readable string. 
      For devices that have no product identifier, the value is zero.

### -field m_szProductRevision

Pointer to the LUN product revision; a zero-terminated, human-readable string. For devices that have no 
      product revision, the value is zero.

### -field m_szSerialNumber

Pointer to the LUN serial number; a zero-terminated, human-readable string. For devices that have no serial 
      number, the value is zero.

### -field m_diskSignature

The signature of the LUN. For disks that use the Master Boot Record (MBR) partitioning structure, the first 
      32 bits of the GUID comprise the disk signature, and the remaining bits are zeros. For disks that use the GUID 
      Partition Table (GPT) partitioning structure, the GUID consists of the GPT disk identifier. If this value is 
      zero, the disk is uninitialized or the hardware provider was unable to retrieve the signature.

### -field m_deviceIdDescriptor

Array containing the LUN descriptor in various formats, such as "VDSStorageIdTypeFCPHName" 
      and "VDSStorageIdTypeVendorSpecific". Providers can use 
      "VDSStorageIdTypeVendorSpecific" to store an arbitrary byte string of the vendor's choosing to 
      uniquely identify the LUN. See the 
      <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_storage_device_id_descriptor">VDS_STORAGE_DEVICE_ID_DESCRIPTOR</a> 
      structure and the 
      <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_storage_identifier">VDS_STORAGE_IDENTIFIER</a> 
      structure.

### -field m_cInterconnects

The number of interconnect ports specified in <b>m_rgInterconnects</b>.

### -field m_rgInterconnects

Pointer to an array of the interconnect ports by which the LUN can be accessed. See the 
      <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_interconnect">VDS_INTERCONNECT</a> structure.

## -remarks

The <b>VDS_LUN_INFORMATION</b> structure includes 
    fields from the SCSI Inquiry Data and Vital Product Data pages 0x80 and 0x83. The 
    <b>GetIdentificationData</b> method on both the 
    <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdslun">IVdsLun</a> and 
    <a href="/windows/desktop/api/vds/nn-vds-ivdsdisk">IVdsDisk</a> interfaces return this structure. It is also 
    passed as an argument in the
    <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwproviderprivate-queryifcreatedlun">IVdsHwProviderPrivate::QueryIfCreatedLun</a> 
    method to determine whether a given provider owns a specified LUN.

To get the LUN object, use the <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-getobject">IVdsService::GetObject</a> method. You can then use the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-getproperties">IVdsLun::GetProperties</a> method to get the LUN properties.

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsdisk-getidentificationdata">IVdsDisk::GetIdentificationData</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwproviderprivate-queryifcreatedlun">IVdsHwProviderPrivate::QueryIfCreatedLun</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-getidentificationdata">IVdsLun::GetIdentificationData</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vdslun/ns-vdslun-vds_interconnect">VDS_INTERCONNECT</a>



<a href="/windows/desktop/api/vdslun/ne-vdslun-vds_storage_bus_type">VDS_STORAGE_BUS_TYPE</a>



<a href="/windows/desktop/api/vdslun/ns-vdslun-vds_storage_device_id_descriptor">VDS_STORAGE_DEVICE_ID_DESCRIPTOR</a>



<a href="/windows/desktop/api/vdslun/ns-vdslun-vds_storage_identifier">VDS_STORAGE_IDENTIFIER</a>