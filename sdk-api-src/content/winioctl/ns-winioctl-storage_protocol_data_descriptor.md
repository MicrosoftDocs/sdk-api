---
UID: NS:winioctl._STORAGE_PROTOCOL_DATA_DESCRIPTOR
title: STORAGE_PROTOCOL_DATA_DESCRIPTOR
description: This structure is used in conjunction with IOCTL_STORAGE_QUERY_PROPERTY to return protocol-specific data from a storage device or adapter.
helpviewer_keywords: ["*PSTORAGE_PROTOCOL_DATA_DESCRIPTOR","PSTORAGE_PROTOCOL_DATA_DESCRIPTOR","PSTORAGE_PROTOCOL_DATA_DESCRIPTOR structure pointer [Files]","STORAGE_PROTOCOL_DATA_DESCRIPTOR","STORAGE_PROTOCOL_DATA_DESCRIPTOR structure [Files]","fs.storage_protocol_data_descriptor","winioctl/PSTORAGE_PROTOCOL_DATA_DESCRIPTOR","winioctl/STORAGE_PROTOCOL_DATA_DESCRIPTOR"]
old-location: fs\storage_protocol_data_descriptor.htm
tech.root: fs
ms.assetid: BCA56343-9FB4-4079-9DB1-5DD55529B586
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_PROTOCOL_DATA_DESCRIPTOR, PSTORAGE_PROTOCOL_DATA_DESCRIPTOR, PSTORAGE_PROTOCOL_DATA_DESCRIPTOR structure pointer [Files], STORAGE_PROTOCOL_DATA_DESCRIPTOR, STORAGE_PROTOCOL_DATA_DESCRIPTOR structure [Files], fs.storage_protocol_data_descriptor, winioctl/PSTORAGE_PROTOCOL_DATA_DESCRIPTOR, winioctl/STORAGE_PROTOCOL_DATA_DESCRIPTOR'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
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
req.typenames: STORAGE_PROTOCOL_DATA_DESCRIPTOR, *PSTORAGE_PROTOCOL_DATA_DESCRIPTOR
req.redist: 
f1_keywords:
 - _STORAGE_PROTOCOL_DATA_DESCRIPTOR
 - winioctl/_STORAGE_PROTOCOL_DATA_DESCRIPTOR
 - PSTORAGE_PROTOCOL_DATA_DESCRIPTOR
 - winioctl/PSTORAGE_PROTOCOL_DATA_DESCRIPTOR
 - STORAGE_PROTOCOL_DATA_DESCRIPTOR
 - winioctl/STORAGE_PROTOCOL_DATA_DESCRIPTOR
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
 - STORAGE_PROTOCOL_DATA_DESCRIPTOR
---

# STORAGE_PROTOCOL_DATA_DESCRIPTOR structure


## -description

This structure is used in conjunction with <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a> to return protocol-specific data from a storage device or adapter. .

## -struct-fields

### -field Version

The version of this structure.

### -field Size

The total size of the descriptor, including the space for all protocol data.

### -field ProtocolSpecificData

The protocol-specific data, of type <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_specific_data">STORAGE_PROTOCOL_SPECIFIC_DATA</a>.

## -remarks

When using <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a> to retrieve protocol-specific information in the <b>STORAGE_PROTOCOL_DATA_DESCRIPTOR</b>, configure the <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_property_query">STORAGE_PROPERTY_QUERY</a> structure as follows:

<ul>
<li>
Allocate a buffer that can contains both a <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_property_query">STORAGE_PROPERTY_QUERY</a> and a <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_specific_data">STORAGE_PROTOCOL_SPECIFIC_DATA</a> structure.

</li>
<li>
Set the <b>PropertyID</b>  field to <b>StorageAdapterProtocolSpecificProperty</b> or <b>StorageDeviceProtocolSpecificProperty</b> for a controller or device/namespace request, respectively.

</li>
<li>
Set the <b>QueryType</b>  field to <b>PropertyStandardQuery</b>.

</li>
<li>
Fill the <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_specific_data">STORAGE_PROTOCOL_SPECIFIC_DATA</a> structure with the desired values. The start of the <b>STORAGE_PROTOCOL_SPECIFIC_DATA</b> is the <b>AdditionalParameters</b> field of <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_property_query">STORAGE_PROPERTY_QUERY</a>.

</li>
</ul>
To specify a type of NVMe protocol-specific information,  configure the <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_specific_data">STORAGE_PROTOCOL_SPECIFIC_DATA</a> structure as follows:

<ul>
<li>
Set the <b>ProtocolType</b>  field to <b>ProtocolTypeNVMe</b>.

</li>
<li>
Set the <b>DataType</b>  field to an enumeration value defined by <a href="/windows/desktop/api/winioctl/ne-winioctl-storage_protocol_nvme_data_type">STORAGE_PROTOCOL_NVME_DATA_TYPE</a>:<ul>
<li>Use <b>NVMeDataTypeIdentify</b> to get Identify Controller data or Identify Namespace data.</li>
<li>Use <b>NVMeDataTypeLogPage</b> to get log pages (including SMART/health data).</li>
<li>Use <b>NVMeDataTypeFeature</b> to get features of the NVMe drive.</li>
</ul>


</li>
</ul>
To specify a type of ATA protocol-specific information,  configure the <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_specific_data">STORAGE_PROTOCOL_SPECIFIC_DATA</a> structure as follows:

<ul>
<li>
Set the <b>ProtocolType</b>  field to <b>ProtocolTypeAta</b>.

</li>
<li>
Set the <b>DataType</b>  field to an enumeration value defined by <a href="/windows/desktop/api/winioctl/ne-winioctl-storage_protocol_ata_data_type">STORAGE_PROTOCOL_ATA_DATA_TYPE</a>:<ul>
<li>Use <b>AtaDataTypeIdentify</b> to identify the ATA drive.</li>
<li>Use <b>AtaDataTypeLogPage</b> to get log pages from the ATA drive.</li>
</ul>


</li>
</ul>

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_property_query">STORAGE_PROPERTY_QUERY</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_specific_data">STORAGE_PROTOCOL_SPECIFIC_DATA</a>