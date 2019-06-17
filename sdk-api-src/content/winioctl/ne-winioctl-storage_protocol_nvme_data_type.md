---
UID: NE:winioctl._STORAGE_PROTOCOL_NVME_DATA_TYPE
title: STORAGE_PROTOCOL_NVME_DATA_TYPE
author: windows-sdk-content
description: Describes the type of NVMe protocol-specific data that's to be queried during an IOCTL_STORAGE_QUERY_PROPERTY request.
old-location: fs\storage_protocol_nvme_data_type.htm
tech.root: FileIO
ms.assetid: BB171CEE-1CB7-44AC-9F39-87394EFAFAEC
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PSTORAGE_PROTOCOL_NVME_DATA_TYPE, NVMeDataTypeFeature, NVMeDataTypeIdentify, NVMeDataTypeLogPage, NVMeDataTypeUnknown, PSTORAGE_PROTOCOL_NVME_DATA_TYPE, PSTORAGE_PROTOCOL_NVME_DATA_TYPE enumeration pointer [Files], STORAGE_PROTOCOL_NVME_DATA_TYPE, STORAGE_PROTOCOL_NVME_DATA_TYPE enumeration [Files], fs.storage_protocol_nvme_data_type, winioctl/NVMeDataTypeFeature, winioctl/NVMeDataTypeIdentify, winioctl/NVMeDataTypeLogPage, winioctl/NVMeDataTypeUnknown, winioctl/PSTORAGE_PROTOCOL_NVME_DATA_TYPE, winioctl/STORAGE_PROTOCOL_NVME_DATA_TYPE"
ms.topic: enum
f1_keywords: ["winioctl/STORAGE_PROTOCOL_NVME_DATA_TYPE"]
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
 - STORAGE_PROTOCOL_NVME_DATA_TYPE
product: Windows
targetos: Windows
req.typenames: STORAGE_PROTOCOL_NVME_DATA_TYPE, *PSTORAGE_PROTOCOL_NVME_DATA_TYPE
req.redist: 
---

# STORAGE_PROTOCOL_NVME_DATA_TYPE enumeration


## -description


Describes  the type of NVMe protocol-specific data that's to be queried during an <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a> request.


## -enum-fields




### -field NVMeDataTypeUnknown

Unknown data type.


### -field NVMeDataTypeIdentify

Identify data type. This can be either Identify Controller data or Identify Namespace data. When this type of data is being queried, the ProtocolDataRequestValue field of <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_storage_protocol_specific_data">STORAGE_PROTOCOL_SPECIFIC_DATA</a> will have a value of <b>NVME_IDENTIFY_CNS_CONTROLLER</b> for adapter or <b>NVME_IDENTIFY_CNS_SPECIFIC_NAMESPACE</b> for namespace. If the ProtocolDataRequestValue is <b>NVME_IDENTIFY_CNS_SPECIFIC_NAMESPACE</b>, the ProtocolDataRequestSubValue field from the <b>STORAGE_PROTOCOL_SPECIFIC_DATA</b> structure will have a value of the namespace ID.


### -field NVMeDataTypeLogPage

Log page data type.


### -field NVMeDataTypeFeature

Feature data type.


## -remarks



When using <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a> to retrieve protocol-specific information in the <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_storage_protocol_data_descriptor">STORAGE_PROTOCOL_DATA_DESCRIPTOR</a>, configure the <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_storage_property_query">STORAGE_PROPERTY_QUERY</a> structure as follows:

<ul>
<li>
Allocate a buffer that can contains both a <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_storage_property_query">STORAGE_PROPERTY_QUERY</a> and a <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_storage_protocol_specific_data">STORAGE_PROTOCOL_SPECIFIC_DATA</a> structure.

</li>
<li>
Set the <b>PropertyID</b>  field to <b>StorageAdapterProtocolSpecificProperty</b> or <b>StorageDeviceProtocolSpecificProperty</b> for a controller or device/namespace request, respectively.

</li>
<li>
Set the <b>QueryType</b>  field to <b>PropertyStandardQuery</b>.

</li>
<li>
Fill the <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_storage_protocol_specific_data">STORAGE_PROTOCOL_SPECIFIC_DATA</a> structure with the desired values. The start of the <b>STORAGE_PROTOCOL_SPECIFIC_DATA</b> is the <b>AdditionalParameters</b> field of <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_storage_property_query">STORAGE_PROPERTY_QUERY</a>.

</li>
</ul>
To specify a type of NVMe protocol-specific information,  configure the <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_storage_protocol_specific_data">STORAGE_PROTOCOL_SPECIFIC_DATA</a> structure as follows:

<ul>
<li>
Set the <b>ProtocolType</b>  field to <b>ProtocolTypeNVMe</b>.

</li>
<li>
Set the <b>DataType</b>  field to an enumeration value defined by <b>STORAGE_PROTOCOL_NVME_DATA_TYPE</b>:<ul>
<li>Use <b>NVMeDataTypeIdentify</b> to get Identify Controller data or Identify Namespace data.</li>
<li>Use <b>NVMeDataTypeLogPage</b> to get log pages (including SMART/health data).</li>
<li>Use <b>NVMeDataTypeFeature</b> to get features of the NVMe drive.</li>
</ul>


</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_storage_property_query">STORAGE_PROPERTY_QUERY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_storage_protocol_specific_data">STORAGE_PROTOCOL_SPECIFIC_DATA</a>
 

 

