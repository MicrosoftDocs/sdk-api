---
UID: NS:winioctl._MARK_HANDLE_INFO
title: MARK_HANDLE_INFO
description: Contains information that is used to mark a specified file or directory, and its update sequence number (USN) change journal record with data about changes.
helpviewer_keywords: ["*PMARK_HANDLE_INFO","MARK_HANDLE_INFO","MARK_HANDLE_INFO structure [Files]","MARK_HANDLE_NOT_READ_COPY","MARK_HANDLE_NOT_REALTIME","MARK_HANDLE_NOT_TXF_SYSTEM_LOG","MARK_HANDLE_PROTECT_CLUSTERS","MARK_HANDLE_READ_COPY","MARK_HANDLE_REALTIME","MARK_HANDLE_TXF_SYSTEM_LOG","PMARK_HANDLE_INFO","PMARK_HANDLE_INFO structure pointer [Files]","USN_SOURCE_AUXILIARY_DATA","USN_SOURCE_DATA_MANAGEMENT","USN_SOURCE_REPLICATION_MANAGEMENT","_win32_mark_handle_info_str","base.mark_handle_info_str","fs.mark_handle_info_str","winioctl/MARK_HANDLE_INFO","winioctl/PMARK_HANDLE_INFO"]
old-location: fs\mark_handle_info_str.htm
tech.root: fs
ms.assetid: 6f736b31-279d-4118-a5e3-ad3c2bea2250
ms.date: 12/05/2018
ms.keywords: '*PMARK_HANDLE_INFO, MARK_HANDLE_INFO, MARK_HANDLE_INFO structure [Files], MARK_HANDLE_NOT_READ_COPY, MARK_HANDLE_NOT_REALTIME, MARK_HANDLE_NOT_TXF_SYSTEM_LOG, MARK_HANDLE_PROTECT_CLUSTERS, MARK_HANDLE_READ_COPY, MARK_HANDLE_REALTIME, MARK_HANDLE_TXF_SYSTEM_LOG, PMARK_HANDLE_INFO, PMARK_HANDLE_INFO structure pointer [Files], USN_SOURCE_AUXILIARY_DATA, USN_SOURCE_DATA_MANAGEMENT, USN_SOURCE_REPLICATION_MANAGEMENT, _win32_mark_handle_info_str, base.mark_handle_info_str, fs.mark_handle_info_str, winioctl/MARK_HANDLE_INFO, winioctl/PMARK_HANDLE_INFO'
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
req.typenames: MARK_HANDLE_INFO, *PMARK_HANDLE_INFO
req.redist: 
f1_keywords:
 - PMARK_HANDLE_INFO
 - winioctl/PMARK_HANDLE_INFO
 - MARK_HANDLE_INFO
 - winioctl/MARK_HANDLE_INFO
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
 - MARK_HANDLE_INFO
---

# MARK_HANDLE_INFO structure


## -description

Contains information that is used to mark a specified file or directory, and its update sequence 
    number (USN) change journal record with data about changes. It is used by the 
    <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_mark_handle">FSCTL_MARK_HANDLE</a> control code.

## -struct-fields

### -field DUMMYUNIONNAME

### -field UsnSourceInfo

The type of changes being made.

The operation does not modify the file or directory externally from the point of view of the application that 
       created it.

When a thread writes a new USN record, the source information flags in the prior record continues to be 
       present only if the thread also sets those flags. Therefore, the source information structure allows 
       applications to filter out USN records that are set only by a known source, such as an antivirus filter.

The following values are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="USN_SOURCE_DATA_MANAGEMENT"></a><a id="usn_source_data_management"></a><dl>
<dt><b>USN_SOURCE_DATA_MANAGEMENT</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The operation provides information about a change to the file or directory made by the operating system.

A typical use is when Remote Storage moves data from external to local storage. Remote Storage is the 
         hierarchical storage management software. Such a move usually at a minimum adds the 
         <b>USN_REASON_DATA_OVERWRITE</b> flag to a USN record. However, the data has not changed 
         from the user point of view. By noting <b>USN_SOURCE_DATA_MANAGEMENT</b> in the 
         <b>SourceInfo</b> member of the 
         <a href="/windows/desktop/api/winioctl/ns-winioctl-usn_record_v2">USN_RECORD</a> structure that holds the record, you can 
         determine that although a write operation is performed on the item, data has not changed.

