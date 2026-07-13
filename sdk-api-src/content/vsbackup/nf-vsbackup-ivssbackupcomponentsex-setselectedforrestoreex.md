---
UID: NF:vsbackup.IVssBackupComponentsEx.SetSelectedForRestoreEx
title: IVssBackupComponentsEx::SetSelectedForRestoreEx (vsbackup.h)
description: The SetSelectedForRestoreEx method indicates whether the specified selectable component is selected for restoration to a specified writer instance.
helpviewer_keywords: ["IVssBackupComponentsEx interface [VSS]","SetSelectedForRestoreEx method","IVssBackupComponentsEx.SetSelectedForRestoreEx","IVssBackupComponentsEx::SetSelectedForRestoreEx","SetSelectedForRestoreEx","SetSelectedForRestoreEx method [VSS]","SetSelectedForRestoreEx method [VSS]","IVssBackupComponentsEx interface","base.ivssbackupcomponentsex_setselectedforrestoreex","vsbackup/IVssBackupComponentsEx::SetSelectedForRestoreEx"]
old-location: base\ivssbackupcomponentsex_setselectedforrestoreex.htm
tech.root: base
ms.assetid: 469e6d61-85c6-4385-92be-df6addefe37f
ms.date: 12/05/2018
ms.keywords: IVssBackupComponentsEx interface [VSS],SetSelectedForRestoreEx method, IVssBackupComponentsEx.SetSelectedForRestoreEx, IVssBackupComponentsEx::SetSelectedForRestoreEx, SetSelectedForRestoreEx, SetSelectedForRestoreEx method [VSS], SetSelectedForRestoreEx method [VSS],IVssBackupComponentsEx interface, base.ivssbackupcomponentsex_setselectedforrestoreex, vsbackup/IVssBackupComponentsEx::SetSelectedForRestoreEx
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
 - IVssBackupComponentsEx::SetSelectedForRestoreEx
 - vsbackup/IVssBackupComponentsEx::SetSelectedForRestoreEx
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
 - IVssBackupComponentsEx.SetSelectedForRestoreEx
---

# IVssBackupComponentsEx::SetSelectedForRestoreEx


## -description

The 
    <b>SetSelectedForRestoreEx</b> method indicates whether the specified selectable component is selected for restoration to a specified writer instance.

## -parameters

### -param writerId [in]

Globally unique identifier (GUID) of the writer class.

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
      the <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addcomponent">IVssBackupComponents::AddComponent</a> method.

### -param bSelectedForRestore [in]

If the value of this parameter is <b>true</b>, the selected component has been selected for restoration. If the 
     value is <b>false</b>, the selected component has not been selected for restoration.

### -param instanceId [in]

GUID of the writer instance.

The default value for this parameter is GUID_NULL.

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

<b>SetSelectedForRestoreEx</b>, which moves a component to a different writer instance, can be called only for a writer that supports running multiple writer instances with the same class ID and supports a requester moving a component to a different writer instance at restore time. To determine whether a writer provides this support, call the <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema">IVssExamineWriterMetadata::GetBackupSchema</a> method.

<b>SetSelectedForRestoreEx</b> has 
    meaning only for restores taking place in component mode.

<b>SetSelectedForRestoreEx</b> can 
    be called only for components that were explicitly added to the backup document at backup time using 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addcomponent">AddComponent</a>. 
    Restoring a component that was implicitly selected for backup as part of a component set must be done by calling 
   <b>SetSelectedForRestoreEx</b> on the 
    closest ancestor component that was added to the document. If only this component's data is to be restored, that 
    should be accomplished through 
    the <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent">IVssBackupComponents::AddRestoreSubcomponent</a> method; 
    this can be done only if the component is selectable for restore (see 
    <a href="/windows/desktop/VSS/working-with-selectability-and-logical-paths">Working with Selectability and 
    Logical Paths</a>).

This method must be called before 
    the <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">IVssBackupComponents::PreRestore</a> method.

The distinction between the <i>instanceId</i> and <i>writerID</i> parameters is necessary because it is possible that multiple instances of the same writer are running on the computer.

If the value of the <i>instanceId</i> parameter is  GUID_NULL, this is equivalent to calling the <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore">IVssBackupComponents::SetSelectedForRestore</a> method.

The <i>instanceId</i> parameter is used to specify that the component is to be restored to a different writer instance. If the value of the <i>instanceId</i> parameter is not GUID_NULL, it must match the instance ID of a writer instance with the same writer class ID specified in the <i>writerID</i> parameter.

A writer's class identifier, instance identifier, and instance name can be found by calling the <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadataex-getidentityex">IVssExamineWriterMetadataEx::GetIdentityEx</a> method.

## -see-also

<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore">IVssBackupComponents::SetSelectedForRestore</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponentsex">IVssBackupComponentsEx</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema">IVssExamineWriterMetadata::GetBackupSchema</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadataex-getidentityex">IVssExamineWriterMetadataEx::GetIdentityEx</a>