---
UID: NS:winioctl.USN_RECORD_V3
title: USN_RECORD_V3
description: Contains the information for an update sequence number (USN) change journal version 3.0 record.
helpviewer_keywords: ["*PUSN_RECORD_V3","PUSN_RECORD_V3","PUSN_RECORD_V3 structure pointer [Files]","USN_REASON_BASIC_INFO_CHANGE","USN_REASON_CLOSE","USN_REASON_COMPRESSION_CHANGE","USN_REASON_DATA_EXTEND","USN_REASON_DATA_OVERWRITE","USN_REASON_DATA_TRUNCATION","USN_REASON_EA_CHANGE","USN_REASON_ENCRYPTION_CHANGE","USN_REASON_FILE_CREATE","USN_REASON_FILE_DELETE","USN_REASON_HARD_LINK_CHANGE","USN_REASON_INDEXABLE_CHANGE","USN_REASON_INTEGRITY_CHANGE","USN_REASON_NAMED_DATA_EXTEND","USN_REASON_NAMED_DATA_OVERWRITE","USN_REASON_NAMED_DATA_TRUNCATION","USN_REASON_OBJECT_ID_CHANGE","USN_REASON_RENAME_NEW_NAME","USN_REASON_RENAME_OLD_NAME","USN_REASON_REPARSE_POINT_CHANGE","USN_REASON_SECURITY_CHANGE","USN_REASON_STREAM_CHANGE","USN_REASON_TRANSACTED_CHANGE","USN_RECORD_V3","USN_RECORD_V3 structure [Files]","USN_SOURCE_AUXILIARY_DATA","USN_SOURCE_CLIENT_REPLICATION_MANAGEMENT","USN_SOURCE_DATA_MANAGEMENT","USN_SOURCE_REPLICATION_MANAGEMENT","fs.usn_record_v3","winioctl/PUSN_RECORD_V3","winioctl/USN_RECORD_V3"]
old-location: fs\usn_record_v3.htm
tech.root: fs
ms.assetid: 6d95c5d1-6c6b-498f-a00d-eaa540e8b15b
ms.date: 12/05/2018
ms.keywords: '*PUSN_RECORD_V3, PUSN_RECORD_V3, PUSN_RECORD_V3 structure pointer [Files], USN_REASON_BASIC_INFO_CHANGE, USN_REASON_CLOSE, USN_REASON_COMPRESSION_CHANGE, USN_REASON_DATA_EXTEND, USN_REASON_DATA_OVERWRITE, USN_REASON_DATA_TRUNCATION, USN_REASON_EA_CHANGE, USN_REASON_ENCRYPTION_CHANGE, USN_REASON_FILE_CREATE, USN_REASON_FILE_DELETE, USN_REASON_HARD_LINK_CHANGE, USN_REASON_INDEXABLE_CHANGE, USN_REASON_INTEGRITY_CHANGE, USN_REASON_NAMED_DATA_EXTEND, USN_REASON_NAMED_DATA_OVERWRITE, USN_REASON_NAMED_DATA_TRUNCATION, USN_REASON_OBJECT_ID_CHANGE, USN_REASON_RENAME_NEW_NAME, USN_REASON_RENAME_OLD_NAME, USN_REASON_REPARSE_POINT_CHANGE, USN_REASON_SECURITY_CHANGE, USN_REASON_STREAM_CHANGE, USN_REASON_TRANSACTED_CHANGE, USN_RECORD_V3, USN_RECORD_V3 structure [Files], USN_SOURCE_AUXILIARY_DATA, USN_SOURCE_CLIENT_REPLICATION_MANAGEMENT, USN_SOURCE_DATA_MANAGEMENT, USN_SOURCE_REPLICATION_MANAGEMENT, fs.usn_record_v3, winioctl/PUSN_RECORD_V3, winioctl/USN_RECORD_V3'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: USN_RECORD_V3, *PUSN_RECORD_V3
req.redist: 
f1_keywords:
 - PUSN_RECORD_V3
 - winioctl/PUSN_RECORD_V3
 - USN_RECORD_V3
 - winioctl/USN_RECORD_V3
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
 - USN_RECORD_V3
---

# USN_RECORD_V3 structure


## -description

