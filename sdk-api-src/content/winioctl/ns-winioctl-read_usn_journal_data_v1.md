---
UID: NS:winioctl.READ_USN_JOURNAL_DATA_V1
title: READ_USN_JOURNAL_DATA_V1
description: Contains information defining a set of update sequence number (USN) change journal records to return to the calling process.R
helpviewer_keywords: ["*PREAD_USN_JOURNAL_DATA","*PREAD_USN_JOURNAL_DATA_V1","PREAD_USN_JOURNAL_DATA","PREAD_USN_JOURNAL_DATA structure pointer [Files]","PREAD_USN_JOURNAL_DATA_V0","PREAD_USN_JOURNAL_DATA_V0 structure pointer [Files]","READ_USN_JOURNAL_DATA","READ_USN_JOURNAL_DATA structure [Files]","READ_USN_JOURNAL_DATA_V0","READ_USN_JOURNAL_DATA_V0 structure [Files]","READ_USN_JOURNAL_DATA_V1","USN_REASON_BASIC_INFO_CHANGE","USN_REASON_CLOSE","USN_REASON_COMPRESSION_CHANGE","USN_REASON_DATA_EXTEND","USN_REASON_DATA_OVERWRITE","USN_REASON_DATA_TRUNCATION","USN_REASON_EA_CHANGE","USN_REASON_ENCRYPTION_CHANGE","USN_REASON_FILE_CREATE","USN_REASON_FILE_DELETE","USN_REASON_HARD_LINK_CHANGE","USN_REASON_INDEXABLE_CHANGE","USN_REASON_NAMED_DATA_EXTEND","USN_REASON_NAMED_DATA_OVERWRITE","USN_REASON_NAMED_DATA_TRUNCATION","USN_REASON_OBJECT_ID_CHANGE","USN_REASON_RENAME_NEW_NAME","USN_REASON_RENAME_OLD_NAME","USN_REASON_REPARSE_POINT_CHANGE","USN_REASON_SECURITY_CHANGE","USN_REASON_STREAM_CHANGE","_win32_read_usn_journal_data_str","base.read_usn_journal_data_str","fs.read_usn_journal_data_str","winioctl/PREAD_USN_JOURNAL_DATA","winioctl/PREAD_USN_JOURNAL_DATA_V0","winioctl/READ_USN_JOURNAL_DATA","winioctl/READ_USN_JOURNAL_DATA_v0"]
old-location: fs\read_usn_journal_data_str.htm
tech.root: fs
ms.assetid: f88e71ba-6099-4928-9d71-732a4ca809bc
ms.date: 12/05/2018
ms.keywords: '*PREAD_USN_JOURNAL_DATA, *PREAD_USN_JOURNAL_DATA_V1, PREAD_USN_JOURNAL_DATA, PREAD_USN_JOURNAL_DATA structure pointer [Files], PREAD_USN_JOURNAL_DATA_V0, PREAD_USN_JOURNAL_DATA_V0 structure pointer [Files], READ_USN_JOURNAL_DATA, READ_USN_JOURNAL_DATA structure [Files], READ_USN_JOURNAL_DATA_V0, READ_USN_JOURNAL_DATA_V0 structure [Files], READ_USN_JOURNAL_DATA_V1, USN_REASON_BASIC_INFO_CHANGE, USN_REASON_CLOSE, USN_REASON_COMPRESSION_CHANGE, USN_REASON_DATA_EXTEND, USN_REASON_DATA_OVERWRITE, USN_REASON_DATA_TRUNCATION, USN_REASON_EA_CHANGE, USN_REASON_ENCRYPTION_CHANGE, USN_REASON_FILE_CREATE, USN_REASON_FILE_DELETE, USN_REASON_HARD_LINK_CHANGE, USN_REASON_INDEXABLE_CHANGE, USN_REASON_NAMED_DATA_EXTEND, USN_REASON_NAMED_DATA_OVERWRITE, USN_REASON_NAMED_DATA_TRUNCATION, USN_REASON_OBJECT_ID_CHANGE, USN_REASON_RENAME_NEW_NAME, USN_REASON_RENAME_OLD_NAME, USN_REASON_REPARSE_POINT_CHANGE, USN_REASON_SECURITY_CHANGE, USN_REASON_STREAM_CHANGE, _win32_read_usn_journal_data_str, base.read_usn_journal_data_str, fs.read_usn_journal_data_str, winioctl/PREAD_USN_JOURNAL_DATA, winioctl/PREAD_USN_JOURNAL_DATA_V0, winioctl/READ_USN_JOURNAL_DATA, winioctl/READ_USN_JOURNAL_DATA_v0'
req.header: winioctl.h
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
req.typenames: READ_USN_JOURNAL_DATA_V1, *PREAD_USN_JOURNAL_DATA_V1
req.redist: 
f1_keywords:
 - PREAD_USN_JOURNAL_DATA_V1
 - winioctl/PREAD_USN_JOURNAL_DATA_V1
 - READ_USN_JOURNAL_DATA_V1
 - winioctl/READ_USN_JOURNAL_DATA_V1
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
 - READ_USN_JOURNAL_DATA_V1
