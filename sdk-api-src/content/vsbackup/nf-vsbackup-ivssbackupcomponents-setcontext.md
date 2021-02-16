---
UID: NF:vsbackup.IVssBackupComponents.SetContext
title: IVssBackupComponents::SetContext (vsbackup.h)
description: The SetContext method sets the context for subsequent shadow copy-related operations.
helpviewer_keywords: ["IVssBackupComponents interface [VSS]","SetContext method","IVssBackupComponents.SetContext","IVssBackupComponents::SetContext","SetContext","SetContext method [VSS]","SetContext method [VSS]","IVssBackupComponents interface","_win32_ivssbackupcomponents_setcontext","base.ivssbackupcomponents_setcontext","vsbackup/IVssBackupComponents::SetContext"]
old-location: base\ivssbackupcomponents_setcontext.htm
tech.root: base
ms.assetid: 0e466090-b551-44e8-a86d-75126352aa49
ms.date: 12/05/2018
ms.keywords: IVssBackupComponents interface [VSS],SetContext method, IVssBackupComponents.SetContext, IVssBackupComponents::SetContext, SetContext, SetContext method [VSS], SetContext method [VSS],IVssBackupComponents interface, _win32_ivssbackupcomponents_setcontext, base.ivssbackupcomponents_setcontext, vsbackup/IVssBackupComponents::SetContext
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
 - IVssBackupComponents::SetContext
 - vsbackup/IVssBackupComponents::SetContext
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
 - IVssBackupComponents.SetContext
---

# IVssBackupComponents::SetContext


## -description

The <b>SetContext</b> method sets the context 
    for subsequent shadow copy-related operations.

## -parameters

### -param lContext [in]

The context to be set. The context must be one of the supported values of 
      <a href="/windows/desktop/api/vss/ne-vss-vss_snapshot_context">_VSS_SNAPSHOT_CONTEXT</a> or a supported bit mask (or
      bitwise OR) of 
      <a href="/windows/desktop/api/vss/ne-vss-vss_volume_snapshot_attributes">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a> with a 
      valid <b>_VSS_SNAPSHOT_CONTEXT</b>.

## -returns

The default return value of this method is S_OK. The following are the valid return codes for this method.
     

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
Successfully set the context.

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
<dt><b>VSS_E_BAD_STATE</b></dt>
</dl>
</td>
<td width="60%">
The backup components object is not initialized, this method has been called during a restore operation, or 
        this method has not been called within the correct sequence.
       

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

The default context for VSS shadow copies is VSS_CTX_BACKUP.

<b>Windows XP:  </b>The only supported context is the default context, VSS_CTX_BACKUP. Therefore, calling 
     <b>SetContext</b> under Windows XP returns
     E_NOTIMPL.

<b>SetContext</b> can be called only once, 
    and it must be called prior to calling most VSS  functions.

For details on how the context set by 
    <b>IVssBackupComponents::SetContext</b> affects 
    how a shadow copy is created and managed, see 
    <a href="/windows/desktop/VSS/implementation-details-for-creating-shadow-copies">Implementation Details for 
    Creating Shadow Copies</a>.
   

For a complete discussion of the permitted shadow copy contexts, see 
    <a href="/windows/desktop/api/vss/ne-vss-vss_snapshot_context">_VSS_SNAPSHOT_CONTEXT</a> and 
    <a href="/windows/desktop/api/vss/ne-vss-vss_volume_snapshot_attributes">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a>.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset">IVssBackupComponents::DoSnapshotSet</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset">IVssBackupComponents::StartSnapshotSet</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_snapshot_context">_VSS_SNAPSHOT_CONTEXT</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_volume_snapshot_attributes">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a>