Contains the information for an update sequence number (USN) change journal version 3.0 
    record. The version 2.0 record is defined by the 
    <a href="/windows/desktop/api/winioctl/ns-winioctl-usn_record_v2">USN_RECORD_V2</a> structure (also called 
    <b>USN_RECORD</b> structure).

## -struct-fields

### -field RecordLength

The total length of a record, in bytes.

Because <b>USN_RECORD_V3</b> is a variable size, the 
       <b>RecordLength</b> member should be used when calculating the address of the next record 
       in an output buffer, for example,  a buffer that is returned from operations for the 
       <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function that work with 
       <b>USN_RECORD_V3</b>.

The size in bytes of any change 
       journal record is at most the size of the <b>USN_RECORD_V3</b> 
       structure, plus <i>MaximumComponentLength</i> characters minus 1 (for the character declared 
       in the structure) times the size of a wide character. The value of 
       <i>MaximumComponentLength</i> may be determined by calling the  
       <a href="/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa">GetVolumeInformation</a> function. In C, you can 
       determine a record size by using the following code example.

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>  MaximumChangeJournalRecordSize = 
      QuadAlign( (MaximumComponentLength - 1) * sizeof(WCHAR) 
       + sizeof(USN_RECORD_V3) );
</pre>
</td>
</tr>
</table></span></div>
To maintain compatibility across version changes of the change journal software, use a run-time calculation 
       to determine the size of the <b>USN_RECORD_V3</b> structure. For 
       more information about compatibility across version changes, see the Remarks section in this topic.

### -field MajorVersion

The major version number of the change journal software for this record.

For example, if the change journal software is version 3.0, the major version number is 3.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The structure is a <a href="/windows/desktop/api/winioctl/ns-winioctl-usn_record_v2">USN_RECORD_V2</a> structure and the 
        remainder of the structure should be parsed using that layout.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The structure is a <b>USN_RECORD_V3</b> structure and the 
        remainder of the structure should be parsed using that layout.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The structure is a [USN_RECORD_V4 structure](ns-winioctl-usn_record_v4.md) and the remainder of the structure should be parsed using that layout.

</td>
</tr>
</table>

### -field MinorVersion

The minor version number of the change journal software for this record. For example, if the change journal 
      software is version 3.0, the minor version number is zero.

### -field FileReferenceNumber

The 128-bit ordinal number of the file or directory for which this record notes changes.

This is an arbitrarily assigned value that associates a journal record with a file.

### -field ParentFileReferenceNumber

The 128-bit ordinal number of the directory where the file or directory that is associated with this record 
       is located.

This is an arbitrarily assigned value that associates a journal record with a parent directory.

### -field Usn

The USN of this record.

### -field TimeStamp

The standard UTC time stamp (<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>) of this 
      record, in 64-bit format.

### -field Reason

The flags that identify reasons for changes that have accumulated in this file or directory journal record 
       since the file or directory opened.

When a file or directory closes, then a final USN record is generated with the 
       <b>USN_REASON_CLOSE</b> flag set. The next change (for example, after the next open 
       operation or deletion) starts a new record with a new set of reason flags.

A rename or move operation generates two USN records, one that records the old parent directory for the item, 
       and one that records a new parent.

The following  table identifies the possible flags.

