---
UID: NF:vswriter.IVssComponent.GetFileRestoreStatus
title: IVssComponent::GetFileRestoreStatus (vswriter.h)
description: The GetFileRestoreStatus method returns the status of a completed attempt to restore all the files of a selected component or component set as a VSS_FILE_RESTORE_STATUS enumeration.
helpviewer_keywords: ["GetFileRestoreStatus","GetFileRestoreStatus method [VSS]","GetFileRestoreStatus method [VSS]","IVssComponent interface","IVssComponent interface [VSS]","GetFileRestoreStatus method","IVssComponent.GetFileRestoreStatus","IVssComponent::GetFileRestoreStatus","_win32_ivsscomponent_getfilerestorestatus","base.ivsscomponent_getfilerestorestatus","vswriter/IVssComponent::GetFileRestoreStatus"]
old-location: base\ivsscomponent_getfilerestorestatus.htm
tech.root: base
ms.assetid: b79c4443-c850-4edf-bdd2-917e22e67d77
ms.date: 12/05/2018
ms.keywords: GetFileRestoreStatus, GetFileRestoreStatus method [VSS], GetFileRestoreStatus method [VSS],IVssComponent interface, IVssComponent interface [VSS],GetFileRestoreStatus method, IVssComponent.GetFileRestoreStatus, IVssComponent::GetFileRestoreStatus, _win32_ivsscomponent_getfilerestorestatus, base.ivsscomponent_getfilerestorestatus, vswriter/IVssComponent::GetFileRestoreStatus
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
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
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssComponent::GetFileRestoreStatus
 - vswriter/IVssComponent::GetFileRestoreStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssComponent.GetFileRestoreStatus
---

# IVssComponent::GetFileRestoreStatus


## -description

The 
<b>GetFileRestoreStatus</b> method returns the status of a completed attempt to restore all the files of a selected component or component set as a 
<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_file_restore_status">VSS_FILE_RESTORE_STATUS</a> enumeration. (See 
<a href="/windows/desktop/VSS/working-with-selectability-and-logical-paths">Working with Selectability and Logical Paths</a> for information on selecting components.)

Either a writer or a requester can call this method.

## -parameters

### -param pStatus [out]

The address of a caller-allocated variable that receives a 
<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_file_restore_status">VSS_FILE_RESTORE_STATUS</a> enumeration value that specifies whether all files were successfully restored.

## -returns

The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Successfully returned the attribute value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_BAD_STATE</b></dt>
</dl>
</td>
<td width="60%">
The method was not called as part of a restore operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_INVALID_XML_DOCUMENT</b></dt>
</dl>
</td>
<td width="60%">
The XML document is not valid. Check the event log for details. For more information, see 
<a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

</td>
</tr>
</table>

## -remarks

This method should be called only following a 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-postrestore">PostRestore</a> event.

The status returned is undefined if this method is applied to a component that has not been selected for restore by being added to the Backup Components via 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addcomponent">IVssBackupComponents::AddComponent</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>



<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_file_restore_status">VSS_FILE_RESTORE_STATUS</a>