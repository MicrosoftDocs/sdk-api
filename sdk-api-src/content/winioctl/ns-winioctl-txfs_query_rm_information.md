---
UID: NS:winioctl._TXFS_QUERY_RM_INFORMATION
title: TXFS_QUERY_RM_INFORMATION
description: Contains information about the resource manager (RM).
helpviewer_keywords: ["*PTXFS_QUERY_RM_INFORMATION","PTXFS_QUERY_RM_INFORMATION","PTXFS_QUERY_RM_INFORMATION structure pointer [Files]","TXFS_LOGGING_MODE_FULL","TXFS_LOGGING_MODE_SIMPLE","TXFS_QUERY_RM_INFORMATION","TXFS_QUERY_RM_INFORMATION structure [Files]","TXFS_RM_FLAG_DO_NOT_RESET_RM_AT_NEXT_START","TXFS_RM_FLAG_LOG_CONTAINER_COUNT_MIN","TXFS_RM_FLAG_LOG_GROWTH_INCREMENT_NUM_CONTAINERS","TXFS_RM_FLAG_LOG_GROWTH_INCREMENT_PERCENT","TXFS_RM_FLAG_LOG_NO_CONTAINER_COUNT_MAX","TXFS_RM_FLAG_PREFER_AVAILABILITY","TXFS_RM_FLAG_PREFER_CONSISTENCY","TXFS_RM_FLAG_RESET_RM_AT_NEXT_START","TXFS_RM_STATE_ACTIVE","TXFS_RM_STATE_NOT_STARTED","TXFS_RM_STATE_SHUTTING_DOWN","TXFS_RM_STATE_STARTING","base.txfs_query_rm_information","fs.txfs_query_rm_information","winioctl/PTXFS_QUERY_RM_INFORMATION","winioctl/TXFS_QUERY_RM_INFORMATION"]
old-location: fs\txfs_query_rm_information.htm
tech.root: fs
ms.assetid: a8dc6b69-306a-4843-b7b5-ea6a1e5068cb
ms.date: 12/05/2018
ms.keywords: '*PTXFS_QUERY_RM_INFORMATION, PTXFS_QUERY_RM_INFORMATION, PTXFS_QUERY_RM_INFORMATION structure pointer [Files], TXFS_LOGGING_MODE_FULL, TXFS_LOGGING_MODE_SIMPLE, TXFS_QUERY_RM_INFORMATION, TXFS_QUERY_RM_INFORMATION structure [Files], TXFS_RM_FLAG_DO_NOT_RESET_RM_AT_NEXT_START, TXFS_RM_FLAG_LOG_CONTAINER_COUNT_MIN, TXFS_RM_FLAG_LOG_GROWTH_INCREMENT_NUM_CONTAINERS, TXFS_RM_FLAG_LOG_GROWTH_INCREMENT_PERCENT, TXFS_RM_FLAG_LOG_NO_CONTAINER_COUNT_MAX, TXFS_RM_FLAG_PREFER_AVAILABILITY, TXFS_RM_FLAG_PREFER_CONSISTENCY, TXFS_RM_FLAG_RESET_RM_AT_NEXT_START, TXFS_RM_STATE_ACTIVE, TXFS_RM_STATE_NOT_STARTED, TXFS_RM_STATE_SHUTTING_DOWN, TXFS_RM_STATE_STARTING, base.txfs_query_rm_information, fs.txfs_query_rm_information, winioctl/PTXFS_QUERY_RM_INFORMATION, winioctl/TXFS_QUERY_RM_INFORMATION'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
targetos: Windows
req.typenames: TXFS_QUERY_RM_INFORMATION, *PTXFS_QUERY_RM_INFORMATION
req.redist: 
f1_keywords:
 - _TXFS_QUERY_RM_INFORMATION
 - winioctl/_TXFS_QUERY_RM_INFORMATION
 - PTXFS_QUERY_RM_INFORMATION
 - winioctl/PTXFS_QUERY_RM_INFORMATION
 - TXFS_QUERY_RM_INFORMATION
 - winioctl/TXFS_QUERY_RM_INFORMATION
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
 - TXFS_QUERY_RM_INFORMATION
