---
UID: NF:vsbackup.IVssBackupComponents.FreeWriterStatus
title: IVssBackupComponents::FreeWriterStatus (vsbackup.h)
description: The FreeWriterStatus method frees system resources allocated during the call to IVssBackupComponents::GatherWriterStatus.
helpviewer_keywords: ["FreeWriterStatus","FreeWriterStatus method [VSS]","FreeWriterStatus method [VSS]","IVssBackupComponents interface","IVssBackupComponents interface [VSS]","FreeWriterStatus method","IVssBackupComponents.FreeWriterStatus","IVssBackupComponents::FreeWriterStatus","_win32_ivssbackupcomponents_freewriterstatus","base.ivssbackupcomponents_freewriterstatus","vsbackup/IVssBackupComponents::FreeWriterStatus"]
old-location: base\ivssbackupcomponents_freewriterstatus.htm
tech.root: base
ms.assetid: 2bf4c575-f94d-43df-b141-94ed5a55294b
ms.date: 12/05/2018
ms.keywords: FreeWriterStatus, FreeWriterStatus method [VSS], FreeWriterStatus method [VSS],IVssBackupComponents interface, IVssBackupComponents interface [VSS],FreeWriterStatus method, IVssBackupComponents.FreeWriterStatus, IVssBackupComponents::FreeWriterStatus, _win32_ivssbackupcomponents_freewriterstatus, base.ivssbackupcomponents_freewriterstatus, vsbackup/IVssBackupComponents::FreeWriterStatus
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
 - IVssBackupComponents::FreeWriterStatus
 - vsbackup/IVssBackupComponents::FreeWriterStatus
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
 - IVssBackupComponents.FreeWriterStatus
---

# IVssBackupComponents::FreeWriterStatus


## -description

The 
<b>FreeWriterStatus</b> method frees system resources allocated during the call to <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus">IVssBackupComponents::GatherWriterStatus</a>.



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
The writer status was successfully freed.

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
</table>

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus">IVssBackupComponents::GatherWriterStatus</a>
