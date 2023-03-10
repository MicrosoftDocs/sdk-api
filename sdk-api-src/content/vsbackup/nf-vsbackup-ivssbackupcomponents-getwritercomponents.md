---
UID: NF:vsbackup.IVssBackupComponents.GetWriterComponents
title: IVssBackupComponents::GetWriterComponents (vsbackup.h)
description: The GetWriterComponents method is used to return information about those components of a given writer that have been stored in a requester's Backup Components Document.
helpviewer_keywords: ["GetWriterComponents","GetWriterComponents method [VSS]","GetWriterComponents method [VSS]","IVssBackupComponents interface","IVssBackupComponents interface [VSS]","GetWriterComponents method","IVssBackupComponents.GetWriterComponents","IVssBackupComponents::GetWriterComponents","_win32_ivssbackupcomponents_getwritercomponents","base.ivssbackupcomponents_getwritercomponents","vsbackup/IVssBackupComponents::GetWriterComponents"]
old-location: base\ivssbackupcomponents_getwritercomponents.htm
tech.root: base
ms.assetid: b99e7e41-1c88-462c-b6d8-734f7a6e24d4
ms.date: 12/05/2018
ms.keywords: GetWriterComponents, GetWriterComponents method [VSS], GetWriterComponents method [VSS],IVssBackupComponents interface, IVssBackupComponents interface [VSS],GetWriterComponents method, IVssBackupComponents.GetWriterComponents, IVssBackupComponents::GetWriterComponents, _win32_ivssbackupcomponents_getwritercomponents, base.ivssbackupcomponents_getwritercomponents, vsbackup/IVssBackupComponents::GetWriterComponents
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
 - IVssBackupComponents::GetWriterComponents
 - vsbackup/IVssBackupComponents::GetWriterComponents
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
 - IVssBackupComponents.GetWriterComponents
---

# IVssBackupComponents::GetWriterComponents


## -description

The 
<b>GetWriterComponents</b> method is used to return information about those components of a given writer that have been stored in a requester's Backup Components Document.

## -parameters

### -param iWriter [in]

The index of the writer being queried. It is a number between 0 and <i>n</i>-1, where <i>n</i> is the value returned by 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount">IVssBackupComponents::GetWriterComponentsCount</a>.

### -param ppWriter [out]

Doubly indirect pointer to an 
<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivsswritercomponentsext">IVssWriterComponentsExt</a> interface object that will receive the returned component information.

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
Successfully returned a pointer to an 
<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivsswritercomponentsext">IVssWriterComponentsExt</a> interface object.

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
The specified shadow copy does not exist.

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

The caller of this method must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> when it finishes accessing the component information.

<b>GetWriterComponents</b> retrieves component information for a component stored in the Backup Components Document by earlier calls to 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addcomponent">IVssBackupComponents::AddComponent</a>.

The information in the components stored in the Backup Components Document is not static. If a writer updates a component during a restore, that change will be reflected in the component retrieved by 
<b>GetWriterComponents</b>. This is in contrast with component information found in the 
<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivsswmcomponent">IVssWMComponent</a> object returned by 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent">IVssExamineWriterMetadata::GetComponent</a>. That information is read-only and comes from the Writer Metadata Document of a writer process.

The <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivsswritercomponentsext">IVssWriterComponentsExt</a> interface pointer that is returned in the <i>pWriterComponents</i> parameter should not be cached, because the following <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a> methods cause the interface pointer that is returned by <b>GetWriterComponents</b> to be no longer valid:

<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup">IVssBackupComponents::PrepareForBackup</a>
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset">IVssBackupComponents::DoSnapshotSet</a>
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-backupcomplete">IVssBackupComponents::BackupComplete</a>
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">IVssBackupComponents::PreRestore</a>
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-postrestore">IVssBackupComponents::PostRestore</a>
If you call one of these methods after you have retrieved an <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivsswritercomponentsext">IVssWriterComponentsExt</a> interface pointer by calling <b>GetWriterComponents</b>, you cannot reuse that pointer, because it is no longer valid. Instead, you must call <b>GetWriterComponents</b> again to retrieve a new <b>IVssWriterComponentsExt</b> interface pointer.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addcomponent">IVssBackupComponents::AddComponent</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata">IVssBackupComponents::GatherWriterMetadata</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount">IVssBackupComponents::GetWriterComponentsCount</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata">IVssBackupComponents::GetWriterMetadata</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">IVssBackupComponents::PreRestore</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadata">IVssExamineWriterMetadata</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent">IVssExamineWriterMetadata::GetComponent</a>



<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswritercomponents">IVssWriterComponents</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivsswritercomponentsext">IVssWriterComponentsExt</a>