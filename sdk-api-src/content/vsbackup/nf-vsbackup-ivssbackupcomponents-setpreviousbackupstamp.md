---
UID: NF:vsbackup.IVssBackupComponents.SetPreviousBackupStamp
title: IVssBackupComponents::SetPreviousBackupStamp (vsbackup.h)
description: The SetPreviousBackupStamp method sets the backup stamp of an earlier backup operation, upon which a differential or incremental backup operation will be based.
helpviewer_keywords: ["IVssBackupComponents interface [VSS]","SetPreviousBackupStamp method","IVssBackupComponents.SetPreviousBackupStamp","IVssBackupComponents::SetPreviousBackupStamp","SetPreviousBackupStamp","SetPreviousBackupStamp method [VSS]","SetPreviousBackupStamp method [VSS]","IVssBackupComponents interface","_win32_ivssbackupcomponents_setpreviousbackupstamp","base.ivssbackupcomponents_setpreviousbackupstamp","vsbackup/IVssBackupComponents::SetPreviousBackupStamp"]
old-location: base\ivssbackupcomponents_setpreviousbackupstamp.htm
tech.root: base
ms.assetid: cc1c75bf-b281-4741-9273-f7264532860f
ms.date: 12/05/2018
ms.keywords: IVssBackupComponents interface [VSS],SetPreviousBackupStamp method, IVssBackupComponents.SetPreviousBackupStamp, IVssBackupComponents::SetPreviousBackupStamp, SetPreviousBackupStamp, SetPreviousBackupStamp method [VSS], SetPreviousBackupStamp method [VSS],IVssBackupComponents interface, _win32_ivssbackupcomponents_setpreviousbackupstamp, base.ivssbackupcomponents_setpreviousbackupstamp, vsbackup/IVssBackupComponents::SetPreviousBackupStamp
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
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
 - IVssBackupComponents::SetPreviousBackupStamp
 - vsbackup/IVssBackupComponents::SetPreviousBackupStamp
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
 - IVssBackupComponents.SetPreviousBackupStamp
---

# IVssBackupComponents::SetPreviousBackupStamp


## -description

The 
<b>SetPreviousBackupStamp</b> method sets the backup stamp of an earlier backup operation, upon which a differential or incremental backup operation will be based.

The method can be called only during a backup operation.

## -parameters

### -param writerId [in]

Writer identifier.

### -param ct [in]

Type of the component. See 
<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_component_type">VSS_COMPONENT_TYPE</a> for the possible values.

### -param wszLogicalPath [in]

<b>Null</b>-terminated wide character string containing the logical path of the component. 


For more information, see <a href="/windows/desktop/VSS/logical-pathing-of-components">Logical Pathing of Components</a>.

The value of the string containing the logical path used here should be the same as was used when the component was added to the backup set using 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addcomponent">IVssBackupComponents::AddComponent</a>.

The logical path can be <b>NULL</b>.

### -param wszComponentName [in]

<b>Null</b>-terminated wide character string containing the name of the component. 




The string cannot be <b>NULL</b> and should contain the same component name as was used when the component was added to the backup set using 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addcomponent">IVssBackupComponents::AddComponent</a>.

### -param wszPreviousBackupStamp [in]

The backup stamp to be set.

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
Successfully set the previous backup time stamp.

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
The backup components object is not initialized, this method has been called during a restore operation, or this method has not been called within the correct sequence.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The backup component does not exist.

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
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error. The error code is logged in the error log file. For more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>

## -remarks

This method should be called before 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup">IVssBackupComponents::PrepareForBackup</a>.

Only requesters can call this method.

The backup stamp set by 
<b>SetPreviousBackupStamp</b> applies to all files in the component and any nonselectable subcomponents it has.

Requesters merely store the backup stamps in the Backup Components Document. They cannot make direct use of the backup stamps, do not know their format, and do not know how to generate them.

Therefore, the value set with 
<b>SetPreviousBackupStamp</b> should either be retrieved from the stored Backup Components Document of an earlier backup operation (using 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getbackupstamp">IVssComponent::GetBackupStamp</a> for the correct component), or from information stored by the requester into its own internal records.

A writer will then obtain this value (using 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp">IVssComponent::GetPreviousBackupStamp</a>) and using it will be able to mark the appropriate files for participation in an incremental or differential backup.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">IVssBackupComponents::PreRestore</a>