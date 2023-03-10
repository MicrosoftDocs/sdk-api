---
UID: NF:vsbackup.IVssBackupComponents.GetWriterComponentsCount
title: IVssBackupComponents::GetWriterComponentsCount (vsbackup.h)
description: The GetWriterComponentsCount method returns the number of writers whose components have been added to a requester's Backup Components Document.
helpviewer_keywords: ["GetWriterComponentsCount","GetWriterComponentsCount method [VSS]","GetWriterComponentsCount method [VSS]","IVssBackupComponents interface","IVssBackupComponents interface [VSS]","GetWriterComponentsCount method","IVssBackupComponents.GetWriterComponentsCount","IVssBackupComponents::GetWriterComponentsCount","_win32_ivssbackupcomponents_getwritercomponentscount","base.ivssbackupcomponents_getwritercomponentscount","vsbackup/IVssBackupComponents::GetWriterComponentsCount"]
old-location: base\ivssbackupcomponents_getwritercomponentscount.htm
tech.root: base
ms.assetid: 39ab6179-2828-46dc-bfcd-0dd62c34ce95
ms.date: 12/05/2018
ms.keywords: GetWriterComponentsCount, GetWriterComponentsCount method [VSS], GetWriterComponentsCount method [VSS],IVssBackupComponents interface, IVssBackupComponents interface [VSS],GetWriterComponentsCount method, IVssBackupComponents.GetWriterComponentsCount, IVssBackupComponents::GetWriterComponentsCount, _win32_ivssbackupcomponents_getwritercomponentscount, base.ivssbackupcomponents_getwritercomponentscount, vsbackup/IVssBackupComponents::GetWriterComponentsCount
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
 - IVssBackupComponents::GetWriterComponentsCount
 - vsbackup/IVssBackupComponents::GetWriterComponentsCount
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
 - IVssBackupComponents.GetWriterComponentsCount
---

# IVssBackupComponents::GetWriterComponentsCount


## -description

The 
<b>GetWriterComponentsCount</b> method returns the number of writers whose components have been added to a requester's Backup Components Document.

## -parameters

### -param pcComponents [out]

Pointer to the returned number of writers whose components have been stored.

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
Successfully returned the number of components.

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

The count returned by 
<b>GetWriterComponentsCount</b> is that of writers that have had at least one of their components stored in the Backup Components Document by earlier calls to 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addcomponent">IVssBackupComponents::AddComponent</a>.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>