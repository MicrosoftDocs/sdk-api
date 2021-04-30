---
UID: NS:winioctl._STORAGE_ADAPTER_DESCRIPTOR
title: STORAGE_ADAPTER_DESCRIPTOR
description: Used with the IOCTL_STORAGE_QUERY_PROPERTY control code to retrieve the storage adapter descriptor data for a device.
helpviewer_keywords: ["*PSTORAGE_ADAPTER_DESCRIPTOR","PSTORAGE_ADAPTER_DESCRIPTOR","PSTORAGE_ADAPTER_DESCRIPTOR structure pointer [Files]","SRB_TYPE_SCSI_REQUEST_BLOCK","SRB_TYPE_STORAGE_REQUEST_BLOCK","STORAGE_ADAPTER_DESCRIPTOR","STORAGE_ADAPTER_DESCRIPTOR structure [Files]","STORAGE_ADDRESS_TYPE_BTL8","fs.storage_adapter_descriptor","winioctl/PSTORAGE_ADAPTER_DESCRIPTOR","winioctl/STORAGE_ADAPTER_DESCRIPTOR"]
old-location: fs\storage_adapter_descriptor.htm
tech.root: fs
ms.assetid: 8a5059d3-09a4-4411-8d86-d1257edb409a
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_ADAPTER_DESCRIPTOR, PSTORAGE_ADAPTER_DESCRIPTOR, PSTORAGE_ADAPTER_DESCRIPTOR structure pointer [Files], SRB_TYPE_SCSI_REQUEST_BLOCK, SRB_TYPE_STORAGE_REQUEST_BLOCK, STORAGE_ADAPTER_DESCRIPTOR, STORAGE_ADAPTER_DESCRIPTOR structure [Files], STORAGE_ADDRESS_TYPE_BTL8, fs.storage_adapter_descriptor, winioctl/PSTORAGE_ADAPTER_DESCRIPTOR, winioctl/STORAGE_ADAPTER_DESCRIPTOR'
req.header: winioctl.h
req.include-header: Windows.h
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
req.typenames: STORAGE_ADAPTER_DESCRIPTOR, *PSTORAGE_ADAPTER_DESCRIPTOR
req.redist: 
f1_keywords:
 - _STORAGE_ADAPTER_DESCRIPTOR
 - winioctl/_STORAGE_ADAPTER_DESCRIPTOR
 - PSTORAGE_ADAPTER_DESCRIPTOR
 - winioctl/PSTORAGE_ADAPTER_DESCRIPTOR
 - STORAGE_ADAPTER_DESCRIPTOR
 - winioctl/STORAGE_ADAPTER_DESCRIPTOR
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
 - STORAGE_ADAPTER_DESCRIPTOR
---

# STORAGE_ADAPTER_DESCRIPTOR structure


## -description

Used with the 
   <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a> control code to 
   retrieve the storage adapter descriptor data for a device.

## -struct-fields

### -field Version

Contains the size of this structure, in bytes. The value of this member will change as members are added to 
      the structure.

### -field Size

Specifies the total size of the data returned, in bytes. This may include data that follows this 
      structure.

### -field MaximumTransferLength

Specifies the maximum number of bytes the storage adapter can transfer in a single operation.

### -field MaximumPhysicalPages

Specifies the maximum number of discontinuous physical pages the storage adapter can manage in a single 
      transfer (in other words, the extent of its scatter/gather support).

### -field AlignmentMask

Specifies the storage adapter's alignment requirements for transfers. The alignment mask indicates 
      alignment restrictions for buffers required by the storage adapter for transfer operations. Valid mask values 
      are also restricted by characteristics of the memory managers on different versions of Windows.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Buffers must be aligned on <b>BYTE</b> boundaries.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Buffers must be aligned on <b>WORD</b> boundaries.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Buffers must be aligned on <b>DWORD32</b> boundaries.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>7</dt>
</dl>
</td>
<td width="60%">
Buffers must be aligned on <b>DWORD64</b> boundaries.

</td>
</tr>
</table>

### -field AdapterUsesPio

If this member is <b>TRUE</b>, the storage adapter uses programmed I/O (PIO) and 
      requires the use of system-space virtual addresses mapped to physical memory for data buffers. When this member 
      is <b>FALSE</b>, the storage adapter does not use PIO.

### -field AdapterScansDown

If this member is <b>TRUE</b>, the storage adapter scans down for BIOS devices, that is, 
      the storage adapter begins scanning with the highest device number rather than the lowest. When this member is 
      <b>FALSE</b>, the storage adapter begins scanning with the lowest device number. This member 
      is reserved for legacy miniport drivers.

### -field CommandQueueing

If this member is <b>TRUE</b>, the storage adapter supports SCSI tagged queuing and/or 
      per-logical-unit internal queues, or the non-SCSI equivalent. When this member is 
      <b>FALSE</b>, the storage adapter neither supports SCSI-tagged queuing nor per-logical-unit 
      internal queues.

### -field AcceleratedTransfer

If this member is <b>TRUE</b>, the storage adapter supports synchronous transfers as a 
      way of speeding up I/O. When this member is <b>FALSE</b>, the storage adapter does not 
      support synchronous transfers as a way of speeding up I/O.

### -field BusType

Specifies a value of type <a href="/windows/desktop/api/winioctl/ne-winioctl-storage_bus_type">STORAGE_BUS_TYPE</a> that 
      indicates the type of the bus to which the device is connected.

### -field BusMajorVersion

Specifies the major version number, if any, of the storage adapter.

### -field BusMinorVersion

Specifies the minor version number, if any, of the storage adapter.

### -field SrbType

Specifies the SCSI request block (SRB) type used by the HBA.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SRB_TYPE_SCSI_REQUEST_BLOCK"></a><a id="srb_type_scsi_request_block"></a><dl>
<dt><b>SRB_TYPE_SCSI_REQUEST_BLOCK</b></dt>
</dl>
</td>
<td width="60%">
The HBA uses SCSI request blocks.

</td>
</tr>
<tr>
<td width="40%"><a id="SRB_TYPE_STORAGE_REQUEST_BLOCK"></a><a id="srb_type_storage_request_block"></a><dl>
<dt><b>SRB_TYPE_STORAGE_REQUEST_BLOCK</b></dt>
</dl>
</td>
<td width="60%">
The HBA uses extended SCSI request blocks.

</td>
</tr>
</table>
 

This member is valid starting with Windows 8.

### -field AddressType

Specifies the address type of the HBA.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="STORAGE_ADDRESS_TYPE_BTL8"></a><a id="storage_address_type_btl8"></a><dl>
<dt><b>STORAGE_ADDRESS_TYPE_BTL8</b></dt>
</dl>
</td>
<td width="60%">
The HBA uses 8-bit bus, target, and LUN addressing.

</td>
</tr>
</table>
 

This member is valid starting with Windows 8.

## -see-also

<a href="/windows/desktop/FileIO/disk-management-structures">Disk Management Structures</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_adapter_descriptor">STORAGE_ADAPTER_DESCRIPTOR</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_descriptor_header">STORAGE_DESCRIPTOR_HEADER</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_device_id_descriptor">STORAGE_DEVICE_ID_DESCRIPTOR</a>