---
UID: NF:vsbackup.IVssBackupComponents.DisableWriterClasses
title: IVssBackupComponents::DisableWriterClasses (vsbackup.h)
description: The DisableWriterClasses method prevents a specific class of writers from receiving any events.
helpviewer_keywords: ["DisableWriterClasses","DisableWriterClasses method [VSS]","DisableWriterClasses method [VSS]","IVssBackupComponents interface","IVssBackupComponents interface [VSS]","DisableWriterClasses method","IVssBackupComponents.DisableWriterClasses","IVssBackupComponents::DisableWriterClasses","_win32_ivssbackupcomponents_disablewriterclasses","base.ivssbackupcomponents_disablewriterclasses","vsbackup/IVssBackupComponents::DisableWriterClasses"]
old-location: base\ivssbackupcomponents_disablewriterclasses.htm
tech.root: base
ms.assetid: 7567bf23-4f4c-4210-87f7-4f90262fda7a
ms.date: 12/05/2018
ms.keywords: DisableWriterClasses, DisableWriterClasses method [VSS], DisableWriterClasses method [VSS],IVssBackupComponents interface, IVssBackupComponents interface [VSS],DisableWriterClasses method, IVssBackupComponents.DisableWriterClasses, IVssBackupComponents::DisableWriterClasses, _win32_ivssbackupcomponents_disablewriterclasses, base.ivssbackupcomponents_disablewriterclasses, vsbackup/IVssBackupComponents::DisableWriterClasses
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
 - IVssBackupComponents::DisableWriterClasses
 - vsbackup/IVssBackupComponents::DisableWriterClasses
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
 - IVssBackupComponents.DisableWriterClasses
---

# IVssBackupComponents::DisableWriterClasses


## -description

The 
<b>DisableWriterClasses</b> method prevents a specific class of writers from receiving any events.

## -parameters

### -param rgWriterClassId [in]

An array containing one or more writer class identifiers.

### -param cClassId [in]

The number of entries in the <i>rgWriterClassId</i> array.

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
The writer class has been successfully disabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient backup privileges or is not an administrator.

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

If you have multiple running copies of the same writer, they will all have the same writer class identifier, but they will have different writer instance identifiers. Disabling a writer class causes all of the writer's instances to be disabled.

If the <b>DisableWriterClasses</b> method and the <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-enablewriterclasses">IVssBackupComponents::EnableWriterClasses</a> method are never called, all writer classes are enabled.

After the first call to <b>DisableWriterClasses</b> returns, the writer classes that were specified in the <i>rgWriterClassId</i> array are disabled, and all other writer classes are enabled.

If you call <b>DisableWriterClasses</b> more than once, each call adds the writers in the <i>rgWriterClassId</i> array to the list of disabled writers.

If you call <b>DisableWriterClasses</b> one or more times and then call <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-enablewriterclasses">EnableWriterClasses</a>, the first call to <b>EnableWriterClasses</b> cancels the effect of the calls to <b>DisableWriterClasses</b> and enables only the writers in the <i>rgWriterClassId</i> array.

If you call <b>DisableWriterClasses</b>, you must do so before calling the <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata">IVssBackupComponents::GatherWriterMetadata</a> method. If you call <b>GatherWriterMetadata</b> first and then call <b>DisableWriterClasses</b>, the call to <b>DisableWriterClasses</b> has no effect. If you need to call <b>GatherWriterMetadata</b> first, to determine which writer classes to disable, you must call it from a different instance of the <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a> interface.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-disablewriterinstances">IVssBackupComponents::DisableWriterInstances</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-enablewriterclasses">IVssBackupComponents::EnableWriterClasses</a>