---
UID: NS:winioctl.MARK_HANDLE_INFO
title: MARK_HANDLE_INFO
author: windows-sdk-content
description: Contains information that is used to mark a specified file or directory, and its update sequence number (USN) change journal record with data about changes.
old-location: fs\mark_handle_info_str.htm
old-project: FileIO
ms.assetid: 6f736b31-279d-4118-a5e3-ad3c2bea2250
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: "*PMARK_HANDLE_INFO, MARK_HANDLE_INFO, MARK_HANDLE_INFO structure [Files], MARK_HANDLE_NOT_READ_COPY, MARK_HANDLE_NOT_REALTIME, MARK_HANDLE_NOT_TXF_SYSTEM_LOG, MARK_HANDLE_PROTECT_CLUSTERS, MARK_HANDLE_READ_COPY, MARK_HANDLE_REALTIME, MARK_HANDLE_TXF_SYSTEM_LOG, PMARK_HANDLE_INFO, PMARK_HANDLE_INFO structure pointer [Files], USN_SOURCE_AUXILIARY_DATA, USN_SOURCE_DATA_MANAGEMENT, USN_SOURCE_REPLICATION_MANAGEMENT, _win32_mark_handle_info_str, base.mark_handle_info_str, fs.mark_handle_info_str, winioctl/MARK_HANDLE_INFO, winioctl/PMARK_HANDLE_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: MARK_HANDLE_INFO, *PMARK_HANDLE_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoCtl.h
api_name:
-	MARK_HANDLE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# MARK_HANDLE_INFO structure


## -description


Contains information that is used to mark a specified file or directory, and its update sequence 
    number (USN) change journal record with data about changes. It is used by the 
    <a href="https://msdn.microsoft.com/c96b49d8-12f3-4281-9f9f-6621769359f0">FSCTL_MARK_HANDLE</a> control code.


## -struct-fields




### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.UsnSourceInfo

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
         <a href="https://msdn.microsoft.com/1747453d-fd18-4853-a953-47131f3067ae">USN_RECORD</a> structure that holds the record, you can 
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
</table>
 


### -field DUMMYUNIONNAME.CopyNumber

The zero-based copy number to use for subsequent reads. This is for use on  on Storage Spaces and Streams on 
        NTFS and ReFS and non-integrity streams on ReFS (streams with integrity on ReFS handle this automatically.)

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This member is not supported before Windows 8 and Windows Server 2012.


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
         <a href="https://msdn.microsoft.com/1747453d-fd18-4853-a953-47131f3067ae">USN_RECORD</a> structure that holds the record, you can 
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
</table>
 


### -field VolumeHandle

The volume handle to the volume where the file or directory resides. For more information on obtaining a 
       volume handle, see the Remarks section.

This handle is required to check the privileges for this operation.

The caller must have the <b>SE_MANAGE_VOLUME_NAME</b> privilege. For more information, see 
       <a href="https://msdn.microsoft.com/library/windows/hardware/ff559863">Privileges</a>.


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
         flag must be opened for <a href="https://msdn.microsoft.com/ae1e5d0f-9b55-4aae-8402-b9c8e33d9363">unbuffered I/O</a>.

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
         <a href="https://msdn.microsoft.com/ae1e5d0f-9b55-4aae-8402-b9c8e33d9363">unbuffered I/O</a>.

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
         <a href="https://msdn.microsoft.com/ae1e5d0f-9b55-4aae-8402-b9c8e33d9363">unbuffered I/O</a>.

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
        <a href="https://msdn.microsoft.com/ae1e5d0f-9b55-4aae-8402-b9c8e33d9363">unbuffered I/O</a>.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This flag is not supported until Windows 8 and Windows Server 2012.

</td>
</tr>
</table>
 


## -remarks



To retrieve a handle to a volume, call 
     <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> with the 
     <i>lpFileName</i> parameter set to a string in the following form:

"\\.\<i>X</i>:"

In the preceding string, <i>X</i> is the letter identifying the drive on which the volume 
     appears.




## -see-also




<a href="https://msdn.microsoft.com/c96b49d8-12f3-4281-9f9f-6621769359f0">FSCTL_MARK_HANDLE</a>



<a href="https://msdn.microsoft.com/1747453d-fd18-4853-a953-47131f3067ae">USN_RECORD</a>
 

 

