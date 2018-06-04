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

# _WIN32_STREAM_ID structure


## -description


The <b>WIN32_STREAM_ID</b> structure contains stream data.


## -struct-fields




### -field dwStreamId

Type of data. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BACKUP_ALTERNATE_DATA"></a><a id="backup_alternate_data"></a><dl>
<dt><b>BACKUP_ALTERNATE_DATA</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Alternative data streams. This corresponds to the NTFS $DATA stream type on a named data stream.

</td>
</tr>
<tr>
<td width="40%"><a id="BACKUP_DATA"></a><a id="backup_data"></a><dl>
<dt><b>BACKUP_DATA</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Standard data. This corresponds to the NTFS $DATA stream type on the default (unnamed) data stream.

</td>
</tr>
<tr>
<td width="40%"><a id="BACKUP_EA_DATA"></a><a id="backup_ea_data"></a><dl>
<dt><b>BACKUP_EA_DATA</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Extended attribute data. This corresponds to the NTFS $EA stream type.

</td>
</tr>
<tr>
<td width="40%"><a id="BACKUP_LINK"></a><a id="backup_link"></a><dl>
<dt><b>BACKUP_LINK</b></dt>
<dt>0x00000005</dt>
</dl>
</td>
<td width="60%">
Hard link information. This corresponds to the NTFS $FILE_NAME stream type.

</td>
</tr>
<tr>
<td width="40%"><a id="BACKUP_OBJECT_ID"></a><a id="backup_object_id"></a><dl>
<dt><b>BACKUP_OBJECT_ID</b></dt>
<dt>0x00000007</dt>
</dl>
</td>
<td width="60%">
Objects identifiers. This corresponds to the NTFS $OBJECT_ID stream type.

</td>
</tr>
<tr>
<td width="40%"><a id="BACKUP_PROPERTY_DATA"></a><a id="backup_property_data"></a><dl>
<dt><b>BACKUP_PROPERTY_DATA</b></dt>
<dt>0x00000006</dt>
</dl>
</td>
<td width="60%">
Property data.

</td>
</tr>
<tr>
<td width="40%"><a id="BACKUP_REPARSE_DATA"></a><a id="backup_reparse_data"></a><dl>
<dt><b>BACKUP_REPARSE_DATA</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Reparse points. This corresponds to the NTFS $REPARSE_POINT stream type.

</td>
</tr>
<tr>
<td width="40%"><a id="BACKUP_SECURITY_DATA"></a><a id="backup_security_data"></a><dl>
<dt><b>BACKUP_SECURITY_DATA</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
Security descriptor data.

</td>
</tr>
<tr>
<td width="40%"><a id="BACKUP_SPARSE_BLOCK"></a><a id="backup_sparse_block"></a><dl>
<dt><b>BACKUP_SPARSE_BLOCK</b></dt>
<dt>0x00000009</dt>
</dl>
</td>
<td width="60%">
Sparse file. This corresponds to the NTFS $DATA stream type for a sparse file.

</td>
</tr>
<tr>
<td width="40%"><a id="BACKUP_TXFS_DATA"></a><a id="backup_txfs_data"></a><dl>
<dt><b>BACKUP_TXFS_DATA</b></dt>
<dt>0x0000000A</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/e8c3ceed-d391-4934-b3f7-12c2123c8c23">Transactional NTFS (TxF)</a> data stream. 
         This corresponds to the NTFS $TXF_DATA stream type.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
</table>
 


### -field dwStreamAttributes

Attributes of data to facilitate cross-operating system transfer. This member can be one or more of the 
      following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="STREAM_MODIFIED_WHEN_READ"></a><a id="stream_modified_when_read"></a><dl>
<dt><b>STREAM_MODIFIED_WHEN_READ</b></dt>
</dl>
</td>
<td width="60%">
Attribute set if the stream contains data that is modified when read. Allows the backup application to 
        know that verification of data will fail.

</td>
</tr>
<tr>
<td width="40%"><a id="STREAM_CONTAINS_SECURITY"></a><a id="stream_contains_security"></a><dl>
<dt><b>STREAM_CONTAINS_SECURITY</b></dt>
</dl>
</td>
<td width="60%">
Stream contains security data (general attributes). Allows the stream to be ignored on cross-operations 
        restore.

</td>
</tr>
</table>
 


### -field Size

Size of data, in bytes.


### -field dwStreamNameSize

Length of the name of the alternative data stream, in bytes.


### -field cStreamName

Unicode string that specifies the name of the alternative data stream.


## -see-also




<a href="https://msdn.microsoft.com/47d13662-af70-4c76-9fb6-3835e329ae5f">BackupRead</a>



<a href="https://msdn.microsoft.com/d5ffba3d-f744-49b4-83e0-e32bd45ecc4c">BackupSeek</a>



<a href="https://msdn.microsoft.com/92befb48-68eb-4af3-b58a-c5e17bf14098">BackupWrite</a>
 

 

