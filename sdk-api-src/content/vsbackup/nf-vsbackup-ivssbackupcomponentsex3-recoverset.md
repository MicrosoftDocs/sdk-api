---
UID: NF:vsbackup.IVssBackupComponentsEx3.RecoverSet
title: IVssBackupComponentsEx3::RecoverSet (vsbackup.h)
description: Initiates a LUN resynchronization operation.
helpviewer_keywords: ["IVssBackupComponentsEx3 interface","RecoverSet method","IVssBackupComponentsEx3.RecoverSet","IVssBackupComponentsEx3::RecoverSet","RecoverSet","RecoverSet method","RecoverSet method","IVssBackupComponentsEx3 interface","base.ivssbackupcomponentsex3_recoverset","vsbackup/IVssBackupComponentsEx3::RecoverSet"]
old-location: base\ivssbackupcomponentsex3_recoverset.htm
tech.root: base
ms.assetid: 2e468527-11e7-42d8-808b-2cb2eb86e0ba
ms.date: 12/05/2018
ms.keywords: IVssBackupComponentsEx3 interface,RecoverSet method, IVssBackupComponentsEx3.RecoverSet, IVssBackupComponentsEx3::RecoverSet, RecoverSet, RecoverSet method, RecoverSet method,IVssBackupComponentsEx3 interface, base.ivssbackupcomponentsex3_recoverset, vsbackup/IVssBackupComponentsEx3::RecoverSet
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssBackupComponentsEx3::RecoverSet
 - vsbackup/IVssBackupComponentsEx3::RecoverSet
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsBackup.h
api_name:
 - IVssBackupComponentsEx3.RecoverSet
---

# IVssBackupComponentsEx3::RecoverSet


## -description

Initiates a LUN resynchronization operation. This method is supported only on Windows server operating systems.

## -parameters

### -param dwFlags [in]

A bitmask of <a href="/windows/desktop/api/vss/ne-vss-vss_recovery_options">VSS_RECOVERY_OPTIONS</a> flags that specify how the resynchronization is to be performed.

### -param ppAsync [out]

A pointer to a variable that receives an <a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> interface pointer that can be used to retrieve the status of the LUN resynchronization operation. When the operation is complete, the caller must release the interface pointer by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
The operation was successfully completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
<dt>0x80000001L</dt>
</dl>
</td>
<td width="60%">
The provider for the volume does not support LUN resynchronization.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_BAD_STATE</b></dt>
<dt>0x80042301L</dt>
</dl>
</td>
<td width="60%">
Possible reasons for this return value include:

<ul>
<li>There is no hardware provider that supports the operation.</li>
<li>The requester did not successfully add any volumes to the recovery set.</li>
<li>The method was called in WinPE or in Safe mode.</li>
<li>The caller did not call the <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore">IVssBackupComponents::InitializeForRestore</a> method before calling this method.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_LEGACY_PROVIDER</b></dt>
<dt>0x800423F7L</dt>
</dl>
</td>
<td width="60%">
This version of the hardware provider does not support this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
<dt>0x80042306L</dt>
</dl>
</td>
<td width="60%">
An unexpected provider error occurred. If this error code is returned, the error must be described in an entry in 
        the application event log, giving the user information on how to resolve the problem.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNSELECTED_VOLUME</b></dt>
<dt>0x8004232AL</dt>
</dl>
</td>
<td width="60%">
The resynchronization destination contained a volume that was not explicitly included.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_CANNOT_REVERT_DISKID</b></dt>
<dt>0x800423FEL</dt>
</dl>
</td>
<td width="60%">
The MBR signature or GPT ID for one or more disks could not be set to the intended value. Check the Application event log for more information.

</td>
</tr>
</table>

## -remarks

At the end of the resynchronization operation, by default the newly resychronized LUN will have the same disk signature that the destination LUN had before the resynchronization.

This method cannot be called in WinPE, and it cannot be called in Safe mode. Before calling this method, the caller must call <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore">IVssBackupComponents::InitializeForRestore</a> to prepare for the resynchronization.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponentsex3">IVssBackupComponentsEx3</a>