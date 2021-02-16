---
UID: NF:vsbackup.IVssBackupComponents.AddComponent
title: IVssBackupComponents::AddComponent (vsbackup.h)
description: Used to explicitly add to the backup set.
helpviewer_keywords: ["AddComponent","AddComponent method [VSS]","AddComponent method [VSS]","IVssBackupComponents interface","IVssBackupComponents interface [VSS]","AddComponent method","IVssBackupComponents.AddComponent","IVssBackupComponents::AddComponent","_win32_ivssbackupcomponents_addcomponent","base.ivssbackupcomponents_addcomponent","vsbackup/IVssBackupComponents::AddComponent"]
old-location: base\ivssbackupcomponents_addcomponent.htm
tech.root: base
ms.assetid: 50cb0b16-9ed3-4496-962a-9c845c10986c
ms.date: 12/05/2018
ms.keywords: AddComponent, AddComponent method [VSS], AddComponent method [VSS],IVssBackupComponents interface, IVssBackupComponents interface [VSS],AddComponent method, IVssBackupComponents.AddComponent, IVssBackupComponents::AddComponent, _win32_ivssbackupcomponents_addcomponent, base.ivssbackupcomponents_addcomponent, vsbackup/IVssBackupComponents::AddComponent
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
 - IVssBackupComponents::AddComponent
 - vsbackup/IVssBackupComponents::AddComponent
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
 - IVssBackupComponents.AddComponent
---

# IVssBackupComponents::AddComponent


## -description

The <b>AddComponent</b> method is 
    used to explicitly add to the backup set in the Backup Components Document all required 
    components (nonselectable for backup components without a selectable for backup ancestor), and such optional 
    (selectable for backup) components as the requester considers necessary. Members of component sets (components 
    with a selectable for backup ancestor) are implicitly included in the backup set, but are not explicitly added to 
    the Backup Components Document.

## -parameters

### -param instanceId [in]

Identifies a specific instance of a writer.

### -param writerId [in]

Writer class identifier.

### -param ct [in]

Identifies the type of the component. Refer to the documentation for 
      <a href="/windows/desktop/api/vswriter/ne-vswriter-vss_component_type">VSS_COMPONENT_TYPE</a> for permitted input values.

### -param wszLogicalPath [in]

<b>Null</b>-terminated wide character string containing the logical path of the selectable for backup component.
      For more information, see <a href="/windows/desktop/VSS/logical-pathing-of-components">Logical Pathing of Components</a>.

A logical path is not required when adding a component. Therefore, the value of this parameter can be 
       <b>NULL</b>.

There are no restrictions on the characters that can appear in a non-<b>NULL</b> logical path.

### -param wszComponentName [in]

<b>Null</b>-terminated wide character string containing the name of the selectable for backup component.
      

The value of this parameter cannot be <b>NULL</b>.

There are no restrictions on the characters that can appear in a non-<b>NULL</b> logical path.

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
Successfully added the component.

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
The backup components object is not initialized, this method has been called during a restore operation, 
        or this method has not been called within the correct sequence.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_INVALID_XML_DOCUMENT</b></dt>
</dl>
</td>
<td width="60%">
The XML document is not valid. Check the event log for details. For more 
        information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The object is a duplicate. A component with the same logical path and component name already 
        exists.

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

The <b>AddComponent</b> method has meaning only if the backup operation takes place in component mode.

Only these kinds of components should be added to the Backup Components Document using <b>AddComponent</b>.
- Components that are selectable for backup (see <a href="/windows/win32/vss/vssgloss-s">selectability for backup</a>).
- Nonselectable-for-backup components with no selectable-for-backup ancestors.

Nonselectable for backup components that have a selectable for backup ancestor in the hierarchy of their 
    logical paths are part of a component set defined by the selectable for backup ancestor. These components are 
    implicitly added to the Backup Components Document when the ancestor is added and should never be explicitly added 
    to a requester's Backup Components Document by using 
    <b>AddComponent</b>.The result of doing so is 
    undefined (see <a href="/windows/desktop/VSS/working-with-selectability-and-logical-paths">Working with 
    Selectability and Logical Paths</a>).

Selectable for backup components with selectable for backup ancestors are also subcomponents in a component 
    set. They can be implicitly selected if their ancestor is selected (in which case they are not added to the Backup 
    Components Document using 
    <b>AddComponent</b>), or they can be 
    explicitly selected using 
    <b>AddComponent</b>.

The combination of logical path and name for each component of a given instance of a given class of writer 
    must be unique. Attempting to call 
    <b>AddComponent</b> twice with the same values 
    of <i>wszLogicalPath</i> and <i>wszComponentName</i> results in a 
    VSS_E_OBJECT_ALREADY_EXISTS error.

The distinction between the <i>instanceId</i> and the <i>writerID</i> is 
    necessary because it is possible to run multiple copies for the same writer.

A writer's class identifier and instance can be found by calling 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getidentity">IVssExamineWriterMetadata::GetIdentity</a>.

Before it calls <b>AddComponent</b>, a 
    requester must have been initialized for backup by calling 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup">IVssBackupComponents::InitializeForBackup</a> and <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata">IVssBackupComponents::GatherWriterMetadata</a>. See <a href="/windows/desktop/VSS/overview-of-backup-initialization">Overview of Backup Initialization</a>.

The requester must call <b>AddComponent</b> to add the required components to the shadow copy before calling <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset">IVssBackupComponents::DoSnapshotSet</a> to create the shadow copy. See <a href="/windows/desktop/VSS/overview-of-the-backup-discovery-phase">Overview of the Backup Discovery Phase</a> and <a href="/windows/desktop/VSS/overview-of-pre-backup-tasks">Overview of Pre-Backup Tasks</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize">CVssWriter::Initialize</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup">IVssBackupComponents::PrepareForBackup</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getidentity">IVssExamineWriterMetadata::GetIdentity</a>



<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_component_type">VSS_COMPONENT_TYPE</a>