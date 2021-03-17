---
UID: NF:vsbackup.IVssBackupComponents.InitializeForBackup
title: IVssBackupComponents::InitializeForBackup (vsbackup.h)
description: The InitializeForBackup method initializes the backup components metadata in preparation for backup.
helpviewer_keywords: ["IVssBackupComponents interface [VSS]","InitializeForBackup method","IVssBackupComponents.InitializeForBackup","IVssBackupComponents::InitializeForBackup","InitializeForBackup","InitializeForBackup method [VSS]","InitializeForBackup method [VSS]","IVssBackupComponents interface","_win32_ivssbackupcomponents_initializeforbackup","base.ivssbackupcomponents_initializeforbackup","vsbackup/IVssBackupComponents::InitializeForBackup"]
old-location: base\ivssbackupcomponents_initializeforbackup.htm
tech.root: base
ms.assetid: df469964-c954-4f79-b88f-a521157a0c66
ms.date: 12/05/2018
ms.keywords: IVssBackupComponents interface [VSS],InitializeForBackup method, IVssBackupComponents.InitializeForBackup, IVssBackupComponents::InitializeForBackup, InitializeForBackup, InitializeForBackup method [VSS], InitializeForBackup method [VSS],IVssBackupComponents interface, _win32_ivssbackupcomponents_initializeforbackup, base.ivssbackupcomponents_initializeforbackup, vsbackup/IVssBackupComponents::InitializeForBackup
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
 - IVssBackupComponents::InitializeForBackup
 - vsbackup/IVssBackupComponents::InitializeForBackup
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
 - IVssBackupComponents.InitializeForBackup
---

# IVssBackupComponents::InitializeForBackup


## -description

The 
<b>InitializeForBackup</b> method initializes the backup components metadata in preparation for backup.

## -parameters

### -param bstrXML [in]

Optional. During imports of transported shadow copies, this parameter must be the original document generated when creating the saved shadow copy and saved using <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-saveasxml">IVssBackupComponents::SaveAsXML</a>.

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
Successfully initialized the specified document for backup.

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

The XML document supplied to this method initializes the 
<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a> object with metadata previously stored by a call to 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-saveasxml">IVssBackupComponents::SaveAsXML</a>. Users should not tamper with this metadata document.

For more information on how to use 
<b>InitializeForBackup</b> with transportable shadow copies, see 
<a href="/windows/desktop/VSS/importing-transportable-shadow-copied-volumes">Importing Transportable Shadow Copied Volumes</a>.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-saveasxml">IVssBackupComponents::SaveAsXML</a>