---

# READ_USN_JOURNAL_DATA_V1 structure


## -description

Contains information defining a set of update sequence number (USN) change journal records to return 
    to the calling process. It is used by the 
    <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_query_usn_journal">FSCTL_QUERY_USN_JOURNAL</a> and 
    <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_read_usn_journal">FSCTL_READ_USN_JOURNAL</a> control codes. Prior to 
    Windows 8 and Windows Server 2012 this structure was named 
    <b>READ_USN_JOURNAL_DATA</b>. Use that name to compile 
    with older SDKs and compilers. Windows Server 2012 introduced 
    <a href="/previous-versions/windows/desktop/legacy/hh802706(v=vs.85)">READ_USN_JOURNAL_DATA_V1</a> to support 128-bit file 
    identifiers used by ReFS.

## -struct-fields

### -field StartUsn

The USN at which to begin reading the change journal.

To start the read operation at the first record in the journal, set the <b>StartUsn</b> 
       member to zero. Because a USN is contained in every journal record, the output buffer tells at which record the 
       read operation actually started.

To start the read operation at a specific record, set <b>StartUsn</b> to that record 
       USN.

If a nonzero USN is specified that is less than the first USN in the change journal, then an error occurs and 
       the <b>ERROR_JOURNAL_ENTRY_DELETED</b> error code is returned. This code may indicate a case 
       in which the specified USN is valid at one time but has since been deleted.

For more information on navigating the change journal buffer returned in 
       <b>READ_USN_JOURNAL_DATA_V0</b>, see 
       <a href="/windows/desktop/FileIO/walking-a-buffer-of-change-journal-records">Walking a Buffer of Change Journal Records</a>.

### -field ReasonMask

A mask of flags, each flag noting a change for which the file or directory has a record in the change 
       journal. To be returned in a 
       <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_read_usn_journal">FSCTL_READ_USN_JOURNAL</a> operation, a 
       change journal record must have at least one of these flags set.

The list of valid flags is as follows. Unused bits are reserved.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_BASIC_INFO_CHANGE"></a><a id="usn_reason_basic_info_change"></a><dl>
<dt><b>USN_REASON_BASIC_INFO_CHANGE</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
A user has either changed one or more file or directory attributes (such as the read-only, hidden, 
        system, archive, or sparse attribute), or one or more time stamps.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_CLOSE"></a><a id="usn_reason_close"></a><dl>
<dt><b>USN_REASON_CLOSE</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
The file or directory is closed.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_COMPRESSION_CHANGE"></a><a id="usn_reason_compression_change"></a><dl>
<dt><b>USN_REASON_COMPRESSION_CHANGE</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
The compression state of the file or directory is changed from or to compressed.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_DATA_EXTEND"></a><a id="usn_reason_data_extend"></a><dl>
<dt><b>USN_REASON_DATA_EXTEND</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The file or directory is added to.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_DATA_OVERWRITE"></a><a id="usn_reason_data_overwrite"></a><dl>
<dt><b>USN_REASON_DATA_OVERWRITE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Data in the file or directory is overwritten.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_DATA_TRUNCATION"></a><a id="usn_reason_data_truncation"></a><dl>
<dt><b>USN_REASON_DATA_TRUNCATION</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The file or directory is truncated.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_EA_CHANGE"></a><a id="usn_reason_ea_change"></a><dl>
<dt><b>USN_REASON_EA_CHANGE</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
The user makes a change to the file or directory extended attributes. These NTFS file system attributes 
        are not accessible to Windows-based applications.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_ENCRYPTION_CHANGE"></a><a id="usn_reason_encryption_change"></a><dl>
