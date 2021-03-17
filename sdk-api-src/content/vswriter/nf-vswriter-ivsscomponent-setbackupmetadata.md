---
UID: NF:vswriter.IVssComponent.SetBackupMetadata
title: IVssComponent::SetBackupMetadata (vswriter.h)
description: The SetBackupMetadata method sets backup metadata with the component.
helpviewer_keywords: ["IVssComponent interface [VSS]","SetBackupMetadata method","IVssComponent.SetBackupMetadata","IVssComponent::SetBackupMetadata","SetBackupMetadata","SetBackupMetadata method [VSS]","SetBackupMetadata method [VSS]","IVssComponent interface","_win32_ivsscomponent_setbackupmetadata","base.ivsscomponent_setbackupmetadata","vswriter/IVssComponent::SetBackupMetadata"]
old-location: base\ivsscomponent_setbackupmetadata.htm
tech.root: base
ms.assetid: 96d0a581-87a5-4f97-b23f-08e90a805de1
ms.date: 12/05/2018
ms.keywords: IVssComponent interface [VSS],SetBackupMetadata method, IVssComponent.SetBackupMetadata, IVssComponent::SetBackupMetadata, SetBackupMetadata, SetBackupMetadata method [VSS], SetBackupMetadata method [VSS],IVssComponent interface, _win32_ivsscomponent_setbackupmetadata, base.ivsscomponent_setbackupmetadata, vswriter/IVssComponent::SetBackupMetadata
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
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
 - IVssComponent::SetBackupMetadata
 - vswriter/IVssComponent::SetBackupMetadata
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
 - IVssComponent.SetBackupMetadata
---

# IVssComponent::SetBackupMetadata


## -description

The 
    <b>SetBackupMetadata</b> method sets backup
    metadata with the component.
   

A writer can call this method only during a backup operation.

This method cannot be called while handling a 
    <a href="/windows/desktop/VSS/vssgloss-b">BackupComplete</a> (<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onbackupcomplete">CVssWriter::OnBackupComplete</a>) or 
    <a href="/windows/desktop/VSS/vssgloss-b">BackupShutdown</a> (<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onbackupshutdown">CVssWriter::OnBackupShutdown</a>) event.

## -parameters

### -param wszData [in]

A <b>NULL</b>-terminated wide character string that contains the backup metadata.

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
Successfully set the item.

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
<dt><b>VSS_E_OBJECT_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
Private metadata has already been written for this component.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_BAD_STATE</b></dt>
</dl>
</td>
<td width="60%">
This method was not called by a writer or, if called by a writer, it either was not called during a backup
        operation or was called while handling a 
        BackupComplete or 
        BackupShutdown event.
       

</td>
</tr>
</table>

## -remarks

<b>SetBackupMetadata</b> sets
    private, writer-specific metadata describing a backup operation.
   

The format need not conform to any VSS metadata specification.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getbackupmetadata">IVssComponent::GetBackupMetadata</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-setrestoremetadata">IVssComponent::SetRestoreMetadata</a>