---

# TXFS_QUERY_RM_INFORMATION structure


## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Contains information about the resource manager (RM).

## -struct-fields

### -field BytesRequired

If <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_txfs_query_rm_information">FSCTL_TXFS_QUERY_RM_INFORMATION</a> 
      returns <b>ERROR_BUFFER_TOO_SMALL</b>, this member specifies the minimum number of bytes 
      needed to return the information requested, including the <b>NULL</b> terminating 
      character.

### -field TailLsn

The oldest log sequence number (LSN) currently used by the RM.

### -field CurrentLsn

The LSN most recently used by the RM in its log.

### -field ArchiveTailLsn

The LSN of the archive tail of the log.

### -field LogContainerSize

The actual size of a log container, in bytes.

### -field HighestVirtualClock

The highest timestamp associated with a log record.

### -field LogContainerCount

The number of log containers.

### -field LogContainerCountMax

The maximum number of log containers.

### -field LogContainerCountMin

The minimum number of containers allowed in the log.

### -field LogGrowthIncrement

The amount the log will grow by, which is either a number of containers or percentage of the log size; the 
      growth type used is specified by the flags set in <b>Flags</b> member.

### -field LogAutoShrinkPercentage

If the auto-shrink policy is active, this member specifies the maximum allowable amount of free space in 
      the log. If this member is zero, the auto-shrink policy is not active.

### -field Flags

This member can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TXFS_RM_FLAG_LOG_CONTAINER_COUNT_MIN"></a><a id="txfs_rm_flag_log_container_count_min"></a><dl>
<dt><b>TXFS_RM_FLAG_LOG_CONTAINER_COUNT_MIN</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
If the flag is set, the RM's log is allowed to shrink as far as possible. This flag is mutually exclusive 
        with <b>TXFS_RM_FLAG_LOG_NO_CONTAINER_COUNT_MAX</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_RM_FLAG_LOG_GROWTH_INCREMENT_NUM_CONTAINERS"></a><a id="txfs_rm_flag_log_growth_increment_num_containers"></a><dl>
<dt><b>TXFS_RM_FLAG_LOG_GROWTH_INCREMENT_NUM_CONTAINERS</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Indicates the type of value in <b>LogGrowthIncrement</b>. If this flag is set, 
        <b>LogGrowthIncrement</b> is a number of containers. This flag is mutually exclusive with 
        <b>TXFS_RM_FLAG_LOG_GROWTH_INCREMENT_PERCENT</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_RM_FLAG_LOG_GROWTH_INCREMENT_PERCENT"></a><a id="txfs_rm_flag_log_growth_increment_percent"></a><dl>
<dt><b>TXFS_RM_FLAG_LOG_GROWTH_INCREMENT_PERCENT</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Indicates the type of value in <b>LogGrowthIncrement</b>. If this flag is set, 
        <b>LogGrowthIncrement</b> is a percentage. This flag is mutually exclusive with 
        <b>TXFS_RM_FLAG_LOG_GROWTH_INCREMENT_NUM_CONTAINERS</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_RM_FLAG_LOG_NO_CONTAINER_COUNT_MAX"></a><a id="txfs_rm_flag_log_no_container_count_max"></a><dl>
<dt><b>TXFS_RM_FLAG_LOG_NO_CONTAINER_COUNT_MAX</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Indicates that the RM's log can grow without bounds. This flag is mutually exclusive with 
        <b>TXFS_RM_FLAG_LOG_NO_CONTAINER_COUNT_MIN</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_RM_FLAG_RESET_RM_AT_NEXT_START"></a><a id="txfs_rm_flag_reset_rm_at_next_start"></a><dl>
<dt><b>TXFS_RM_FLAG_RESET_RM_AT_NEXT_START</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
Indicates the current state of the RM reset flag. If this is set, the RM will reset itself the next time 
        it is started. This flag is only valid for default RMs, not secondary RMs. This flag is mutually exclusive 
        with <b>TXFS_RM_FLAG_DO_NOT_RESET_RM_AT_NEXT_START</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_RM_FLAG_DO_NOT_RESET_RM_AT_NEXT_START"></a><a id="txfs_rm_flag_do_not_reset_rm_at_next_start"></a><dl>