<dt><b>USN_REASON_ENCRYPTION_CHANGE</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
The file or directory is encrypted or decrypted.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_FILE_CREATE"></a><a id="usn_reason_file_create"></a><dl>
<dt><b>USN_REASON_FILE_CREATE</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
The file or directory is created for the first time.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_FILE_DELETE"></a><a id="usn_reason_file_delete"></a><dl>
<dt><b>USN_REASON_FILE_DELETE</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
The file or directory is deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_HARD_LINK_CHANGE"></a><a id="usn_reason_hard_link_change"></a><dl>
<dt><b>USN_REASON_HARD_LINK_CHANGE</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
An NTFS file system hard link is added to or removed from the file or directory. An NTFS file system hard 
        link, similar to a POSIX hard link, is one of several directory entries that see the same file or 
        directory.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_INDEXABLE_CHANGE"></a><a id="usn_reason_indexable_change"></a><dl>
<dt><b>USN_REASON_INDEXABLE_CHANGE</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
A user changed the <b>FILE_ATTRIBUTE_NOT_CONTENT_INDEXED</b> attribute. That is, the 
        user changed the file or directory from one that can be content indexed to one that cannot, or vice versa. 
        (Content indexing permits rapid searching of data by building a database of selected content.)

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_NAMED_DATA_EXTEND"></a><a id="usn_reason_named_data_extend"></a><dl>
<dt><b>USN_REASON_NAMED_DATA_EXTEND</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
One or more named data streams for the file were added to.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_NAMED_DATA_OVERWRITE"></a><a id="usn_reason_named_data_overwrite"></a><dl>
<dt><b>USN_REASON_NAMED_DATA_OVERWRITE</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Data in one or more named data streams for the file is overwritten.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_NAMED_DATA_TRUNCATION"></a><a id="usn_reason_named_data_truncation"></a><dl>
<dt><b>USN_REASON_NAMED_DATA_TRUNCATION</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
One or more named data streams for the file is truncated.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_OBJECT_ID_CHANGE"></a><a id="usn_reason_object_id_change"></a><dl>
<dt><b>USN_REASON_OBJECT_ID_CHANGE</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
The object identifier of the file or directory is changed.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_RENAME_NEW_NAME"></a><a id="usn_reason_rename_new_name"></a><dl>
<dt><b>USN_REASON_RENAME_NEW_NAME</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
The file or directory is renamed, and the file name in the 
        <a href="/windows/desktop/api/winioctl/ns-winioctl-usn_record_v2">USN_RECORD_V2</a> or 
        <a href="/windows/desktop/api/winioctl/ns-winioctl-usn_record_v3">USN_RECORD_V3</a> structure holding this journal record is the 
        new name.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_RENAME_OLD_NAME"></a><a id="usn_reason_rename_old_name"></a><dl>
<dt><b>USN_REASON_RENAME_OLD_NAME</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
The file or directory is renamed, and the file name in the 
        <a href="/windows/desktop/api/winioctl/ns-winioctl-usn_record_v2">USN_RECORD_V2</a> or 
        <a href="/windows/desktop/api/winioctl/ns-winioctl-usn_record_v3">USN_RECORD_V3</a> structure holding this journal record is the 
        previous name.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_REPARSE_POINT_CHANGE"></a><a id="usn_reason_reparse_point_change"></a><dl>
<dt><b>USN_REASON_REPARSE_POINT_CHANGE</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
The reparse point contained in the file or directory is changed, or a reparse point is added to or 
        deleted from the file or directory.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_SECURITY_CHANGE"></a><a id="usn_reason_security_change"></a><dl>
<dt><b>USN_REASON_SECURITY_CHANGE</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
A change is made in the access permissions to the file or directory.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_STREAM_CHANGE"></a><a id="usn_reason_stream_change"></a><dl>
<dt><b>USN_REASON_STREAM_CHANGE</b></dt>
<dt>0x00200000</dt>
</dl>
</td>
<td width="60%">
A named stream is added to or removed from the file or directory, or a named stream is renamed.

</td>
</tr>
</table>

### -field ReturnOnlyOnClose

A value that specifies when to return change journal records.

To receive notification when the final handle for the changed file or directory is closed, rather than at the 
       time a change occurs, set <b>ReturnOnlyOnClose</b> to any nonzero value and specify the 
       <b>USN_REASON_CLOSE</b> flag in the <b>ReasonMask</b> member.

All changes indicated by <b>ReasonMask</b> flags eventually generate a call to the change 
       journal software when the file is closed. If your 
       <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> call is waiting for the file to be 
       closed, that call in turn will allow your 
       <b>DeviceIoControl</b> call to return. In the event that a 
       file or directory is not closed prior to a volume failure, operating system failure, or shutdown, a cleanup 
       call to the change journal software occurs the next time the volume is mounted. The call occurs even if there 
       is an intervening system restart.

To receive notification the first time each change is logged, as well as at cleanup, set 
       <b>ReturnOnlyOnClose</b> to zero.

