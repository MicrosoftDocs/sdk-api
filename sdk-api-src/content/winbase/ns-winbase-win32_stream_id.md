---
UID: NS:winbase._WIN32_STREAM_ID
title: WIN32_STREAM_ID (winbase.h)
description: Contains stream data.
helpviewer_keywords: ["*LPWIN32_STREAM_ID","BACKUP_ALTERNATE_DATA","BACKUP_DATA","BACKUP_EA_DATA","BACKUP_LINK","BACKUP_OBJECT_ID","BACKUP_PROPERTY_DATA","BACKUP_REPARSE_DATA","BACKUP_SECURITY_DATA","BACKUP_SPARSE_BLOCK","BACKUP_TXFS_DATA","LPWIN32_STREAM_ID","LPWIN32_STREAM_ID structure pointer [Backup]","STREAM_CONTAINS_SECURITY","STREAM_MODIFIED_WHEN_READ","WIN32_STREAM_ID","WIN32_STREAM_ID structure [Backup]","_WIN32_STREAM_ID","_win32_win32_stream_id_str","backup.win32_stream_id_str","base.win32_stream_id_str","winbase/LPWIN32_STREAM_ID","winbase/WIN32_STREAM_ID"]
old-location: backup\win32_stream_id_str.htm
tech.root: Backup
ms.assetid: 8beb4315-ec0e-4f6f-abfe-369094f7bedd
ms.date: 12/05/2018
ms.keywords: '*LPWIN32_STREAM_ID, BACKUP_ALTERNATE_DATA, BACKUP_DATA, BACKUP_EA_DATA, BACKUP_LINK, BACKUP_OBJECT_ID, BACKUP_PROPERTY_DATA, BACKUP_REPARSE_DATA, BACKUP_SECURITY_DATA, BACKUP_SPARSE_BLOCK, BACKUP_TXFS_DATA, LPWIN32_STREAM_ID, LPWIN32_STREAM_ID structure pointer [Backup], STREAM_CONTAINS_SECURITY, STREAM_MODIFIED_WHEN_READ, WIN32_STREAM_ID, WIN32_STREAM_ID structure [Backup], _WIN32_STREAM_ID, _win32_win32_stream_id_str, backup.win32_stream_id_str, base.win32_stream_id_str, winbase/LPWIN32_STREAM_ID, winbase/WIN32_STREAM_ID'
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: WIN32_STREAM_ID, *LPWIN32_STREAM_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WIN32_STREAM_ID
 - winbase/_WIN32_STREAM_ID
 - LPWIN32_STREAM_ID
 - winbase/LPWIN32_STREAM_ID
 - WIN32_STREAM_ID
 - winbase/WIN32_STREAM_ID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winbase.h
api_name:
 - WIN32_STREAM_ID
---

# WIN32_STREAM_ID structure


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

<a href="/windows/desktop/FileIO/transactional-ntfs-portal">Transactional NTFS (TxF)</a> data stream. 
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

<a href="/windows/desktop/api/winbase/nf-winbase-backupread">BackupRead</a>



<a href="/windows/desktop/api/winbase/nf-winbase-backupseek">BackupSeek</a>



<a href="/windows/desktop/api/winbase/nf-winbase-backupwrite">BackupWrite</a>