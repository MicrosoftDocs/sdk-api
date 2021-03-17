---
UID: NF:vsbackup.IVssBackupComponentsEx2.BreakSnapshotSetEx
title: IVssBackupComponentsEx2::BreakSnapshotSetEx (vsbackup.h)
description: Breaks a shadow copy set according to requester-specified options.
helpviewer_keywords: ["BreakSnapshotSetEx","BreakSnapshotSetEx method","BreakSnapshotSetEx method","IVssBackupComponentsEx2 interface","IVssBackupComponentsEx2 interface","BreakSnapshotSetEx method","IVssBackupComponentsEx2.BreakSnapshotSetEx","IVssBackupComponentsEx2::BreakSnapshotSetEx","base.ivssbackupcomponentsex2_breaksnapshotsetex","vsbackup/IVssBackupComponentsEx2::BreakSnapshotSetEx"]
old-location: base\ivssbackupcomponentsex2_breaksnapshotsetex.htm
tech.root: base
ms.assetid: 595fe295-082d-4130-9698-952df49a922e
ms.date: 12/05/2018
ms.keywords: BreakSnapshotSetEx, BreakSnapshotSetEx method, BreakSnapshotSetEx method,IVssBackupComponentsEx2 interface, IVssBackupComponentsEx2 interface,BreakSnapshotSetEx method, IVssBackupComponentsEx2.BreakSnapshotSetEx, IVssBackupComponentsEx2::BreakSnapshotSetEx, base.ivssbackupcomponentsex2_breaksnapshotsetex, vsbackup/IVssBackupComponentsEx2::BreakSnapshotSetEx
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IVssBackupComponentsEx2::BreakSnapshotSetEx
 - vsbackup/IVssBackupComponentsEx2::BreakSnapshotSetEx
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
 - IVssBackupComponentsEx2.BreakSnapshotSetEx
---

# IVssBackupComponentsEx2::BreakSnapshotSetEx


## -description

Breaks a shadow copy set according to requester-specified options.

## -parameters

### -param SnapshotSetID [in]

A shadow copy set identifier.

### -param dwBreakFlags [in]

A bitmask of <a href="/windows/desktop/api/vss/ne-vss-vss_hardware_options">_VSS_HARDWARE_OPTIONS</a> flags that specify how the shadow copy set is broken.

### -param ppAsync [out]

A pointer to a variable that receives an <a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> interface pointer that can be used to retrieve the status of the shadow copy set break operation. When the break operation is complete, the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method must be called for this interface pointer.

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
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
The shadow copy set was successfully broken.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
<dt>0x80070005L</dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient privileges or is not an administrator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
<dt>0x80070057L</dt>
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
<dt>0x8007000EL</dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_BREAK_REVERT_ID_FAILED</b></dt>
<dt>0x800423F6L</dt>
</dl>
</td>
<td width="60%">
The shadow copy set break operation failed because the MBR disk signature, the GPT disk identifier, or the GPT partition identifier of one or more of the destination LUNs could not be reverted to those of the original LUNs. If one or more original LUNs are not masked on the computer, the break operation would cause a signature collision.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
<dt>0x80042308L</dt>
</dl>
</td>
<td width="60%">
The specified shadow copy does not exist.

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
The shadow copy was created by a software provider and cannot be broken.

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

<b>BreakSnapshotSetEx</b> is similar to the <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset">IVssBackupComponents::BreakSnapshotSet</a> method, except that it has extra parameters to query status and specify how the shadow copy set is broken.

Like <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset">BreakSnapshotSet</a>, <b>BreakSnapshotSetEx</b> can be used only for shadow copies that were created by a hardware shadow copy provider.

After this method returns, the shadow copy volume is still a volume, but it is no longer a shadow copy. For more information, see <a href="/windows/desktop/VSS/breaking-shadow-copies">Breaking Shadow Copies</a>.