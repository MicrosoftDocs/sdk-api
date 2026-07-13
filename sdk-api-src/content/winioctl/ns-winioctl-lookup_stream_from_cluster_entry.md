---
UID: NS:winioctl._LOOKUP_STREAM_FROM_CLUSTER_ENTRY
title: LOOKUP_STREAM_FROM_CLUSTER_ENTRY
description: Returned from the FSCTL_LOOKUP_STREAM_FROM_CLUSTER control code.
helpviewer_keywords: ["*PLOOKUP_STREAM_FROM_CLUSTER_ENTRY","LOOKUP_STREAM_FROM_CLUSTER_ENTRY","LOOKUP_STREAM_FROM_CLUSTER_ENTRY structure [Files]","LOOKUP_STREAM_FROM_CLUSTER_ENTRY_ATTRIBUTE_DATA","LOOKUP_STREAM_FROM_CLUSTER_ENTRY_ATTRIBUTE_INDEX","LOOKUP_STREAM_FROM_CLUSTER_ENTRY_ATTRIBUTE_MASK","LOOKUP_STREAM_FROM_CLUSTER_ENTRY_ATTRIBUTE_SYSTEM","LOOKUP_STREAM_FROM_CLUSTER_ENTRY_FLAG_DENY_DEFRAG_SET","LOOKUP_STREAM_FROM_CLUSTER_ENTRY_FLAG_FS_SYSTEM_FILE","LOOKUP_STREAM_FROM_CLUSTER_ENTRY_FLAG_PAGE_FILE","LOOKUP_STREAM_FROM_CLUSTER_ENTRY_FLAG_TXF_SYSTEM_FILE","PLOOKUP_STREAM_FROM_CLUSTER_ENTRY","PLOOKUP_STREAM_FROM_CLUSTER_ENTRY structure pointer [Files]","fs.lookup_stream_from_cluster_entry","winioctl/LOOKUP_STREAM_FROM_CLUSTER_ENTRY","winioctl/PLOOKUP_STREAM_FROM_CLUSTER_ENTRY"]
old-location: fs\lookup_stream_from_cluster_entry.htm
tech.root: fs
ms.assetid: 2f4de631-8bb4-4b2a-a750-43f06554b22f
ms.date: 12/05/2018
ms.keywords: '*PLOOKUP_STREAM_FROM_CLUSTER_ENTRY, LOOKUP_STREAM_FROM_CLUSTER_ENTRY, LOOKUP_STREAM_FROM_CLUSTER_ENTRY structure [Files], LOOKUP_STREAM_FROM_CLUSTER_ENTRY_ATTRIBUTE_DATA, LOOKUP_STREAM_FROM_CLUSTER_ENTRY_ATTRIBUTE_INDEX, LOOKUP_STREAM_FROM_CLUSTER_ENTRY_ATTRIBUTE_MASK, LOOKUP_STREAM_FROM_CLUSTER_ENTRY_ATTRIBUTE_SYSTEM, LOOKUP_STREAM_FROM_CLUSTER_ENTRY_FLAG_DENY_DEFRAG_SET, LOOKUP_STREAM_FROM_CLUSTER_ENTRY_FLAG_FS_SYSTEM_FILE, LOOKUP_STREAM_FROM_CLUSTER_ENTRY_FLAG_PAGE_FILE, LOOKUP_STREAM_FROM_CLUSTER_ENTRY_FLAG_TXF_SYSTEM_FILE, PLOOKUP_STREAM_FROM_CLUSTER_ENTRY, PLOOKUP_STREAM_FROM_CLUSTER_ENTRY structure pointer [Files], fs.lookup_stream_from_cluster_entry, winioctl/LOOKUP_STREAM_FROM_CLUSTER_ENTRY, winioctl/PLOOKUP_STREAM_FROM_CLUSTER_ENTRY'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: LOOKUP_STREAM_FROM_CLUSTER_ENTRY, *PLOOKUP_STREAM_FROM_CLUSTER_ENTRY
req.redist: 
f1_keywords:
 - _LOOKUP_STREAM_FROM_CLUSTER_ENTRY
 - winioctl/_LOOKUP_STREAM_FROM_CLUSTER_ENTRY
 - PLOOKUP_STREAM_FROM_CLUSTER_ENTRY
 - winioctl/PLOOKUP_STREAM_FROM_CLUSTER_ENTRY
 - LOOKUP_STREAM_FROM_CLUSTER_ENTRY
 - winioctl/LOOKUP_STREAM_FROM_CLUSTER_ENTRY
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
 - LOOKUP_STREAM_FROM_CLUSTER_ENTRY
---

# LOOKUP_STREAM_FROM_CLUSTER_ENTRY structure


## -description

Returned from the 
    <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_lookup_stream_from_cluster">FSCTL_LOOKUP_STREAM_FROM_CLUSTER</a> control 
    code. Zero or more of these structures follow the 
    <a href="/windows/win32/api/winioctl/ns-winioctl-lookup_stream_from_cluster_output">LOOKUP_STREAM_FROM_CLUSTER_OUTPUT</a> 
    structure in the output buffer returned.

## -struct-fields

### -field OffsetToNext

Offset in bytes from the beginning of this structure to the next 
      <b>LOOKUP_STREAM_FROM_CLUSTER_ENTRY</b> 
      structure returned. If there are no more entries, this value is zero.

### -field Flags