</td>
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
<td width="40%"><a id="USN_SOURCE_REPLICATION_MANAGEMENT"></a><a id="usn_source_replication_management"></a><dl>
<dt><b>USN_SOURCE_REPLICATION_MANAGEMENT</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The operation creates or updates the contents of a replicated file.

For example, the file replication service sets this flag when it creates or updates a file in a replicated 
         directory.

</td>
</tr>

</td>
</tr>

<tr>
<td width="40%"><a id="USN_SOURCE_CLIENT_REPLICATION_MANAGEMENT "></a><a id="usn_source_client_replication_management"></a><dl>
<dt><b>USN_SOURCE_CLIENT_REPLICATION_MANAGEMENT</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Replication is being performed on client systems either from the cloud or servers.
</td>
</tr>

</table>

### -field CopyNumber

The zero-based copy number to use for subsequent reads. This is for use on Storage Spaces and Streams on 
        NTFS and ReFS and non-integrity streams on ReFS (streams with integrity on ReFS handle this automatically.)

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This member is not supported before Windows 8 and Windows Server 2012.

### -field VolumeHandle

The volume handle to the volume where the file or directory resides. For more information on obtaining a 
       volume handle, see the Remarks section.

This handle is required to check the privileges for this operation.

The caller must have the <b>SE_MANAGE_VOLUME_NAME</b> privilege. For more information, see 
       <a href="/windows/desktop/SecAuthZ/privileges">Privileges</a>.

### -field HandleInfo

The flag that specifies additional information about the file or directory identified by the handle value 
      in the <b>VolumeHandle</b> member.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MARK_HANDLE_PROTECT_CLUSTERS"></a><a id="mark_handle_protect_clusters"></a><dl>
<dt><b>MARK_HANDLE_PROTECT_CLUSTERS</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The file is marked as unable to be defragmented until the handle is closed.

Once a handle marked <b>MARK_HANDLE_PROTECT_CLUSTERS</b> is closed, there is no guarantee that the file's clusters won't move.

</td>
</tr>
<tr>
<td width="40%"><a id="MARK_HANDLE_TXF_SYSTEM_LOG"></a><a id="mark_handle_txf_system_log"></a><dl>
<dt><b>MARK_HANDLE_TXF_SYSTEM_LOG</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The file is marked as unable to be defragmented until the handle is closed.

<b>Windows Server 2003:  </b>This flag is not supported until Windows Server 2003 with SP1.

<b>Windows XP:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="MARK_HANDLE_NOT_TXF_SYSTEM_LOG"></a><a id="mark_handle_not_txf_system_log"></a><dl>
<dt><b>MARK_HANDLE_NOT_TXF_SYSTEM_LOG</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The file is marked as unable to be defragmented until the handle is closed.

<b>Windows Server 2003:  </b>This flag is not supported until Windows Server 2003 with SP1.

<b>Windows XP:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="MARK_HANDLE_REALTIME"></a><a id="mark_handle_realtime"></a><dl>
<dt><b>MARK_HANDLE_REALTIME</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
The file is marked for real-time read behavior regardless of the actual file type. Files marked with this 
         flag must be opened for <a href="/windows/desktop/FileIO/file-buffering">unbuffered I/O</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="MARK_HANDLE_NOT_REALTIME"></a><a id="mark_handle_not_realtime"></a><dl>
<dt><b>MARK_HANDLE_NOT_REALTIME</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
The file previously marked for real-time read behavior using the 
         <b>MARK_HANDLE_REALTIME</b> flag can be unmarked using this flag, removing the real-time 
         behavior. Files marked with this flag must be opened for 
         <a href="/windows/desktop/FileIO/file-buffering">unbuffered I/O</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="MARK_HANDLE_READ_COPY"></a><a id="mark_handle_read_copy"></a><dl>
