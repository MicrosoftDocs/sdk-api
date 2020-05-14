---
UID: NS:winioctl._TXFS_MODIFY_RM
title: TXFS_MODIFY_RM
description: Contains the information required when modifying log parameters and logging mode for a secondary resource manager.helpviewer_keywords: ["*PTXFS_MODIFY_RM","PTXFS_MODIFY_RM","PTXFS_MODIFY_RM structure pointer [Files]","TXFS_LOGGING_MODE_FULL","TXFS_LOGGING_MODE_SIMPLE","TXFS_MODIFY_RM","TXFS_MODIFY_RM structure [Files]","TXFS_RM_FLAG_DO_NOT_RESET_RM_AT_NEXT_START","TXFS_RM_FLAG_ENFORCE_MINIMUM_SIZE","TXFS_RM_FLAG_GROW_LOG","TXFS_RM_FLAG_LOGGING_MODE","TXFS_RM_FLAG_LOG_AUTO_SHRINK_PERCENTAGE","TXFS_RM_FLAG_LOG_CONTAINER_COUNT_MAX","TXFS_RM_FLAG_LOG_CONTAINER_COUNT_MIN","TXFS_RM_FLAG_LOG_GROWTH_INCREMENT_NUM_CONTAINERS","TXFS_RM_FLAG_LOG_GROWTH_INCREMENT_PERCENT","TXFS_RM_FLAG_LOG_NO_CONTAINER_COUNT_MAX","TXFS_RM_FLAG_LOG_NO_CONTAINER_COUNT_MIN","TXFS_RM_FLAG_PREFER_AVAILABILITY","TXFS_RM_FLAG_PREFER_CONSISTENCY","TXFS_RM_FLAG_PRESERVE_CHANGES","TXFS_RM_FLAG_RENAME_RM","TXFS_RM_FLAG_RESET_RM_AT_NEXT_START","TXFS_RM_FLAG_SHRINK_LOG","base.txfs_set_rm_information","fs.txfs_modify_rm","fs.txfs_set_rm_information","winioctl/PTXFS_MODIFY_RM","winioctl/TXFS_MODIFY_RM"]
old-location: fs\txfs_modify_rm.htm
tech.root: FileIO
ms.assetid: f50d64de-4452-47ac-b2fe-a049afbd526c
ms.date: 12/05/2018
ms.keywords: '*PTXFS_MODIFY_RM, PTXFS_MODIFY_RM, PTXFS_MODIFY_RM structure pointer [Files], TXFS_LOGGING_MODE_FULL, TXFS_LOGGING_MODE_SIMPLE, TXFS_MODIFY_RM, TXFS_MODIFY_RM structure [Files], TXFS_RM_FLAG_DO_NOT_RESET_RM_AT_NEXT_START, TXFS_RM_FLAG_ENFORCE_MINIMUM_SIZE, TXFS_RM_FLAG_GROW_LOG, TXFS_RM_FLAG_LOGGING_MODE, TXFS_RM_FLAG_LOG_AUTO_SHRINK_PERCENTAGE, TXFS_RM_FLAG_LOG_CONTAINER_COUNT_MAX, TXFS_RM_FLAG_LOG_CONTAINER_COUNT_MIN, TXFS_RM_FLAG_LOG_GROWTH_INCREMENT_NUM_CONTAINERS, TXFS_RM_FLAG_LOG_GROWTH_INCREMENT_PERCENT, TXFS_RM_FLAG_LOG_NO_CONTAINER_COUNT_MAX, TXFS_RM_FLAG_LOG_NO_CONTAINER_COUNT_MIN, TXFS_RM_FLAG_PREFER_AVAILABILITY, TXFS_RM_FLAG_PREFER_CONSISTENCY, TXFS_RM_FLAG_PRESERVE_CHANGES, TXFS_RM_FLAG_RENAME_RM, TXFS_RM_FLAG_RESET_RM_AT_NEXT_START, TXFS_RM_FLAG_SHRINK_LOG, base.txfs_set_rm_information, fs.txfs_modify_rm, fs.txfs_set_rm_information, winioctl/PTXFS_MODIFY_RM, winioctl/TXFS_MODIFY_RM'
f1_keywords:
- winioctl/TXFS_MODIFY_RM
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- WinIoCtl.h
api_name:
- TXFS_MODIFY_RM
targetos: Windows
req.typenames: TXFS_MODIFY_RM, *PTXFS_MODIFY_RM
req.redist: 
---

