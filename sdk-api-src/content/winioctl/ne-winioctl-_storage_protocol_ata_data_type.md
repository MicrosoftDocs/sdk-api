---
UID: NE:winioctl._STORAGE_PROTOCOL_ATA_DATA_TYPE
title: "_STORAGE_PROTOCOL_ATA_DATA_TYPE"
author: windows-sdk-content
description: The ATA protocol data type.
old-location: fs\storage_protocol_ata_data_type.htm
tech.root: fileio
ms.assetid: 999CB5EB-9D19-41B9-B4ED-001B63C1A7EA
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PSTORAGE_PROTOCOL_ATA_DATA_TYPE, AtaDataTypeIdentify, AtaDataTypeLogPage, AtaDataTypeUnknown, PSTORAGE_PROTOCOL_ATA_DATA_TYPE, PSTORAGE_PROTOCOL_ATA_DATA_TYPE enumeration pointer [Files], STORAGE_PROTOCOL_ATA_DATA_TYPE, STORAGE_PROTOCOL_ATA_DATA_TYPE enumeration [Files], _STORAGE_PROTOCOL_ATA_DATA_TYPE, fs.storage_protocol_ata_data_type, winioctl/AtaDataTypeIdentify, winioctl/AtaDataTypeLogPage, winioctl/AtaDataTypeUnknown, winioctl/PSTORAGE_PROTOCOL_ATA_DATA_TYPE, winioctl/STORAGE_PROTOCOL_ATA_DATA_TYPE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
product: Windows
targetos: Windows
req.typenames: STORAGE_PROTOCOL_ATA_DATA_TYPE, *PSTORAGE_PROTOCOL_ATA_DATA_TYPE
req.redist: 
---

# _STORAGE_PROTOCOL_ATA_DATA_TYPE enumeration


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



When using <a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a> to retrieve protocol-specific information in the <a href="https://msdn.microsoft.com/BCA56343-9FB4-4079-9DB1-5DD55529B586">STORAGE_PROTOCOL_DATA_DESCRIPTOR</a>, configure the <a href="https://msdn.microsoft.com/c97a14ab-628c-41f1-96c3-0f47654d0606">STORAGE_PROPERTY_QUERY</a> structure as follows:

<ul>
<li>
Allocate a buffer that can contains both a <a href="https://msdn.microsoft.com/c97a14ab-628c-41f1-96c3-0f47654d0606">STORAGE_PROPERTY_QUERY</a> and a <a href="https://msdn.microsoft.com/533EC957-FB37-41A7-8E5B-5A09A458D768">STORAGE_PROTOCOL_SPECIFIC_DATA</a> structure.

</li>
<li>
Set the <b>PropertyID</b>  field to <b>StorageAdapterProtocolSpecificProperty</b> or <b>StorageDeviceProtocolSpecificProperty</b> for a controller or device/namespace request, respectively.

</li>
<li>
Set the <b>QueryType</b>  field to <b>PropertyStandardQuery</b>.

</li>
<li>
Fill the <a href="https://msdn.microsoft.com/533EC957-FB37-41A7-8E5B-5A09A458D768">STORAGE_PROTOCOL_SPECIFIC_DATA</a> structure with the desired values. The start of the <b>STORAGE_PROTOCOL_SPECIFIC_DATA</b> is the <b>AdditionalParameters</b> field of <a href="https://msdn.microsoft.com/c97a14ab-628c-41f1-96c3-0f47654d0606">STORAGE_PROPERTY_QUERY</a>.

</li>
</ul>
To specify a type of ATA protocol-specific information,  configure the <a href="https://msdn.microsoft.com/533EC957-FB37-41A7-8E5B-5A09A458D768">STORAGE_PROTOCOL_SPECIFIC_DATA</a> structure as follows:

<ul>
<li>
Set the <b>ProtocolType</b>  field to <b>ProtocolTypeAta</b>.

</li>
<li>
Set the <b>DataType</b>  field to an enumeration value defined by <b>STORAGE_PROTOCOL_ATA_DATA_TYPE</b>:<ul>
<li>Use <b>AtaDataTypeIdentify</b> to identify the ATA drive.</li>
<li>Use <b>AtaDataTypeLogPage</b> to get log pages from the ATA drive.</li>
</ul>


</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="https://msdn.microsoft.com/c97a14ab-628c-41f1-96c3-0f47654d0606">STORAGE_PROPERTY_QUERY</a>



<a href="https://msdn.microsoft.com/533EC957-FB37-41A7-8E5B-5A09A458D768">STORAGE_PROTOCOL_SPECIFIC_DATA</a>
 

 