<dt><b>MARK_HANDLE_READ_COPY</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Indicates the copy number specified in the <b>CopyNumber</b> member should be used 
         for reads. Files marked with this flag must be opened for 
         <a href="/windows/desktop/FileIO/file-buffering">unbuffered I/O</a>.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This flag is not supported until Windows 8 and Windows Server 2012.

</td>
</tr>
<tr>
<td width="40%"><a id="MARK_HANDLE_NOT_READ_COPY"></a><a id="mark_handle_not_read_copy"></a><dl>
<dt><b>MARK_HANDLE_NOT_READ_COPY</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
The file previously marked for read-copy behavior using the 
        <b>MARK_HANDLE_READ_COPY</b> flag can be unmarked using this flag, removing the read-copy 
        behavior. Files marked with this flag must be opened for 
        <a href="/windows/desktop/FileIO/file-buffering">unbuffered I/O</a>.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This flag is not supported until Windows 8 and Windows Server 2012.
</td>
</tr>

</td>
</tr>
<tr>
<td width="40%"><a id="MARK_HANDLE_RETURN_PURGE_FAILURE"></a><a id="mark_handle_return_purge_failure"></a><dl>
<dt><b>MARK_HANDLE_RETURN_PURGE_FAILURE</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
When intermixing memory mapped/cached IO with non-cached IO the system attempts, when a non-cached io is issued, 
  to purge memory mappings for the range of the non-cached IO.  If these purges fail 
  the system normally does not return the failure to the caller which can lead to corrupted state 
  (which is why the documentation says to not do this). This flag tells the system to return purge failures 
  for the given handle so the application can better handle this situation


This flag is not supported until Windows 8 and Windows Server 2012.

</td>
</tr>

</td>
</tr>
<tr>
<td width="40%"><a id="MARK_HANDLE_DISABLE_FILE_METADATA_OPTIMIZATION"></a><a id="mark_handle_disable_file_metadata_optimization"></a><dl>
<dt><b>MARK_HANDLE_DISABLE_FILE_METADATA_OPTIMIZATION </b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
A highly fragmented file in NTFS uses multiple MFT records to describe all of the extents for a file. This 
list of child MFT records (also known as FRS records) are controlled by a structure known as an attribute list. An 
attribute list is limited to 128K in size. When the size of an attribute list hits a certain threshold NTFS will 
trigger a background compaction on the extents so the minimum number of child FRS records will be used. 
This flag disables this FRS compaction feature for the given file.

This flag is not supported until Windows 10.

</td>
</tr>

</td>
</tr>
<tr>
<td width="40%"><a id="MARK_HANDLE_ENABLE_USN_SOURCE_ON_PAGING_IO      "></a><a id="mark_handle_enable_usn_source_on_paging_io"></a><dl>
<dt><b>MARK_HANDLE_ENABLE_USN_SOURCE_ON_PAGING_IO      </b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
Tells NTFS to set the given UsnSourceInfo value on Paging writes in the USN Journal. Traditionally this was not
done on paging writes since the system did not know what thread made the given changes. This is an override. This only works if the FileObject the memory manager is 
using has this state associated with it.


This flag is not supported until Windows 10.

</td>
</tr>

</td>
</tr>
<tr>
<td width="40%"><a id="MARK_HANDLE_SKIP_COHERENCY_SYNC_DISALLOW_WRITES"></a><a id="mark_handle_skip_coherency_sync_disallow_writes"></a><dl>
<dt><b>MARK_HANDLE_SKIP_COHERENCY_SYNC_DISALLOW_WRITES</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
Setting this flag tells the system that writes are not allowed on this file.  If an application tries 
to open the file for write access, the operation is failed with STATUS_ACCESS_DENIED. 
If a write is seen the operation is failed with STATUS_MARKED_TO_DISALLOW_WRITES


This flag is not supported until Windows 10.
</td>
</tr>
</table>

## -remarks

To retrieve a handle to a volume, call 
     <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> with the 
     <i>lpFileName</i> parameter set to a string in the following form:

"&#92;&#92;.&#92;<i>X</i>:"

In the preceding string, <i>X</i> is the letter identifying the drive on which the volume 
     appears.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_mark_handle">FSCTL_MARK_HANDLE</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-usn_record_v2">USN_RECORD</a>

