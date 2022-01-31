---
UID: NE:winioctl._STORAGE_PROTOCOL_NVME_DATA_TYPE
title: STORAGE_PROTOCOL_NVME_DATA_TYPE
description: Describes the type of NVMe protocol-specific data that's to be queried during an IOCTL_STORAGE_QUERY_PROPERTY request.
helpviewer_keywords: ["*PSTORAGE_PROTOCOL_NVME_DATA_TYPE","NVMeDataTypeFeature","NVMeDataTypeIdentify","NVMeDataTypeLogPage","NVMeDataTypeUnknown","PSTORAGE_PROTOCOL_NVME_DATA_TYPE","PSTORAGE_PROTOCOL_NVME_DATA_TYPE enumeration pointer [Files]","STORAGE_PROTOCOL_NVME_DATA_TYPE","STORAGE_PROTOCOL_NVME_DATA_TYPE enumeration [Files]","fs.storage_protocol_nvme_data_type","winioctl/NVMeDataTypeFeature","winioctl/NVMeDataTypeIdentify","winioctl/NVMeDataTypeLogPage","winioctl/NVMeDataTypeUnknown","winioctl/PSTORAGE_PROTOCOL_NVME_DATA_TYPE","winioctl/STORAGE_PROTOCOL_NVME_DATA_TYPE"]
old-location: fs\storage_protocol_nvme_data_type.htm
tech.root: fs
ms.assetid: BB171CEE-1CB7-44AC-9F39-87394EFAFAEC
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_PROTOCOL_NVME_DATA_TYPE, NVMeDataTypeFeature, NVMeDataTypeIdentify, NVMeDataTypeLogPage, NVMeDataTypeUnknown, PSTORAGE_PROTOCOL_NVME_DATA_TYPE, PSTORAGE_PROTOCOL_NVME_DATA_TYPE enumeration pointer [Files], STORAGE_PROTOCOL_NVME_DATA_TYPE, STORAGE_PROTOCOL_NVME_DATA_TYPE enumeration [Files], fs.storage_protocol_nvme_data_type, winioctl/NVMeDataTypeFeature, winioctl/NVMeDataTypeIdentify, winioctl/NVMeDataTypeLogPage, winioctl/NVMeDataTypeUnknown, winioctl/PSTORAGE_PROTOCOL_NVME_DATA_TYPE, winioctl/STORAGE_PROTOCOL_NVME_DATA_TYPE'
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
targetos: Windows
req.typenames: STORAGE_PROTOCOL_NVME_DATA_TYPE, *PSTORAGE_PROTOCOL_NVME_DATA_TYPE
req.redist: 
f1_keywords:
 - _STORAGE_PROTOCOL_NVME_DATA_TYPE
 - winioctl/_STORAGE_PROTOCOL_NVME_DATA_TYPE
 - PSTORAGE_PROTOCOL_NVME_DATA_TYPE
 - winioctl/PSTORAGE_PROTOCOL_NVME_DATA_TYPE
 - STORAGE_PROTOCOL_NVME_DATA_TYPE
 - winioctl/STORAGE_PROTOCOL_NVME_DATA_TYPE
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
 - STORAGE_PROTOCOL_NVME_DATA_TYPE
---

# STORAGE_PROTOCOL_NVME_DATA_TYPE enumeration


## -description

Describes  the type of NVMe protocol-specific data that's to be queried during an [IOCTL_STORAGE_QUERY_PROPERTY](ni-winioctl-ioctl_storage_query_property.md) request.

## -enum-fields

### -field NVMeDataTypeUnknown:0

Unknown data type.

### -field NVMeDataTypeIdentify

Identify data type. This can be either Identify Controller data or Identify Namespace data. When this type of data is being queried, the ProtocolDataRequestValue field of [STORAGE_PROTOCOL_SPECIFIC_DATA](ns-winioctl-storage_protocol_specific_data.md) will have a value of **NVME_IDENTIFY_CNS_CONTROLLER** for adapter or **NVME_IDENTIFY_CNS_SPECIFIC_NAMESPACE** for namespace. If the ProtocolDataRequestValue is **NVME_IDENTIFY_CNS_SPECIFIC_NAMESPACE**, the ProtocolDataRequestSubValue field from the **STORAGE_PROTOCOL_SPECIFIC_DATA** structure will have a value of the namespace ID.

### -field NVMeDataTypeLogPage

Log page data type.

### -field NVMeDataTypeFeature

Feature data type.

## -remarks

When using [IOCTL_STORAGE_QUERY_PROPERTY](ni-winioctl-ioctl_storage_query_property.md) to retrieve protocol-specific information in the [STORAGE_PROTOCOL_DATA_DESCRIPTOR](ns-winioctl-storage_protocol_data_descriptor.md), configure the [STORAGE_PROPERTY_QUERY](ns-winioctl-storage_property_query.md) structure as follows:
* Allocate a buffer that can contains both a [STORAGE_PROPERTY_QUERY](ns-winioctl-storage_property_query.md) and a [STORAGE_PROTOCOL_SPECIFIC_DATA](ns-winioctl-storage_protocol_specific_data.md) structure.
* Set the **PropertyID** field to **StorageAdapterProtocolSpecificProperty** or **StorageDeviceProtocolSpecificProperty** for a controller or device/namespace request, respectively.
* Set the **QueryType** field to **PropertyStandardQuery**.
* Fill the [STORAGE_PROTOCOL_SPECIFIC_DATA](ns-winioctl-storage_protocol_specific_data.md) structure with the desired values. The start of the **STORAGE_PROTOCOL_SPECIFIC_DATA** is the **AdditionalParameters** field of [STORAGE_PROPERTY_QUERY](ns-winioctl-storage_property_query.md).

To specify a type of NVMe protocol-specific information,  configure the [STORAGE_PROTOCOL_SPECIFIC_DATA](ns-winioctl-storage_protocol_specific_data.md) structure as follows:
* Set the **ProtocolType** field to **ProtocolTypeNVMe**.
* Set the **DataType** field to an enumeration value defined by **STORAGE_PROTOCOL_NVME_DATA_TYPE**:
  * Use **NVMeDataTypeIdentify** to get Identify Controller data or Identify Namespace data.
  * Use **NVMeDataTypeLogPage** to get log pages (including SMART/health data).
  * Use **NVMeDataTypeFeature** to get features of the NVMe drive.

## -see-also

* [IOCTL_STORAGE_QUERY_PROPERTY](ni-winioctl-ioctl_storage_query_property.md)
* [STORAGE_PROPERTY_QUERY](ns-winioctl-storage_property_query.md)
* [STORAGE_PROTOCOL_SPECIFIC_DATA](ns-winioctl-storage_protocol_specific_data.md)