<dt><b>TXFS_RM_FLAG_DO_NOT_RESET_RM_AT_NEXT_START</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
Indicates the current state of the RM reset flag. If this is set, the RM will not reset itself the next 
        time it is started. This flag is only valid for default RMs, not secondary RMs. This flag is mutually 
        exclusive with <b>TXFS_RM_FLAG_RESET_RM_AT_NEXT_START</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_RM_FLAG_PREFER_CONSISTENCY"></a><a id="txfs_rm_flag_prefer_consistency"></a><dl>
<dt><b>TXFS_RM_FLAG_PREFER_CONSISTENCY</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
Indicates that the RM is to prefer transaction 
        <a href="/windows/win32/fileio/glossary">consistency</a> over system 
        <a href="/windows/win32/fileio/glossary">availability</a>. This flag is mutually 
        exclusive with <b>TXFS_RM_FLAG_PREFER_AVAILABILITY</b> and is not supported by the default 
        RM on the system volume.

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_RM_FLAG_PREFER_AVAILABILITY"></a><a id="txfs_rm_flag_prefer_availability"></a><dl>
<dt><b>TXFS_RM_FLAG_PREFER_AVAILABILITY</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
Indicates that the RM is to prefer system 
        <a href="/windows/win32/fileio/glossary">availability</a> over transaction 
        <a href="/windows/win32/fileio/glossary">consistency</a>. This flag is mutually 
        exclusive with <b>TXFS_RM_FLAG_PREFER_CONSISTENCY</b> and is forced by the default RM on 
        the system volume.

</td>
</tr>
</table>

### -field LoggingMode

The current logging mode.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TXFS_LOGGING_MODE_SIMPLE"></a><a id="txfs_logging_mode_simple"></a><dl>
<dt><b>TXFS_LOGGING_MODE_SIMPLE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Simple logging is used.

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_LOGGING_MODE_FULL"></a><a id="txfs_logging_mode_full"></a><dl>
<dt><b>TXFS_LOGGING_MODE_FULL</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Full logging is used

</td>
</tr>
</table>

### -field Reserved

Reserved.

### -field RmState

The state of the RM. Valid values are as follows.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TXFS_RM_STATE_NOT_STARTED"></a><a id="txfs_rm_state_not_started"></a><dl>
<dt><b>TXFS_RM_STATE_NOT_STARTED</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The RM is not yet started.

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_RM_STATE_STARTING"></a><a id="txfs_rm_state_starting"></a><dl>
<dt><b>TXFS_RM_STATE_STARTING</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The RM is starting.

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_RM_STATE_ACTIVE"></a><a id="txfs_rm_state_active"></a><dl>
<dt><b>TXFS_RM_STATE_ACTIVE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The RM is active and ready to accept transactions.

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_RM_STATE_SHUTTING_DOWN"></a><a id="txfs_rm_state_shutting_down"></a><dl>
<dt><b>TXFS_RM_STATE_SHUTTING_DOWN</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The RM is shutting down.

</td>
</tr>
</table>

### -field LogCapacity

The total capacity of the log, in bytes.

### -field LogFree

The number of bytes free in the log.

### -field TopsSize

The size of the $Tops file, in bytes.

### -field TopsUsed

The amount of the $Tops file that is in use, in bytes.

### -field TransactionCount

The number of active transactions, at the time the query was issued.

### -field OnePCCount

The number of single-phase commit operations that have occurred on this RM.

### -field TwoPCCount

The number of two-phase commit operations that have occurred on this RM.

### -field NumberLogFileFull

The number of times this RM's log has become full.

### -field OldestTransactionAge

The length of the oldest active transaction, in milliseconds.

### -field RMName

The <b>GUID</b> that indicates the name of this RM.

### -field TmLogPathOffset

The offset from the beginning of this structure to a <b>NULL</b>-terminated Unicode 
      string that contains the path to the TM's log.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_txfs_query_rm_information">FSCTL_TXFS_QUERY_RM_INFORMATION</a>



<a href="/windows/desktop/FileIO/transactional-ntfs-structures">TxF Structures</a>