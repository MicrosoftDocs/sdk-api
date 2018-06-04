---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _TXF_LOG_RECORD_TRUNCATE structure


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://msdn.microsoft.com/9ee26e7e-990e-4cd3-8180-f0fcaac2b752">Alternatives to using Transactional NTFS</a>.]

Contains the record for a truncate operation.


## -struct-fields




### -field Version

The version identifier for the replication record.


### -field RecordType

The record type. This member is set to TXF_LOG_RECORD_TYPE_TRUNCATE.


### -field RecordLength

The length of this record, in bytes.


### -field Flags

Reserved.


### -field TxfFileId

The TxF file identifier for the file associated with this record. For more information, see <a href="https://msdn.microsoft.com/b7bdb226-69ce-4226-b826-baf9c732ec52">TXF_ID</a>.


### -field KtmGuid

The KTM transaction GUID for this update.


### -field NewFileSize

The new size of the file, in bytes.


### -field FileNameLength

The length of the file name, in bytes.


### -field FileNameByteOffsetInStructure

The offset of the file name from the beginning of this record.


## -see-also




<a href="https://msdn.microsoft.com/b7bdb226-69ce-4226-b826-baf9c732ec52">TXF_ID</a>



<a href="https://msdn.microsoft.com/b891f763-13dd-4b40-aff3-3fccb693d76a">TXF_LOG_RECORD_BASE</a>
 

 