Whether <b>ReturnOnlyOnClose</b> is zero or nonzero, the records generated at cleanup log 
       within the change journal all reasons for USN changes that occurred to the file or directory. Each time a final 
       close operation occurs for an item, a USN close record is written to the change journal, and the 
       <b>ReasonMask</b> flags for the item are all reset.

For a file or directory for which no user data exists (for example, a mounted folder), the final close 
       operation occurs when the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function is 
       called on the last user handle to the item.

### -field Timeout

The time-out value, in seconds, used with the <b>BytesToWaitFor</b> member to tell the 
       operating system what to do if the 
       <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_read_usn_journal">FSCTL_READ_USN_JOURNAL</a> operation 
       requests more data than exists in the change journal.

If <b>Timeout</b> is zero and <b>BytesToWaitFor</b> is nonzero, and 
       the <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_read_usn_journal">FSCTL_READ_USN_JOURNAL</a> operation call reaches 
       the end of the change journal without finding data to return, 
       <b>FSCTL_READ_USN_JOURNAL</b> waits until 
       <b>BytesToWaitFor</b> bytes of unfiltered data have been added to the change journal and 
       then retrieves the specified records.

If <b>Timeout</b> is nonzero and <b>BytesToWaitFor</b> is nonzero, 
       and the <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_read_usn_journal">FSCTL_READ_USN_JOURNAL</a> operation call 
       reaches the end of the change journal without finding data to return, 
       <b>FSCTL_READ_USN_JOURNAL</b> waits 
       <b>Timeout</b> seconds and then attempts to return the specified records. After 
       <b>Timeout</b> seconds, 
       <b>FSCTL_READ_USN_JOURNAL</b> retrieves any records 
       available within the specified range.

In either case, after the time-out period any new data appended to the change journal is processed. If there 
       are still no records to return from the specified set, the time-out period is repeated. In this mode, 
       <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_read_usn_journal">FSCTL_READ_USN_JOURNAL</a> remains outstanding until 
       at least one record is returned or I/O is canceled.

If <b>BytesToWaitFor</b> is zero, then <b>Timeout</b> is ignored. 
       <b>Timeout</b> is also ignored for asynchronously opened handles.

### -field BytesToWaitFor

The number of bytes of unfiltered data added to the change journal. Use this value with 
       <b>Timeout</b> to tell the operating system what to do if the 
       <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_read_usn_journal">FSCTL_READ_USN_JOURNAL</a> operation requests more 
       data than exists in the change journal.

If <b>BytesToWaitFor</b> is zero, then <b>Timeout</b> is ignored. In 
       this case, the <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_read_usn_journal">FSCTL_READ_USN_JOURNAL</a> operation 
       always returns successfully when the end of the change journal file is encountered. It also retrieves the USN 
       that should be used for the next 
       <b>FSCTL_READ_USN_JOURNAL</b> operation. When the 
       returned next USN is the same as the <b>StartUsn</b> supplied, there are no records 
       available. The calling process should not use 
       <b>FSCTL_READ_USN_JOURNAL</b> again immediately.

Because the amount of data returned cannot be predicted when <b>BytesToWaitFor</b> is 
       zero, you run a risk of overflowing the output buffer. To reduce this risk, specify a nonzero 
       <b>BytesToWaitFor</b> value in repeated 
       <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_read_usn_journal">FSCTL_READ_USN_JOURNAL</a> operations until all 
       records in the change journal are exhausted. Then specify zero to await new records.

Alternatively, use the <i>lpBytesReturned</i> parameter of 
       <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> in the 
       <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_read_usn_journal">FSCTL_READ_USN_JOURNAL</a> operation call to 
       determine the amount of data available, reallocate the output buffer (with room to spare for new records), and 
       call <b>DeviceIoControl</b> again.

### -field UsnJournalID

The identifier for the instance of the journal that is current for the volume.

The NTFS file system can miss putting events in the change journal if the change journal is stopped and 
       restarted or deleted and re-created. If either of these events occurs, the NTFS file system gives the journal a 
       new identifier. If the journal identifier does not agree with the current journal identifier, the call to 
       <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> fails and returns an appropriate 
       error code. To retrieve the new journal identifier, call 
       <b>DeviceIoControl</b> with the 
       <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_query_usn_journal">FSCTL_QUERY_USN_JOURNAL</a> 
       operation.

### -field MinMajorVersion

### -field MaxMajorVersion

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_query_usn_journal">FSCTL_QUERY_USN_JOURNAL</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_read_usn_journal">FSCTL_READ_USN_JOURNAL</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-usn_record_v2">USN_RECORD</a>

