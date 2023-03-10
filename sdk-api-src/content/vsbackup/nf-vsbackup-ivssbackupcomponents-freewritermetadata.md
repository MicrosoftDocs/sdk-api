---
UID: NF:vsbackup.IVssBackupComponents.FreeWriterMetadata
title: IVssBackupComponents::FreeWriterMetadata (vsbackup.h)
description: The FreeWriterMetadata method frees system resources allocated when IVssBackupComponents::GatherWriterMetadata was called.
helpviewer_keywords: ["FreeWriterMetadata","FreeWriterMetadata method [VSS]","FreeWriterMetadata method [VSS]","IVssBackupComponents interface","IVssBackupComponents interface [VSS]","FreeWriterMetadata method","IVssBackupComponents.FreeWriterMetadata","IVssBackupComponents::FreeWriterMetadata","_win32_ivssbackupcomponents_freewritermetadata","base.ivssbackupcomponents_freewritermetadata","vsbackup/IVssBackupComponents::FreeWriterMetadata"]
old-location: base\ivssbackupcomponents_freewritermetadata.htm
tech.root: base
ms.assetid: 888d30bd-527b-4b7b-9d31-3df0556b268f
ms.date: 12/05/2018
ms.keywords: FreeWriterMetadata, FreeWriterMetadata method [VSS], FreeWriterMetadata method [VSS],IVssBackupComponents interface, IVssBackupComponents interface [VSS],FreeWriterMetadata method, IVssBackupComponents.FreeWriterMetadata, IVssBackupComponents::FreeWriterMetadata, _win32_ivssbackupcomponents_freewritermetadata, base.ivssbackupcomponents_freewritermetadata, vsbackup/IVssBackupComponents::FreeWriterMetadata
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
 - IVssBackupComponents::FreeWriterMetadata
 - vsbackup/IVssBackupComponents::FreeWriterMetadata
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
 - IVssBackupComponents.FreeWriterMetadata
---

# IVssBackupComponents::FreeWriterMetadata


## -description

The 
<b>FreeWriterMetadata</b> method frees system resources allocated when <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata">IVssBackupComponents::GatherWriterMetadata</a> was called.



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
The writer metadata was successfully freed.

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

## -remarks

This method should never be called prior to the completion of 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata">IVssBackupComponents::GatherWriterMetadata</a>. The result of calling the method prior to completion of the metadata gather is undefined.

Once writer metadata has been freed, it cannot be recovered by the current instance of the 
<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a> interface. It will be necessary to create a new instance of 
<b>IVssBackupComponents</b>, and call the <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata">IVssBackupComponents::GatherWriterMetadata</a> method again.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata">IVssBackupComponents::GatherWriterMetadata</a>
