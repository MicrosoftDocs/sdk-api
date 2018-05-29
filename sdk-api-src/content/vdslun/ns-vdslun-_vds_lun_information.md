---
UID: NS:vdslun._VDS_LUN_INFORMATION
title: "_VDS_LUN_INFORMATION"
author: windows-sdk-content
description: Defines information about a LUN or disk. Applications can use this structure to uniquely identify a LUN at all times.
old-location: base\vds_lun_information.htm
old-project: VDS
ms.assetid: 6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: VDS_LUN_INFORMATION, VDS_LUN_INFORMATION structure [VDS], _VDS_LUN_INFORMATION, base.vds_lun_information, vdslun/_VDS_LUN_INFORMATION
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: VDS_LUN_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	VdsLun.h
api_name:
-	VDS_LUN_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_LUN_INFORMATION structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

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
      <a href="https://msdn.microsoft.com/4fa1bd7a-c675-4588-8753-2614be444c9c">VDS_STORAGE_BUS_TYPE</a>.


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
      <a href="https://msdn.microsoft.com/88fe83cb-6d3c-40bd-a5ce-71771d2e7511">VDS_STORAGE_DEVICE_ID_DESCRIPTOR</a> 
      structure and the 
      <a href="https://msdn.microsoft.com/8cc8b6d9-e189-44af-9f2b-2222b2eb0749">VDS_STORAGE_IDENTIFIER</a> 
      structure.


### -field m_cInterconnects

The number of interconnect ports specified in <b>m_rgInterconnects</b>.


### -field m_rgInterconnects

Pointer to an array of the interconnect ports by which the LUN can be accessed. See the 
      <a href="https://msdn.microsoft.com/fc9f532b-a37f-4338-95db-6ec988131211">VDS_INTERCONNECT</a> structure.


## -remarks



The <b>VDS_LUN_INFORMATION</b> structure includes 
    fields from the SCSI Inquiry Data and Vital Product Data pages 0x80 and 0x83. The 
    <b>GetIdentificationData</b> method on both the 
    <a href="https://msdn.microsoft.com/e2fbebc0-593e-437c-a401-80e35a43da94">IVdsLun</a> and 
    <a href="https://msdn.microsoft.com/0fd6d1d4-daa6-4be3-8749-be98cd7c0288">IVdsDisk</a> interfaces return this structure. It is also 
    passed as an argument in the
    <a href="https://msdn.microsoft.com/06ba3486-9381-4898-b639-3d94b83be857">IVdsHwProviderPrivate::QueryIfCreatedLun</a> 
    method to determine whether a given provider owns a specified LUN.

To get the LUN object, use the <a href="https://msdn.microsoft.com/622a95a4-0e8c-4f65-a935-61cb48379065">IVdsService::GetObject</a> method. You can then use the <a href="https://msdn.microsoft.com/1fec1c8d-7ac9-4b77-830c-930908aac6ef">IVdsLun::GetProperties</a> method to get the LUN properties.




## -see-also




<a href="https://msdn.microsoft.com/400fa102-f98a-4bc1-919c-858c135a5b93">IVdsDisk::GetIdentificationData</a>



<a href="https://msdn.microsoft.com/06ba3486-9381-4898-b639-3d94b83be857">IVdsHwProviderPrivate::QueryIfCreatedLun</a>



<a href="https://msdn.microsoft.com/ab72cbe0-d10d-49af-87a0-4da28f79b124">IVdsLun::GetIdentificationData</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/fc9f532b-a37f-4338-95db-6ec988131211">VDS_INTERCONNECT</a>



<a href="https://msdn.microsoft.com/4fa1bd7a-c675-4588-8753-2614be444c9c">VDS_STORAGE_BUS_TYPE</a>



<a href="https://msdn.microsoft.com/88fe83cb-6d3c-40bd-a5ce-71771d2e7511">VDS_STORAGE_DEVICE_ID_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/8cc8b6d9-e189-44af-9f2b-2222b2eb0749">VDS_STORAGE_IDENTIFIER</a>
 

 

