---
UID: NF:vswriter.IVssComponent.SetBackupStamp
title: IVssComponent::SetBackupStamp (vswriter.h)
description: The SetBackupStamp method sets a string containing information indicating when a backup took place.
helpviewer_keywords: ["IVssComponent interface [VSS]","SetBackupStamp method","IVssComponent.SetBackupStamp","IVssComponent::SetBackupStamp","SetBackupStamp","SetBackupStamp method [VSS]","SetBackupStamp method [VSS]","IVssComponent interface","_win32_ivsscomponent_setbackupstamp","base.ivsscomponent_setbackupstamp","vswriter/IVssComponent::SetBackupStamp"]
old-location: base\ivsscomponent_setbackupstamp.htm
tech.root: base
ms.assetid: 54995cc9-8988-4f26-9c60-5d809a93e4e1
ms.date: 12/05/2018
ms.keywords: IVssComponent interface [VSS],SetBackupStamp method, IVssComponent.SetBackupStamp, IVssComponent::SetBackupStamp, SetBackupStamp, SetBackupStamp method [VSS], SetBackupStamp method [VSS],IVssComponent interface, _win32_ivsscomponent_setbackupstamp, base.ivsscomponent_setbackupstamp, vswriter/IVssComponent::SetBackupStamp
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
 - IVssComponent::SetBackupStamp
 - vswriter/IVssComponent::SetBackupStamp
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
 - IVssComponent.SetBackupStamp
---

# IVssComponent::SetBackupStamp


## -description

The 
<b>SetBackupStamp</b> method sets a string containing information indicating when a backup took place.

A writer can call this method only during a backup operation.

This method cannot be called while handling a 
<a href="/windows/desktop/VSS/vssgloss-b">BackupComplete</a> (<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onbackupcomplete">CVssWriter::OnBackupComplete</a>) or <a href="/windows/desktop/VSS/vssgloss-b">BackupShutdown</a> (<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onbackupshutdown">CVssWriter::OnBackupShutdown</a>) event.

## -parameters

### -param wszBackupStamp [in]

Null-terminated wide character string information indicating when a backup took place.

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
Successfully set the backup time stamp.

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
This method was not called by a writer or, if called by a writer, it either was not called during a backup operation or was called while handling a BackupComplete or BackupShutdown event.

</td>
</tr>
</table>

## -remarks

For more information about backup stamps, see <a href="/windows/desktop/VSS/writer-role-in-backing-up-complex-stores">Writer Role in Backing Up Complex Stores</a>.

The backup stamp set by 
<b>SetBackupStamp</b> applies to all files in the component and any nonselectable subcomponents it has.

Writers typically call 
<b>SetBackupStamp</b> while handling a <a href="/windows/desktop/VSS/vssgloss-p">PostSnapshot</a> event in 
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostsnapshot">CVssWriter::OnPostSnapshot</a>.

Requesters merely store the backup stamp in the Backup Components Document. They do not make direct use of the backup stamp or have to know how to interpret it.

The only use of the backup stamp that a requester makes, during a restore operation, is to make the stored time-stamp string available to a writer by using the 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp">IVssBackupComponents::SetPreviousBackupStamp</a> method.

For this reason, there are no format restrictions on the content of the backup stamp. It may contain time and date information, logical sequence numbers, or any other information that will allow a writer of the same class to determine when the last backup has taken place.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getbackupstamp">IVssComponent::GetBackupStamp</a>