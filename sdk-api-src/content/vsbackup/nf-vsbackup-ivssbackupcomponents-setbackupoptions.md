---
UID: NF:vsbackup.IVssBackupComponents.SetBackupOptions
title: IVssBackupComponents::SetBackupOptions (vsbackup.h)
description: The SetBackupOptions method sets a string of private, or writer-dependent, backup parameters for a component.
helpviewer_keywords: ["IVssBackupComponents interface [VSS]","SetBackupOptions method","IVssBackupComponents.SetBackupOptions","IVssBackupComponents::SetBackupOptions","SetBackupOptions","SetBackupOptions method [VSS]","SetBackupOptions method [VSS]","IVssBackupComponents interface","_win32_ivssbackupcomponents_setbackupoptions","base.ivssbackupcomponents_setbackupoptions","vsbackup/IVssBackupComponents::SetBackupOptions"]
old-location: base\ivssbackupcomponents_setbackupoptions.htm
tech.root: base
ms.assetid: 2b9a64b2-2bc9-441b-97f7-a72fd7579126
ms.date: 12/05/2018
ms.keywords: IVssBackupComponents interface [VSS],SetBackupOptions method, IVssBackupComponents.SetBackupOptions, IVssBackupComponents::SetBackupOptions, SetBackupOptions, SetBackupOptions method [VSS], SetBackupOptions method [VSS],IVssBackupComponents interface, _win32_ivssbackupcomponents_setbackupoptions, base.ivssbackupcomponents_setbackupoptions, vsbackup/IVssBackupComponents::SetBackupOptions
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
 - IVssBackupComponents::SetBackupOptions
 - vsbackup/IVssBackupComponents::SetBackupOptions
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
 - IVssBackupComponents.SetBackupOptions
---

# IVssBackupComponents::SetBackupOptions


## -description

The 
<b>SetBackupOptions</b> method sets a string of private, or writer-dependent, backup parameters for a component.

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

There are no restrictions on the characters that can appear in a non-<b>NULL</b> logical path.

### -param wszComponentName [in]

<b>Null</b>-terminated wide character string containing the name of the component. 




The string containing the name cannot be <b>NULL</b> and should contain the same component name as was used when the component was added to the backup set using 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addcomponent">IVssBackupComponents::AddComponent</a>.

### -param wszBackupOptions [in]

<b>Null</b>-terminated wide character string containing the backup parameters to be set.

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
Successfully set the backup options.

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

The exact syntax and content of the backup options set by the <i>wszBackupOptions</i> parameter of the 
<b>SetBackupOptions</b> method will depend on the specific writer being contacted.

This method must be called before 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup">IVssBackupComponents::PrepareForBackup</a>.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup">IVssBackupComponents::PrepareForBackup</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions">IVssBackupComponents::SetRestoreOptions</a>



<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_component_type">VSS_COMPONENT_TYPE</a>