<div class="alert"><b>Note</b>  Unused bits are reserved.</div>
<div> </div>
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
A user has either changed one or more file or directory attributes (for example,  the read-only, hidden, 
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
The file or directory is extended (added to).

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_DATA_OVERWRITE"></a><a id="usn_reason_data_overwrite"></a><dl>
<dt><b>USN_REASON_DATA_OVERWRITE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The data in the file or directory is overwritten.

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
The user made a change to the extended attributes of a file or directory.

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
An NTFS file system hard link is added to or removed from the file or directory.

An NTFS file system hard link, similar to a POSIX hard link, is one of several directory entries that see 
         the same file or directory.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_INDEXABLE_CHANGE"></a><a id="usn_reason_indexable_change"></a><dl>
<dt><b>USN_REASON_INDEXABLE_CHANGE</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
A user changes the <b>FILE_ATTRIBUTE_NOT_CONTENT_INDEXED</b> attribute.

That is, the user changes the file or directory from one where content can be indexed to one where content 
         cannot be indexed, or vice versa. Content indexing permits rapid searching of data by building a database of 
         selected content.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_INTEGRITY_CHANGE"></a><a id="usn_reason_integrity_change"></a><dl>
<dt><b>USN_REASON_INTEGRITY_CHANGE</b></dt>
<dt>0x00800000</dt>
</dl>
</td>
<td width="60%">
A user changed the state of the <b>FILE_ATTRIBUTE_INTEGRITY_STREAM</b> attribute for the given stream.

On the ReFS file system, integrity streams maintain a checksum of all data for that stream, so that the contents of the file can be validated during read or write operations.


</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_NAMED_DATA_EXTEND"></a><a id="usn_reason_named_data_extend"></a><dl>
<dt><b>USN_REASON_NAMED_DATA_EXTEND</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
The one or more named data streams for a file are extended (added to).

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_NAMED_DATA_OVERWRITE"></a><a id="usn_reason_named_data_overwrite"></a><dl>
<dt><b>USN_REASON_NAMED_DATA_OVERWRITE</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
The data in one or more named data streams for a file is overwritten.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_NAMED_DATA_TRUNCATION"></a><a id="usn_reason_named_data_truncation"></a><dl>
<dt><b>USN_REASON_NAMED_DATA_TRUNCATION</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
The one or more named data streams for a file is truncated.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_OBJECT_ID_CHANGE"></a><a id="usn_reason_object_id_change"></a><dl>
<dt><b>USN_REASON_OBJECT_ID_CHANGE</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
The object identifier of a file or directory is changed.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_RENAME_NEW_NAME"></a><a id="usn_reason_rename_new_name"></a><dl>
<dt><b>USN_REASON_RENAME_NEW_NAME</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
A file or directory is renamed, and the file name in the 
        <b>USN_RECORD_V3</b> structure is the new name.

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
        <b>USN_RECORD_V3</b> structure is the previous name.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_REPARSE_POINT_CHANGE"></a><a id="usn_reason_reparse_point_change"></a><dl>
<dt><b>USN_REASON_REPARSE_POINT_CHANGE</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
The reparse point that is contained in a file or directory is changed, or a reparse point is added to or 
        deleted from a file or directory.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_SECURITY_CHANGE"></a><a id="usn_reason_security_change"></a><dl>
<dt><b>USN_REASON_SECURITY_CHANGE</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
A change is made in the access rights to a file or directory.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_STREAM_CHANGE"></a><a id="usn_reason_stream_change"></a><dl>
<dt><b>USN_REASON_STREAM_CHANGE</b></dt>
<dt>0x00200000</dt>
</dl>
</td>
<td width="60%">
A named stream is added to or removed from a file, or a named stream is renamed.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_REASON_TRANSACTED_CHANGE"></a><a id="usn_reason_transacted_change"></a><dl>
<dt><b>USN_REASON_TRANSACTED_CHANGE</b></dt>
<dt>0x00400000 </dt>
</dl>
</td>
<td width="60%">
The given stream is modified through a TxF transaction.  

</td>
</tr>
</table>

### -field SourceInfo

Additional information about the source of the change, set by the 
       <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_mark_handle">FSCTL_MARK_HANDLE</a> of the 
       <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> operation.

When a thread writes a new USN record, the source information flags in the prior record continues to be 
       present only if the thread also sets those flags.  Therefore, the source information structure allows 
       applications to filter out USN records that are set only by a known source, for example, an antivirus filter.

One of the two following values can be set. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="USN_SOURCE_AUXILIARY_DATA"></a><a id="usn_source_auxiliary_data"></a><dl>
<dt><b>USN_SOURCE_AUXILIARY_DATA</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The operation adds a private data stream to a file or directory.

An example might be a virus detector adding checksum information. As the virus detector modifies the item, 
         the system generates USN records. <b>USN_SOURCE_AUXILIARY_DATA</b> indicates that the 
         modifications did not change the application data.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_SOURCE_DATA_MANAGEMENT"></a><a id="usn_source_data_management"></a><dl>
<dt><b>USN_SOURCE_DATA_MANAGEMENT</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The operation provides information about a change to the file or directory made by the operating system.

A typical use is when the Remote Storage system moves data from external to local storage. Remote Storage 
         is the hierarchical storage management software. Such a move usually at a minimum adds the 
         <b>USN_REASON_DATA_OVERWRITE</b> flag to a USN record. However, the data has not changed 
         from the user's point of view. By noting <b>USN_SOURCE_DATA_MANAGEMENT</b> in the 
         <b>SourceInfo</b> member, you can determine that although a write operation is performed 
         on the item, data has not changed.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_SOURCE_REPLICATION_MANAGEMENT"></a><a id="usn_source_replication_management"></a><dl>
<dt><b>USN_SOURCE_REPLICATION_MANAGEMENT</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The operation is modifying a file to match the contents of the same file which exists in another member 
        of the replica set.

</td>
</tr>
<tr>
<td width="40%"><a id="USN_SOURCE_CLIENT_REPLICATION_MANAGEMENT"></a><a id="usn_source_client_replication_management"></a><dl>
<dt><b>USN_SOURCE_CLIENT_REPLICATION_MANAGEMENT</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The operation is modifying a file on client systems to match the contents of the same file that exists in the cloud. 

</td>
</tr>
</table>

### -field SecurityId

The unique security identifier assigned to the file or directory associated with this record.

### -field FileAttributes

The attributes for the file or directory associated with this record, as returned by the 
      <a href="/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa">GetFileAttributes</a> function. Attributes of streams 
      associated with the file or directory are excluded.

### -field FileNameLength

The length of the name of the file or directory associated with this record, in bytes. The 
      <b>FileName</b> member contains this name. Use this member to determine file name length, 
      rather than depending on a trailing '\0' to delimit the file name in <b>FileName</b>.

### -field FileNameOffset

The offset of the <b>FileName</b> member from the beginning of the structure.

### -field FileName

The name of the file or directory associated with this record in Unicode format. This file or directory name 
       is of variable length.

When working with <b>FileName</b>, do not count on the file name that contains a trailing 
       '\0' delimiter, but instead determine the length of the file name by using 
       <b>FileNameLength</b>.

Do not perform any compile-time pointer arithmetic using <b>FileName</b>. Instead, make 
       necessary calculations at run time by using the value of the <b>FileNameOffset</b> member. 
       Doing so helps make your code compatible with any future versions of 
       <b>USN_RECORD_V3</b>.

## -remarks

In output buffers returned from <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> 
    operations that work with <b>USN_RECORD_V3</b>, all records are 
    aligned on 64-bit boundaries from the start of the buffer.

When range tracking is turned on, NTFS switches to producing only <b>USN_RECORD_V3</b> records as output.

To provide a path for upward compatibility in change journal clients, Microsoft provides a major and minor 
    version number of the change journal software in the 
    <b>USN_RECORD_V3</b> structure. Your code should examine these 
    values, detect its own compatibility with the change journal software, and if necessary gracefully handle any 
    incompatibility.

A change in the minor version number indicates that the existing 
    <b>USN_RECORD_V3</b> structure members are still valid, but that new 
    members may have been added between the penultimate member and the last, which is a variable-length string.

To handle such a change gracefully, your code should not do any compile-time pointer arithmetic that relies on 
    the location of the last member. For example, this makes the C code 
    <code>sizeof(USN_RECORD)</code> unreliable. Instead, rely on run-time calculations by 
    using the <b>RecordLength</b> member.

An increase in the major version number of the change journal software indicates that the 
    <b>USN_RECORD_V3</b> structure may have undergone major changes, and 
    that the current definition may not be reliable. If your code detects a change in the major version number of the 
    change journal software, it should not work with the change journal.

For more information, see 
    <a href="/windows/desktop/FileIO/creating-modifying-and-deleting-a-change-journal">Creating, Modifying, and Deleting a Change Journal</a>.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_mark_handle">FSCTL_MARK_HANDLE</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_read_usn_journal">FSCTL_READ_USN_JOURNAL</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa">GetFileAttributes</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa">GetVolumeInformation</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-read_usn_journal_data_v0">READ_USN_JOURNAL_DATA</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-usn_record_v2">USN_RECORD_V2</a>



[USN_RECORD_V4 structure](ns-winioctl-usn_record_v4.md)



<a href="/windows/desktop/FileIO/volume-management-structures">Volume Management Structures</a>

