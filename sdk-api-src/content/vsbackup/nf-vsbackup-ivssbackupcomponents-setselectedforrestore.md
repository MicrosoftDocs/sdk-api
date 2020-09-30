---
UID: NF:vsbackup.IVssBackupComponents.SetSelectedForRestore
title: IVssBackupComponents::SetSelectedForRestore (vsbackup.h)
description: The SetSelectedForRestore method indicates whether the specified selectable component is selected for restoration.
helpviewer_keywords: ["IVssBackupComponents interface [VSS]","SetSelectedForRestore method","IVssBackupComponents.SetSelectedForRestore","IVssBackupComponents::SetSelectedForRestore","SetSelectedForRestore","SetSelectedForRestore method [VSS]","SetSelectedForRestore method [VSS]","IVssBackupComponents interface","_win32_ivssbackupcomponents_setselectedforrestore","base.ivssbackupcomponents_setselectedforrestore","vsbackup/IVssBackupComponents::SetSelectedForRestore"]
old-location: base\ivssbackupcomponents_setselectedforrestore.htm
tech.root: base
ms.assetid: 8f8051d3-b1b6-418b-8a53-0ddc82a20bb3
ms.date: 12/05/2018
ms.keywords: IVssBackupComponents interface [VSS],SetSelectedForRestore method, IVssBackupComponents.SetSelectedForRestore, IVssBackupComponents::SetSelectedForRestore, SetSelectedForRestore, SetSelectedForRestore method [VSS], SetSelectedForRestore method [VSS],IVssBackupComponents interface, _win32_ivssbackupcomponents_setselectedforrestore, base.ivssbackupcomponents_setselectedforrestore, vsbackup/IVssBackupComponents::SetSelectedForRestore
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
 - IVssBackupComponents::SetSelectedForRestore
 - vsbackup/IVssBackupComponents::SetSelectedForRestore
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
 - IVssBackupComponents.SetSelectedForRestore
---

# IVssBackupComponents::SetSelectedForRestore


## -description

The <b>SetSelectedForRestore</b> 
    method indicates whether the specified selectable component is selected for restoration.

## -parameters

### -param writerId [in]

Writer identifier.

### -param ct [in]

Type of the component. See <a href="/windows/desktop/api/vswriter/ne-vswriter-vss_component_type">VSS_COMPONENT_TYPE</a> 
      for the possible values.

### -param wszLogicalPath [in]

<b>Null</b>-terminated wide character string containing the logical path of the component. 
      For more information, see <a href="/windows/desktop/VSS/logical-pathing-of-components">Logical Pathing of Components</a>.

The value of the string containing the logical path used here should be the same as was used when the 
       component was added.

The logical path can be <b>NULL</b>.

There are no restrictions on the characters that can appear in a non-<b>NULL</b> logical path.

### -param wszComponentName [in]

<b>Null</b>-terminated wide character string containing the name of the component. 
     

The string cannot be <b>NULL</b> and should contain the same component name as was used when the component was added 
      to the backup set using 
      <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addcomponent">IVssBackupComponents::AddComponent</a>.

### -param bSelectedForRestore [in]

If the value of this parameter is <b>true</b>, the selected component has been selected for restoration. If the 
     value is <b>false</b>, the selected component has not been selected for restoration.

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
Successfully indicated that the specified component has been selected to be restored.

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
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The component being selected does not exist in the Backup Components Document, or a live instance of the 
        writer corresponding to that component is not running on the system.

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

<b>SetSelectedForRestore</b> has 
    meaning only for restores taking place in component mode.

<b>SetSelectedForRestore</b> can 
    only be called for components that were explicitly added to the backup document at backup time using 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addcomponent">IVssBackupComponents::AddComponent</a>. 
    Restoring a component that was implicitly selected for backup as part of a component set must be done by calling 
   <b>SetSelectedForRestore</b> on the 
    closest ancestor component that was added to the document. If only this component's data is to be restored, that 
    should be accomplished through 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent">IVssBackupComponents::AddRestoreSubcomponent</a>; 
    this can only be done if the component is selectable for restore (see 
    <a href="/windows/desktop/VSS/working-with-selectability-and-logical-paths">Working with Selectability and 
    Logical Paths</a>).

This method must be called before 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">IVssBackupComponents::PreRestore</a>.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">IVssBackupComponents::PreRestore</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-isselectedforrestore">IVssComponent::IsSelectedForRestore</a>



<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_component_type">VSS_COMPONENT_TYPE</a>