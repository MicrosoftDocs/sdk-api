---
UID: NF:fhcfg.IFhConfigMgr.QueryProtectionStatus
title: IFhConfigMgr::QueryProtectionStatus (fhcfg.h)
description: Retrieves the current File History protection state.
helpviewer_keywords: ["FH_STATE_DISABLED_BY_GP","FH_STATE_FATAL_CONFIG_ERROR","FH_STATE_NOT_TRACKED","FH_STATE_NO_ERROR","FH_STATE_OFF","FH_STATE_STAGING_FULL","FH_STATE_TARGET_ABSENT","FH_STATE_TARGET_ACCESS_DENIED","FH_STATE_TARGET_FULL","FH_STATE_TARGET_FULL_RETENTION_MAX","FH_STATE_TARGET_LOW_SPACE","FH_STATE_TARGET_LOW_SPACE_RETENTION_MAX","FH_STATE_TARGET_VOLUME_DIRTY","FH_STATE_TOO_MUCH_BEHIND","FhConfigMgr class [Windows API]","QueryProtectionStatus method","IFhConfigMgr interface [Windows API]","QueryProtectionStatus method","IFhConfigMgr.QueryProtectionStatus","IFhConfigMgr::QueryProtectionStatus","QueryProtectionStatus","QueryProtectionStatus method [Windows API]","QueryProtectionStatus method [Windows API]","FhConfigMgr class","QueryProtectionStatus method [Windows API]","IFhConfigMgr interface","fhcfg/IFhConfigMgr::QueryProtectionStatus","winprog.ifhconfigmgr_queryprotectionstatus"]
old-location: winprog\ifhconfigmgr_queryprotectionstatus.htm
tech.root: winprog
ms.assetid: 662B1F54-D50D-4434-BD81-DF600D28B573
ms.date: 12/05/2018
ms.keywords: FH_STATE_DISABLED_BY_GP, FH_STATE_FATAL_CONFIG_ERROR, FH_STATE_NOT_TRACKED, FH_STATE_NO_ERROR, FH_STATE_OFF, FH_STATE_STAGING_FULL, FH_STATE_TARGET_ABSENT, FH_STATE_TARGET_ACCESS_DENIED, FH_STATE_TARGET_FULL, FH_STATE_TARGET_FULL_RETENTION_MAX, FH_STATE_TARGET_LOW_SPACE, FH_STATE_TARGET_LOW_SPACE_RETENTION_MAX, FH_STATE_TARGET_VOLUME_DIRTY, FH_STATE_TOO_MUCH_BEHIND, FhConfigMgr class [Windows API],QueryProtectionStatus method, IFhConfigMgr interface [Windows API],QueryProtectionStatus method, IFhConfigMgr.QueryProtectionStatus, IFhConfigMgr::QueryProtectionStatus, QueryProtectionStatus, QueryProtectionStatus method [Windows API], QueryProtectionStatus method [Windows API],FhConfigMgr class, QueryProtectionStatus method [Windows API],IFhConfigMgr interface, fhcfg/IFhConfigMgr::QueryProtectionStatus, winprog.ifhconfigmgr_queryprotectionstatus
req.header: fhcfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fhcfg.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFhConfigMgr::QueryProtectionStatus
 - fhcfg/IFhConfigMgr::QueryProtectionStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fhcfg.h
api_name:
 - IFhConfigMgr.QueryProtectionStatus
 - FhConfigMgr.QueryProtectionStatus
---

# IFhConfigMgr::QueryProtectionStatus


## -description

Retrieves the current File History protection state.

> [!NOTE] 
> **IFhConfigMgr** is deprecated and may be altered or unavailable in future releases.

## -parameters

### -param ProtectionState [out]

On return, this parameter receives the current File History protection state. The following protection states are defined in the FhStatus.h header file.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FH_STATE_NOT_TRACKED"></a><a id="fh_state_not_tracked"></a><dl>
<dt><b>FH_STATE_NOT_TRACKED</b></dt>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
The File History protection state is unknown, because the File History service is not started or the current user is not tracked in it. This value cannot be ORed with <b>FH_STATE_RUNNING</b> (0x100).

