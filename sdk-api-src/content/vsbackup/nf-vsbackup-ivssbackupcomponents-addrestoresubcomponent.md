---
UID: NF:vsbackup.IVssBackupComponents.AddRestoreSubcomponent
title: IVssBackupComponents::AddRestoreSubcomponent (vsbackup.h)
description: Indicates that a subcomponent member of a component set, which had been marked as nonselectable for backup but is marked selectable for restore, is to be restored.
helpviewer_keywords: ["AddRestoreSubcomponent","AddRestoreSubcomponent method [VSS]","AddRestoreSubcomponent method [VSS]","IVssBackupComponents interface","IVssBackupComponents interface [VSS]","AddRestoreSubcomponent method","IVssBackupComponents.AddRestoreSubcomponent","IVssBackupComponents::AddRestoreSubcomponent","_win32_ivssbackupcomponents_addrestoresubcomponent","base.ivssbackupcomponents_addrestoresubcomponent","vsbackup/IVssBackupComponents::AddRestoreSubcomponent"]
old-location: base\ivssbackupcomponents_addrestoresubcomponent.htm
tech.root: base
ms.assetid: 8eea27d7-6780-49cf-97ea-8876a9a2c8f8
ms.date: 12/05/2018
ms.keywords: AddRestoreSubcomponent, AddRestoreSubcomponent method [VSS], AddRestoreSubcomponent method [VSS],IVssBackupComponents interface, IVssBackupComponents interface [VSS],AddRestoreSubcomponent method, IVssBackupComponents.AddRestoreSubcomponent, IVssBackupComponents::AddRestoreSubcomponent, _win32_ivssbackupcomponents_addrestoresubcomponent, base.ivssbackupcomponents_addrestoresubcomponent, vsbackup/IVssBackupComponents::AddRestoreSubcomponent
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
 - IVssBackupComponents::AddRestoreSubcomponent
 - vsbackup/IVssBackupComponents::AddRestoreSubcomponent
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
 - IVssBackupComponents.AddRestoreSubcomponent
---

# IVssBackupComponents::AddRestoreSubcomponent


## -description

The <b>AddRestoreSubcomponent</b> 
    method indicates that a subcomponent member of a component set, which had been marked as nonselectable 
    for backup but is marked selectable for restore, is to be restored irrespective of whether any other 
    member of the component set will be restored.

## -parameters

### -param writerId [in]

Writer class identifier.

### -param componentType [in]

Identifies the type of the component. Refer to the documentation for 
      <a href="/windows/desktop/api/vswriter/ne-vswriter-vss_component_type">VSS_COMPONENT_TYPE</a> for possible return values.

### -param wszLogicalPath [in]

<b>Null</b>-terminated wide character string containing the logical path of the component in the backup document 
      that defines the backup component set containing the subcomponent to be added for restore. 
      

The value of this parameter can be <b>NULL</b>.

There are no restrictions on the characters that can appear in a non-<b>NULL</b> logical path.

### -param wszComponentName [in]

<b>Null</b>-terminated wide character string containing the logical path of the component in the backup document 
      that defines the backup component set containing the subcomponent to be added for restore.
      

The value of this parameter cannot be <b>NULL</b>.

There are no restrictions on the characters that can appear in a non-<b>NULL</b> component name.

### -param wszSubComponentLogicalPath [in]

<b>Null</b>-terminated wide character string containing the logical path of the subcomponent to be added for 
      restore.
      

A logical path is required when adding a subcomponent. Therefore, the value of this parameter cannot be 
       <b>NULL</b>.

There are no restrictions on the characters that can appear in a non-<b>NULL</b> logical path.

### -param wszSubComponentName [in]

<b>Null</b>-terminated wide character string containing the logical name of the subcomponent to be added for 
      restore. 
      

The value of this parameter cannot be <b>NULL</b>.

There are no restrictions on the characters that can appear in a non-<b>NULL</b> component name.

### -param bRepair [in]

This parameter is reserved for future use. This parameter should always be set to <b>false</b>

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
Successfully added the restore subcomponent.

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
The backup components object is not initialized, this method has not been called during a restore 
        operation, or this method has not been called within the correct sequence.

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
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The component does not exist.

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

Before calling 
    <b>AddRestoreSubcomponent</b>, the 
    root component defined by the <i>wszLogicalPath</i> and 
    <i>wszComponentName</i> parameters must first be selected for restore using 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore">IVssBackupComponents::SetSelectedForRestore</a>.

If a requester is to support restoring subcomponents, this method must be called before 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">IVssBackupComponents::PreRestore</a>.

<b>AddRestoreSubcomponent</b> 
    is intended for the case in which all the files in a writer's component set must be backed up as a unit, but where 
    it is desirable that selected files (subcomponents) be capable of being restored individually.

To participate in such a restore, a subcomponent must have the 
    <b>bSelectableForRestore</b> member of 
    <a href="/windows/desktop/api/vsbackup/ns-vsbackup-vss_componentinfo">VSS_COMPONENTINFO</a> set to <b>TRUE</b>. The component defined 
    by the <i>wszLogicalPath</i> and <i>wszComponentName</i> parameters must 
    also be selected for restore using 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore">IVssBackupComponents::SetSelectedForRestore</a>.

See <a href="/windows/desktop/VSS/working-with-selectability-for-restore-and-subcomponents">Working with 
    Selectability for Restore and Subcomponents</a> for more information.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">IVssBackupComponents::PreRestore</a>



<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_component_type">VSS_COMPONENT_TYPE</a>