# TXFS_MODIFY_RM structure


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://docs.microsoft.com/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Contains the information required when modifying log parameters and logging mode for a secondary 
   resource manager.


## -struct-fields




### -field Flags

The log parameters to be set.

This member can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TXFS_RM_FLAG_LOGGING_MODE"></a><a id="txfs_rm_flag_logging_mode"></a><dl>
<dt><b>TXFS_RM_FLAG_LOGGING_MODE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the <b>LoggingMode</b> member of this structure is being used. 
        If the flag is not set, the <b>LoggingMode</b> member is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_RM_FLAG_RENAME_RM"></a><a id="txfs_rm_flag_rename_rm"></a><dl>
<dt><b>TXFS_RM_FLAG_RENAME_RM</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the RM is instructed to rename itself (creating a new 
        <b>GUID</b>).

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_RM_FLAG_LOG_CONTAINER_COUNT_MAX"></a><a id="txfs_rm_flag_log_container_count_max"></a><dl>
<dt><b>TXFS_RM_FLAG_LOG_CONTAINER_COUNT_MAX</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the <b>LogContainerCountMax</b> member is being used. If the 
        flag is not set, the <b>LogContainerCountMax</b> member is ignored. This flag is mutually 
        exclusive with <b>TXFS_RM_FLAG_LOG_NO_CONTAINER_COUNT_MIN</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_RM_FLAG_LOG_CONTAINER_COUNT_MIN"></a><a id="txfs_rm_flag_log_container_count_min"></a><dl>
<dt><b>TXFS_RM_FLAG_LOG_CONTAINER_COUNT_MIN</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the <b>LogContainerCountMin</b> member is being used. If the 
        flag is not set, the <b>LogContainerCountMin</b> member is ignored. This flag is mutually 
        exclusive with <b>TXFS_RM_FLAG_LOG_NO_CONTAINER_COUNT_MAX</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_RM_FLAG_LOG_GROWTH_INCREMENT_NUM_CONTAINERS"></a><a id="txfs_rm_flag_log_growth_increment_num_containers"></a><dl>
<dt><b>TXFS_RM_FLAG_LOG_GROWTH_INCREMENT_NUM_CONTAINERS</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the <b>LogGrowthIncrement</b> member is being used. If the flag 
        is not set, the <b>LogGrowthIncrement</b> member is ignored. This flag indicates that the 
        log should grow by the number of containers specified in the <b>LogGrowthIncrement</b> 
        member. This flag is mutually exclusive with 
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
If this flag is set, the <b>LogGrowthIncrement</b> member is being used. If the flag 
        is not set, the <b>LogGrowthIncrement</b> member is ignored. This flag indicates that the 
        log should grow by the percentage of the log size specified in the 
        <b>LogGrowthIncrement</b> member. This flag is mutually exclusive with 
        <b>TXFS_RM_FLAG_LOG_GROWTH_INCREMENT_NUM_CONTAINERS</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_RM_FLAG_LOG_AUTO_SHRINK_PERCENTAGE"></a><a id="txfs_rm_flag_log_auto_shrink_percentage"></a><dl>
<dt><b>TXFS_RM_FLAG_LOG_AUTO_SHRINK_PERCENTAGE</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the <b>LogAutoShrinkPercentage</b> member is being used. If the 
        flag is not set, the <b>LogAutoShrinkPercentage</b> is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_RM_FLAG_LOG_NO_CONTAINER_COUNT_MAX"></a><a id="txfs_rm_flag_log_no_container_count_max"></a><dl>
<dt><b>TXFS_RM_FLAG_LOG_NO_CONTAINER_COUNT_MAX</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the RM is instructed to allow its log to grow without bounds. This flag is mutually 
        exclusive with <b>TXFS_RM_FLAG_LOG_NO_CONTAINER_COUNT_MIN</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_RM_FLAG_LOG_NO_CONTAINER_COUNT_MIN"></a><a id="txfs_rm_flag_log_no_container_count_min"></a><dl>
<dt><b>TXFS_RM_FLAG_LOG_NO_CONTAINER_COUNT_MIN</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the RM is instructed to allow its log to shrink the log to only two containers. This 
        flag is mutually exclusive with <b>TXFS_RM_FLAG_LOG_NO_CONTAINER_COUNT_MAX</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_RM_FLAG_GROW_LOG"></a><a id="txfs_rm_flag_grow_log"></a><dl>
