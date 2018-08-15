---
UID: NS:winioctl._STORAGE_PROTOCOL_SPECIFIC_DATA
title: "_STORAGE_PROTOCOL_SPECIFIC_DATA"
author: windows-sdk-content
description: Describes protocol-specific device data, provided in the input and output buffer of an IOCTL_STORAGE_QUERY_PROPERTY request.
old-location: fs\storage_protocol_specific_data.htm
old-project: fileio
ms.assetid: 533EC957-FB37-41A7-8E5B-5A09A458D768
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PSTORAGE_PROTOCOL_SPECIFIC_DATA, PSTORAGE_PROTOCOL_SPECIFIC_DATA, PSTORAGE_PROTOCOL_SPECIFIC_DATA structure pointer [Files], STORAGE_PROTOCOL_SPECIFIC_DATA, STORAGE_PROTOCOL_SPECIFIC_DATA structure [Files], _STORAGE_PROTOCOL_SPECIFIC_DATA, fs.storage_protocol_specific_data, winioctl/PSTORAGE_PROTOCOL_SPECIFIC_DATA, winioctl/STORAGE_PROTOCOL_SPECIFIC_DATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: STORAGE_PROTOCOL_SPECIFIC_DATA, *PSTORAGE_PROTOCOL_SPECIFIC_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - STORAGE_PROTOCOL_SPECIFIC_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _STORAGE_PROTOCOL_SPECIFIC_DATA structure


## -description


Describes  protocol-specific device data, provided in the input and output buffer of an  <a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a> request.


## -struct-fields




### -field ProtocolType

The protocol type. Values for this member are defined in the <a href="https://msdn.microsoft.com/8055B633-99EF-4AAE-AA80-FC09F357BEAB">STORAGE_PROTOCOL_TYPE</a> enumeration.


### -field DataType

The protocol data type. Data types are defined in the <a href="https://msdn.microsoft.com/BB171CEE-1CB7-44AC-9F39-87394EFAFAEC">STORAGE_PROTOCOL_NVME_DATA_TYPE</a> and <a href="https://msdn.microsoft.com/999CB5EB-9D19-41B9-B4ED-001B63C1A7EA">STORAGE_PROTOCOL_ATA_DATA_TYPE</a> enumerations.


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

 


### -field Reserved

Reserved for future use.


## -remarks



When using <a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a> to retrieve protocol-specific information in the <a href="https://msdn.microsoft.com/BCA56343-9FB4-4079-9DB1-5DD55529B586">STORAGE_PROTOCOL_DATA_DESCRIPTOR</a>, configure the <a href="https://msdn.microsoft.com/c97a14ab-628c-41f1-96c3-0f47654d0606">STORAGE_PROPERTY_QUERY</a> structure as follows:

<ul>
<li>
Allocate a buffer that can contains both a <a href="https://msdn.microsoft.com/c97a14ab-628c-41f1-96c3-0f47654d0606">STORAGE_PROPERTY_QUERY</a> and a <b>STORAGE_PROTOCOL_SPECIFIC_DATA</b> structure.

</li>
<li>
Set the <b>PropertyID</b>  field to <b>StorageAdapterProtocolSpecificProperty</b> or <b>StorageDeviceProtocolSpecificProperty</b> for a controller or device/namespace request, respectively.

</li>
<li>
Set the <b>QueryType</b>  field to <b>PropertyStandardQuery</b>.

</li>
<li>
Fill the <b>STORAGE_PROTOCOL_SPECIFIC_DATA</b> structure with the desired values. The start of the <b>STORAGE_PROTOCOL_SPECIFIC_DATA</b> is the <b>AdditionalParameters</b> field of <a href="https://msdn.microsoft.com/c97a14ab-628c-41f1-96c3-0f47654d0606">STORAGE_PROPERTY_QUERY</a>.

</li>
</ul>
To specify a type of NVMe protocol-specific information,  configure the <b>STORAGE_PROTOCOL_SPECIFIC_DATA</b> structure as follows:

<ul>
<li>
Set the <b>ProtocolType</b>  field to <b>ProtocolTypeNVMe</b>.

</li>
<li>
Set the <b>DataType</b>  field to an enumeration value defined by <a href="https://msdn.microsoft.com/BB171CEE-1CB7-44AC-9F39-87394EFAFAEC">STORAGE_PROTOCOL_NVME_DATA_TYPE</a>:<ul>
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
Set the <b>DataType</b>  field to an enumeration value defined by <a href="https://msdn.microsoft.com/999CB5EB-9D19-41B9-B4ED-001B63C1A7EA">STORAGE_PROTOCOL_ATA_DATA_TYPE</a>:<ul>
<li>Use <b>AtaDataTypeIdentify</b> to identify the ATA drive.</li>
<li>Use <b>AtaDataTypeLogPage</b> to get log pages from the ATA drive.</li>
</ul>


</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="https://msdn.microsoft.com/c97a14ab-628c-41f1-96c3-0f47654d0606">STORAGE_PROPERTY_QUERY</a>
 

 

