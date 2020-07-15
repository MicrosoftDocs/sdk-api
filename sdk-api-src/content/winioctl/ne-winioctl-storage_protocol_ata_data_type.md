---
UID: NE:winioctl._STORAGE_PROTOCOL_ATA_DATA_TYPE
title: STORAGE_PROTOCOL_ATA_DATA_TYPE
description: The ATA protocol data type.
helpviewer_keywords: ["*PSTORAGE_PROTOCOL_ATA_DATA_TYPE","AtaDataTypeIdentify","AtaDataTypeLogPage","AtaDataTypeUnknown","PSTORAGE_PROTOCOL_ATA_DATA_TYPE","PSTORAGE_PROTOCOL_ATA_DATA_TYPE enumeration pointer [Files]","STORAGE_PROTOCOL_ATA_DATA_TYPE","STORAGE_PROTOCOL_ATA_DATA_TYPE enumeration [Files]","fs.storage_protocol_ata_data_type","winioctl/AtaDataTypeIdentify","winioctl/AtaDataTypeLogPage","winioctl/AtaDataTypeUnknown","winioctl/PSTORAGE_PROTOCOL_ATA_DATA_TYPE","winioctl/STORAGE_PROTOCOL_ATA_DATA_TYPE"]
old-location: fs\storage_protocol_ata_data_type.htm
tech.root: FileIO
ms.assetid: 999CB5EB-9D19-41B9-B4ED-001B63C1A7EA
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_PROTOCOL_ATA_DATA_TYPE, AtaDataTypeIdentify, AtaDataTypeLogPage, AtaDataTypeUnknown, PSTORAGE_PROTOCOL_ATA_DATA_TYPE, PSTORAGE_PROTOCOL_ATA_DATA_TYPE enumeration pointer [Files], STORAGE_PROTOCOL_ATA_DATA_TYPE, STORAGE_PROTOCOL_ATA_DATA_TYPE enumeration [Files], fs.storage_protocol_ata_data_type, winioctl/AtaDataTypeIdentify, winioctl/AtaDataTypeLogPage, winioctl/AtaDataTypeUnknown, winioctl/PSTORAGE_PROTOCOL_ATA_DATA_TYPE, winioctl/STORAGE_PROTOCOL_ATA_DATA_TYPE'
f1_keywords:
- winioctl/STORAGE_PROTOCOL_ATA_DATA_TYPE
dev_langs:
- c++
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
- STORAGE_PROTOCOL_ATA_DATA_TYPE
targetos: Windows
req.typenames: STORAGE_PROTOCOL_ATA_DATA_TYPE, *PSTORAGE_PROTOCOL_ATA_DATA_TYPE
req.redist: 
---

# STORAGE_PROTOCOL_ATA_DATA_TYPE enumeration


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

The ATA protocol data type.


## -enum-fields

### -field AtaDataTypeUnknown

Unknown data type.


### -field AtaDataTypeIdentify

Identify device data type.


### -field AtaDataTypeLogPage

Log page data type.


## -remarks

When using [IOCTL_STORAGE_QUERY_PROPERTY](ni-winioctl-ioctl_storage_query_property.md) to retrieve protocol-specific information in the [STORAGE_PROTOCOL_DATA_DESCRIPTOR](ns-winioctl-storage_protocol_data_descriptor.md), configure the [STORAGE_PROPERTY_QUERY](ns-winioctl-storage_property_query.md) structure as follows:
* Allocate a buffer that can contains both a [STORAGE_PROPERTY_QUERY](ns-winioctl-storage_property_query.md) and a [STORAGE_PROTOCOL_SPECIFIC_DATA](ns-winioctl-storage_protocol_specific_data.md) structure.
* Set the **PropertyID** field to **StorageAdapterProtocolSpecificProperty** or **StorageDeviceProtocolSpecificProperty** for a controller or device/namespace request, respectively.
* Set the **QueryType** field to **PropertyStandardQuery**.
* Fill the [STORAGE_PROTOCOL_SPECIFIC_DATA](ns-winioctl-storage_protocol_specific_data.md) structure with the desired values. The start of the **STORAGE_PROTOCOL_SPECIFIC_DATA** is the **AdditionalParameters** field of [STORAGE_PROPERTY_QUERY](ns-winioctl-storage_property_query.md).

To specify a type of ATA protocol-specific information,  configure the [STORAGE_PROTOCOL_SPECIFIC_DATA](ns-winioctl-storage_protocol_specific_data.md) structure as follows:
* Set the **ProtocolType** field to **ProtocolTypeAta**.
* Set the **DataType** field to an enumeration value defined by **STORAGE_PROTOCOL_ATA_DATA_TYPE**:
  * Use **AtaDataTypeIdentify** to identify the ATA drive.
  * Use **AtaDataTypeLogPage** to get log pages from the ATA drive.


## -see-also

* [IOCTL_STORAGE_QUERY_PROPERTY](ni-winioctl-ioctl_storage_query_property.md)
* [STORAGE_PROPERTY_QUERY](ns-winioctl-storage_property_query.md)
* [STORAGE_PROTOCOL_SPECIFIC_DATA](ns-winioctl-storage_protocol_specific_data.md)
