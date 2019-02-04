---
UID: NS:txfw32._TXF_LOG_RECORD_WRITE
title: TXF_LOG_RECORD_WRITE
author: windows-sdk-content
description: Contains the record for a write operation.
old-location: fs\txf_log_record_write.htm
tech.root: FileIO
ms.assetid: 754ea93e-bc82-498e-8333-eda3262aebc0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PTXF_LOG_RECORD_WRITE, PTXF_LOG_RECORD_WRITE, PTXF_LOG_RECORD_WRITE structure pointer [Files], TXF_LOG_RECORD_WRITE, TXF_LOG_RECORD_WRITE structure [Files], fs.txf_log_record_write, txfw32/PTXF_LOG_RECORD_WRITE, txfw32/TXF_LOG_RECORD_WRITE"
ms.topic: struct
req.header: txfw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - TxfW32.h
api_name:
 - TXF_LOG_RECORD_WRITE
product: Windows
targetos: Windows
req.typenames: TXF_LOG_RECORD_WRITE, *PTXF_LOG_RECORD_WRITE
req.redist: 
---

# TXF_LOG_RECORD_WRITE structure


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://msdn.microsoft.com/9ee26e7e-990e-4cd3-8180-f0fcaac2b752">Alternatives to using Transactional NTFS</a>.]

Contains the record for a write operation.


## -struct-fields




### -field Version

The version identifier for the replication record.


### -field RecordType

The record type. This member is set to <b>TXF_LOG_RECORD_TYPE_WRITE</b>.


### -field RecordLength

The length of this record, in bytes.


### -field Flags

Reserved.


### -field TxfFileId

The TxF file identifier for the file associated with this record. For more information, see <a href="https://msdn.microsoft.com/b7bdb226-69ce-4226-b826-baf9c732ec52">TXF_ID</a>.


### -field KtmGuid

The KTM transaction <b>GUID</b> for this update.


### -field ByteOffsetInFile

The starting location of the write operation, as an offset from the beginning of the file.


### -field NumBytesWritten

The number of bytes written.


### -field ByteOffsetInStructure

The offset of the data (bytes written) from the beginning of this record.


### -field FileNameLength

The length of the file name, in bytes.


### -field FileNameByteOffsetInStructure

The offset of the file name from the beginning of this record.


## -remarks



If the write operation goes beyond the end of the file, the file is being extended.




## -see-also




<a href="https://msdn.microsoft.com/b7bdb226-69ce-4226-b826-baf9c732ec52">TXF_ID</a>



<a href="https://msdn.microsoft.com/b891f763-13dd-4b40-aff3-3fccb693d76a">TXF_LOG_RECORD_BASE</a>
 

 