</td>
</tr>
<tr>
<td width="40%"><a id="FH_STATE_OFF"></a><a id="fh_state_off"></a><dl>
<dt><b>FH_STATE_OFF</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
File History protection is not enabled for the current user. No files will be backed up. This value cannot be ORed with <b>FH_STATE_RUNNING</b> (0x100).

</td>
</tr>
<tr>
<td width="40%"><a id="FH_STATE_DISABLED_BY_GP"></a><a id="fh_state_disabled_by_gp"></a><dl>
<dt><b>FH_STATE_DISABLED_BY_GP</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
File History protection is disabled by Group Policy. No files will be backed up. This value cannot be ORed with <b>FH_STATE_RUNNING</b> (0x100).

</td>
</tr>
<tr>
<td width="40%"><a id="FH_STATE_FATAL_CONFIG_ERROR"></a><a id="fh_state_fatal_config_error"></a><dl>
<dt><b>FH_STATE_FATAL_CONFIG_ERROR</b></dt>
<dt>0x03</dt>
</dl>
</td>
<td width="60%">
There is a fatal error in one of the files that store internal File History information for the current user. No files will be backed up. This value cannot be ORed with <b>FH_STATE_RUNNING</b> (0x100).

</td>
</tr>
<tr>
<td width="40%"><a id="FH_STATE_TARGET_ACCESS_DENIED"></a><a id="fh_state_target_access_denied"></a><dl>
<dt><b>FH_STATE_TARGET_ACCESS_DENIED</b></dt>
<dt>0x0E</dt>
</dl>
</td>
<td width="60%">
The current user does not have write permission for the currently assigned target. Backup copies of file versions will not be  created. This value can be ORed with <b>FH_STATE_RUNNING</b> (0x100) to indicate that a backup cycle is being performed for the current user right now.

</td>
</tr>
<tr>
<td width="40%"><a id="FH_STATE_TARGET_VOLUME_DIRTY"></a><a id="fh_state_target_volume_dirty"></a><dl>
<dt><b>FH_STATE_TARGET_VOLUME_DIRTY</b></dt>
<dt>0x0F</dt>
</dl>
</td>
<td width="60%">
The currently assigned target has been marked as dirty. Backup copies of file versions will not be created until after the <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc730714(v=ws.11)">Chkdsk</a> utility is run. This value can be ORed with <b>FH_STATE_RUNNING</b> (0x100) to indicate that a backup cycle is being performed for the current user right now.

</td>
</tr>
<tr>
<td width="40%"><a id="FH_STATE_TARGET_FULL_RETENTION_MAX"></a><a id="fh_state_target_full_retention_max"></a><dl>
<dt><b>FH_STATE_TARGET_FULL_RETENTION_MAX</b></dt>
<dt>0x10</dt>
</dl>
</td>
<td width="60%">
The currently assigned target does not have sufficient space for storing backup copies of files from the File History protection scope, and retention is already set to the most aggressive policy. File History will provide a degraded level of protection. This value can be ORed with <b>FH_STATE_RUNNING</b> (0x100) to indicate that a backup cycle is being performed for the current user right now.

</td>
</tr>
<tr>
<td width="40%"><a id="FH_STATE_TARGET_FULL"></a><a id="fh_state_target_full"></a><dl>
<dt><b>FH_STATE_TARGET_FULL</b></dt>
<dt>0x11</dt>
</dl>
</td>
<td width="60%">
The currently assigned target does not have sufficient space for storing backup copies of files from the File History protection scope. File History will provide a degraded level of protection. This value can be ORed with <b>FH_STATE_RUNNING</b> (0x100) to indicate that a backup cycle is being performed for the current user right now.

</td>
</tr>
<tr>
<td width="40%"><a id="FH_STATE_STAGING_FULL"></a><a id="fh_state_staging_full"></a><dl>
<dt><b>FH_STATE_STAGING_FULL</b></dt>
<dt>0x12</dt>
</dl>
</td>
<td width="60%">
The File History cache on one of the local disks does not have sufficient space for storing backup copies of files from the File History protection scope temporarily. File History will provide a degraded level of protection. This value can be ORed with <b>FH_STATE_RUNNING</b> (0x100) to indicate that a backup cycle is being performed for the current user right now.