Flags describing characteristics about this stream. The value will consist of one or more of these values. 
      At least one of the <b>LOOKUP_STREAM_FROM_CLUSTER_ENTRY_ATTRIBUTE_*</b> values that fall 
      within the <b>LOOKUP_STREAM_FROM_CLUSTER_ENTRY_ATTRIBUTE_MASK</b> (0xff000000) will be set; 
      one or more of the other flag values may be set.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LOOKUP_STREAM_FROM_CLUSTER_ENTRY_FLAG_PAGE_FILE"></a><a id="lookup_stream_from_cluster_entry_flag_page_file"></a><dl>
<dt><b>LOOKUP_STREAM_FROM_CLUSTER_ENTRY_FLAG_PAGE_FILE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The stream is part of the system pagefile.

</td>
</tr>
<tr>
<td width="40%"><a id="LOOKUP_STREAM_FROM_CLUSTER_ENTRY_FLAG_DENY_DEFRAG_SET"></a><a id="lookup_stream_from_cluster_entry_flag_deny_defrag_set"></a><dl>
<dt><b>LOOKUP_STREAM_FROM_CLUSTER_ENTRY_FLAG_DENY_DEFRAG_SET</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The stream is locked from defragmentation. The <b>HandleInfo</b> member of the [MARK_HANDLE_INFO structure](ns-winioctl-mark_handle_info.md) for this stream has the <b>MARK_HANDLE_PROTECT_CLUSTERS</b> flag set.

</td>
</tr>
<tr>
<td width="40%"><a id="LOOKUP_STREAM_FROM_CLUSTER_ENTRY_FLAG_FS_SYSTEM_FILE"></a><a id="lookup_stream_from_cluster_entry_flag_fs_system_file"></a><dl>
<dt><b>LOOKUP_STREAM_FROM_CLUSTER_ENTRY_FLAG_FS_SYSTEM_FILE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The stream is part of a file that is internal to the filesystem.

</td>
</tr>
<tr>
<td width="40%"><a id="LOOKUP_STREAM_FROM_CLUSTER_ENTRY_FLAG_TXF_SYSTEM_FILE"></a><a id="lookup_stream_from_cluster_entry_flag_txf_system_file"></a><dl>
<dt><b>LOOKUP_STREAM_FROM_CLUSTER_ENTRY_FLAG_TXF_SYSTEM_FILE</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The stream is part of a file that is internal to TxF.

</td>
</tr>
<tr>
<td width="40%"><a id="LOOKUP_STREAM_FROM_CLUSTER_ENTRY_ATTRIBUTE_DATA"></a><a id="lookup_stream_from_cluster_entry_attribute_data"></a><dl>
<dt><b>LOOKUP_STREAM_FROM_CLUSTER_ENTRY_ATTRIBUTE_DATA</b></dt>
<dt>0x01000000</dt>
</dl>
</td>
<td width="60%">
The stream is part of a $DATA attribute for the file (data stream).

</td>
</tr>
<tr>
<td width="40%"><a id="LOOKUP_STREAM_FROM_CLUSTER_ENTRY_ATTRIBUTE_INDEX"></a><a id="lookup_stream_from_cluster_entry_attribute_index"></a><dl>
<dt><b>LOOKUP_STREAM_FROM_CLUSTER_ENTRY_ATTRIBUTE_INDEX</b></dt>
<dt>0x02000000</dt>
</dl>
</td>
<td width="60%">
The stream is part of the $INDEX_ALLOCATION attribute for the file.

</td>
</tr>
<tr>
<td width="40%"><a id="LOOKUP_STREAM_FROM_CLUSTER_ENTRY_ATTRIBUTE_SYSTEM"></a><a id="lookup_stream_from_cluster_entry_attribute_system"></a><dl>
<dt><b>LOOKUP_STREAM_FROM_CLUSTER_ENTRY_ATTRIBUTE_SYSTEM</b></dt>
<dt>0x03000000</dt>
</dl>
</td>
<td width="60%">
The stream is part of another attribute for the file.

</td>
</tr>
</table>

### -field Reserved

This value is reserved and is currently zero.

### -field Cluster

This is the cluster that this entry refers to. It will be one of the clusters passed in the input 
      structure.

### -field FileName

A <b>NULL</b>-terminated Unicode string containing the path of the object relative to 
      the root of the volume. This string will refer to the attribute or stream represented by the cluster. This 
      string is not limited by <b>MAX_PATH</b> and may be up to 32,768 characters (65,536 bytes) in 
      length. Not all of the filenames returned can be opened; some are internal to NTFS and always opened 
      exclusively. The string returned includes the full path including filename, stream name, and attribute type name 
      in the form 
      "<i>full</i>&#92;<i>path</i>&#92;<i>to</i>&#92;<i>file</i>&#92;<i>filename.ext</i>:<i>streamname</i>:<i>typename</i>".

## -remarks

The name in the <b>FileName</b> member can be very long and in a format not recognized by 
    a customer with the stream name and attribute type name following the filename. While it's appropriate to log the 
    entire filename for diagnostic purposes, if it is to be presented to an end-user it should be reformatted to be 
    more understandable (for example, remove the attribute type name and if the <b>Flags</b> 
    member has any flag other than <b>LOOKUP_STREAM_FROM_CLUSTER_ENTRY_ATTRIBUTE_DATA</b> set then 
    an appropriate message should be displayed.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_lookup_stream_from_cluster">FSCTL_LOOKUP_STREAM_FROM_CLUSTER</a>



<a href="/windows/win32/api/winioctl/ns-winioctl-lookup_stream_from_cluster_output">LOOKUP_STREAM_FROM_CLUSTER_OUTPUT</a>



<a href="/windows/desktop/FileIO/volume-management-structures">Volume Management Structures</a>