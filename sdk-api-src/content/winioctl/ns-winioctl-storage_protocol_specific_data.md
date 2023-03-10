---
UID: NS:winioctl._STORAGE_PROTOCOL_SPECIFIC_DATA
title: STORAGE_PROTOCOL_SPECIFIC_DATA
description: Describes protocol-specific device data, provided in the input and output buffer of an IOCTL_STORAGE_QUERY_PROPERTY request.
helpviewer_keywords: ["*PSTORAGE_PROTOCOL_SPECIFIC_DATA","PSTORAGE_PROTOCOL_SPECIFIC_DATA","PSTORAGE_PROTOCOL_SPECIFIC_DATA structure pointer [Files]","STORAGE_PROTOCOL_SPECIFIC_DATA","STORAGE_PROTOCOL_SPECIFIC_DATA structure [Files]","fs.storage_protocol_specific_data","winioctl/PSTORAGE_PROTOCOL_SPECIFIC_DATA","winioctl/STORAGE_PROTOCOL_SPECIFIC_DATA"]
old-location: fs\storage_protocol_specific_data.htm
tech.root: fs
ms.assetid: 533EC957-FB37-41A7-8E5B-5A09A458D768
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_PROTOCOL_SPECIFIC_DATA, PSTORAGE_PROTOCOL_SPECIFIC_DATA, PSTORAGE_PROTOCOL_SPECIFIC_DATA structure pointer [Files], STORAGE_PROTOCOL_SPECIFIC_DATA, STORAGE_PROTOCOL_SPECIFIC_DATA structure [Files], fs.storage_protocol_specific_data, winioctl/PSTORAGE_PROTOCOL_SPECIFIC_DATA, winioctl/STORAGE_PROTOCOL_SPECIFIC_DATA'
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
req.typenames: STORAGE_PROTOCOL_SPECIFIC_DATA, *PSTORAGE_PROTOCOL_SPECIFIC_DATA
req.redist: 
f1_keywords:
 - _STORAGE_PROTOCOL_SPECIFIC_DATA
 - winioctl/_STORAGE_PROTOCOL_SPECIFIC_DATA
 - PSTORAGE_PROTOCOL_SPECIFIC_DATA
 - winioctl/PSTORAGE_PROTOCOL_SPECIFIC_DATA
 - STORAGE_PROTOCOL_SPECIFIC_DATA
 - winioctl/STORAGE_PROTOCOL_SPECIFIC_DATA
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
 - STORAGE_PROTOCOL_SPECIFIC_DATA
---

# STORAGE_PROTOCOL_SPECIFIC_DATA structure


## -description

Describes  protocol-specific device data, provided in the input and output buffer of an  <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a> request.

## -struct-fields

### -field ProtocolType

The protocol type. Values for this member are defined in the <a href="/windows/desktop/api/winioctl/ne-winioctl-storage_protocol_type">STORAGE_PROTOCOL_TYPE</a> enumeration.

### -field DataType

The protocol data type. Data types are defined in the <a href="/windows/desktop/api/winioctl/ne-winioctl-storage_protocol_nvme_data_type">STORAGE_PROTOCOL_NVME_DATA_TYPE</a> and <a href="/windows/desktop/api/winioctl/ne-winioctl-storage_protocol_ata_data_type">STORAGE_PROTOCOL_ATA_DATA_TYPE</a> enumerations.

### -field ProtocolDataRequestValue

The protocol data request value.

### -field ProtocolDataRequestSubValue

The sub value of the protocol data request.

### -field ProtocolDataOffset

The offset of the data buffer that is from the beginning of this structure. The typical value can be sizeof(<b>STORAGE_PROTOCOL_SPECIFIC_DATA</b>).

### -field ProtocolDataLength

The length of the protocol data.

### -field FixedProtocolReturnData

The returned data.

### -field ProtocolDataRequestSubValue2

### -field ProtocolDataRequestSubValue3

### -field Reserved

Reserved for future use.

## -remarks

When using <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a> to retrieve protocol-specific information in the <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_data_descriptor">STORAGE_PROTOCOL_DATA_DESCRIPTOR</a>, configure the <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_property_query">STORAGE_PROPERTY_QUERY</a> structure as follows:

<ul>
<li>
Allocate a buffer that can contains both a <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_property_query">STORAGE_PROPERTY_QUERY</a> and a <b>STORAGE_PROTOCOL_SPECIFIC_DATA</b> structure.

</li>
<li>
Set the <b>PropertyID</b>  field to <b>StorageAdapterProtocolSpecificProperty</b> or <b>StorageDeviceProtocolSpecificProperty</b> for a controller or device/namespace request, respectively.

</li>
<li>
Set the <b>QueryType</b>  field to <b>PropertyStandardQuery</b>.

</li>
<li>
Fill the <b>STORAGE_PROTOCOL_SPECIFIC_DATA</b> structure with the desired values. The start of the <b>STORAGE_PROTOCOL_SPECIFIC_DATA</b> is the <b>AdditionalParameters</b> field of <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_property_query">STORAGE_PROPERTY_QUERY</a>.

</li>
</ul>
To specify a type of NVMe protocol-specific information,  configure the <b>STORAGE_PROTOCOL_SPECIFIC_DATA</b> structure as follows:

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
To specify a type of ATA protocol-specific information,  configure the <b>STORAGE_PROTOCOL_SPECIFIC_DATA</b> structure as follows:

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