</td>
</tr>
<tr>
<td width="40%"><a id="FH_STATE_TARGET_LOW_SPACE_RETENTION_MAX"></a><a id="fh_state_target_low_space_retention_max"></a><dl>
<dt><b>FH_STATE_TARGET_LOW_SPACE_RETENTION_MAX</b></dt>
<dt>0x13</dt>
</dl>
</td>
<td width="60%">
The currently assigned target is running low on free space, and retention is already set to the most aggressive policy. The level of File History protection is likely to degrade soon. This value can be ORed with <b>FH_STATE_RUNNING</b> (0x100) to indicate that a backup cycle is being performed for the current user right now.

</td>
</tr>
<tr>
<td width="40%"><a id="FH_STATE_TARGET_LOW_SPACE"></a><a id="fh_state_target_low_space"></a><dl>
<dt><b>FH_STATE_TARGET_LOW_SPACE</b></dt>
<dt>0x14</dt>
</dl>
</td>
<td width="60%">
The currently assigned target is running low on free space. The level of File History protection is likely to degrade soon. This value can be ORed with <b>FH_STATE_RUNNING</b> (0x100) to indicate that a backup cycle is being performed for the current user right now.

</td>
</tr>
<tr>
<td width="40%"><a id="FH_STATE_TARGET_ABSENT"></a><a id="fh_state_target_absent"></a><dl>
<dt><b>FH_STATE_TARGET_ABSENT</b></dt>
<dt>0x15</dt>
</dl>
</td>
<td width="60%">
The currently assigned target has not been available for backups for a substantial period of time, causing File History level of protection to start degrading. This value can be ORed with <b>FH_STATE_RUNNING</b> (0x100) to indicate that a backup cycle is being performed for the current user right now.

</td>
</tr>
<tr>
<td width="40%"><a id="FH_STATE_TOO_MUCH_BEHIND"></a><a id="fh_state_too_much_behind"></a><dl>
<dt><b>FH_STATE_TOO_MUCH_BEHIND</b></dt>
<dt>0x16</dt>
</dl>
</td>
<td width="60%">
Too many changes have been made in the protected files or the protection scope. File History level of protection is likely to degrade, unless the user explicitly initiates an immediate backup instead of relying on regular backup cycles to be performed in the background. This value can be ORed with <b>FH_STATE_RUNNING</b> (0x100) to indicate that a backup cycle is being performed for the current user right now.

</td>
</tr>
<tr>
<td width="40%"><a id="FH_STATE_NO_ERROR"></a><a id="fh_state_no_error"></a><dl>
<dt><b>FH_STATE_NO_ERROR</b></dt>
<dt>0xFF</dt>
</dl>
</td>
<td width="60%">
File History backups are performed regularly, no error conditions are detected, an optimal level of File History protection is provided. This value can be ORed with <b>FH_STATE_RUNNING</b> (0x100) to indicate that a backup cycle is being performed for the current user right now.

</td>
</tr>
</table>

### -param ProtectedUntilTime [out]

Receives a pointer to a string allocated with <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> containing the date and time until which all files within the File History protection scope are protected. The date and time are formatted per the system locale. If the date and time are unknown, an empty string is returned.

A file is considered protected until a certain point in time if one of the following conditions is true:<ul>
<li>There is a version of that file that was captured at or after that point in time and was fully copied to the currently assigned backup target before now.</li>
<li>The file was created or included in the File History protection scope at or after that point in time.</li>
</ul>

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code such as one of the values defined in the FhErrors.h header file.

## -remarks

The caller is responsible for releasing the memory allocated for <i>ProtectedUntilTime</i> by calling <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> on it.

The protection state indicates the File History operational state and the date and time until which all files within the protection scope are protected.

If the target is full or disconnected, the File History feature will provide a degraded level of protection as follows: 

<ul>
<li>Files will be backed up to the File History cache on one of the local disks.</li>
<li>If the cache fills up during this time, older copies will be deleted from the cache to back up newer copies.</li>
<li>If the target is low on free space, the degraded level of protection will start once the target becomes full.</li>
</ul>

## -see-also

<a href="/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a>



<a href="/windows/desktop/api/fhcfg/nn-fhcfg-ifhconfigmgr">IFhConfigMgr</a>