<dt><b>TXFS_RM_FLAG_GROW_LOG</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the log is instructed to immediately increase its size to the size specified in 
        <b>LogContainerCount</b>. If the flag is not set, the 
        <b>LogContainerCount</b> is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_RM_FLAG_SHRINK_LOG"></a><a id="txfs_rm_flag_shrink_log"></a><dl>
<dt><b>TXFS_RM_FLAG_SHRINK_LOG</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the log is instructed to immediately decrease its size to the size specified in 
        <b>LogContainerCount</b>. If this flag and 
        <b>TXFS_RM_FLAG_ENFORCE_MINIMUM_SIZE</b> are set, the log is instructed to shrink to its 
        minimum allowable size, and <b>LogContainerCount</b> is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_RM_FLAG_ENFORCE_MINIMUM_SIZE"></a><a id="txfs_rm_flag_enforce_minimum_size"></a><dl>
<dt><b>TXFS_RM_FLAG_ENFORCE_MINIMUM_SIZE</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
If this flag and <b>TXFS_RM_FLAG_SHRINK_LOG</b> are set, the log is instructed to 
        shrink to its minimum allowable size, and <b>LogContainerCount</b> is ignored. If this 
        flag is set, the <b>TXFS_RM_FLAG_SHRINK_LOG</b> must be set.

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_RM_FLAG_PRESERVE_CHANGES"></a><a id="txfs_rm_flag_preserve_changes"></a><dl>
<dt><b>TXFS_RM_FLAG_PRESERVE_CHANGES</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the log is instructed to preserve the changes on disk. If this flag is not set, any 
        changes made are temporary (that is, until the RM is shut down and restarted).

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_RM_FLAG_RESET_RM_AT_NEXT_START"></a><a id="txfs_rm_flag_reset_rm_at_next_start"></a><dl>
<dt><b>TXFS_RM_FLAG_RESET_RM_AT_NEXT_START</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
This flag is only valid for default RMs, not secondary RMs. If this flag is set, the RM is instructed to 
        reset itself the next time it is started. The log and the associated metadata are deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_RM_FLAG_DO_NOT_RESET_RM_AT_NEXT_START"></a><a id="txfs_rm_flag_do_not_reset_rm_at_next_start"></a><dl>
<dt><b>TXFS_RM_FLAG_DO_NOT_RESET_RM_AT_NEXT_START</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
This flag is only valid for default RMs, not secondary RMs. If this flag is set, a previous call to 
        <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_txfs_modify_rm">FSCTL_TXFS_MODIFY_RM</a> is canceled with 
        the <b>TXFS_RM_FLAG_RESET_RM_AT_NEXT_START</b> flag set.

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
        <a href="/windows/win32/fileio/glossary">availability</a>. This flag is mutually exclusive with 
        <b>TXFS_RM_FLAG_PREFER_AVAILABILITY</b> and is not supported by the default RM on the 
        system volume.

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
        <a href="/windows/win32/fileio/glossary">consistency</a>. This flag is mutually exclusive with 
        <b>TXFS_RM_FLAG_PREFER_CONSISTENCY</b> and is forced by the default RM on the system 
        volume.

</td>
</tr>
</table>
 


### -field LogContainerCountMax

The maximum size of the log, in containers.


### -field LogContainerCountMin

The minimum size of the log, in containers.


### -field LogContainerCount

The actual size of the log, in containers.


### -field LogGrowthIncrement

The number of containers or percentage of space that should be added to the log.


### -field LogAutoShrinkPercentage

The percentage of log space to keep free. This member is used when the 
      <b>TXFS_RM_FLAG_LOG_AUTO_SHRINK_PERCENTAGE</b> flag is used, and instructs the log to 
      automatically shrink itself, so no more than <b>LogAutoShrinkPercentage</b> of the log is 
      free at any given time.


### -field Reserved

Reserved.


### -field LoggingMode

The current logging mode.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TXFS_LOGGING_MODE_SIMPLE"></a><a id="txfs_logging_mode_simple"></a><dl>
<dt><b><b>TXFS_LOGGING_MODE_SIMPLE</b></b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Simple logging is used.

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_LOGGING_MODE_FULL"></a><a id="txfs_logging_mode_full"></a><dl>
<dt><b><b>TXFS_LOGGING_MODE_FULL</b></b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Full logging is used

</td>
</tr>
</table>
 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_txfs_modify_rm">FSCTL_TXFS_MODIFY_RM</a>
 

 

