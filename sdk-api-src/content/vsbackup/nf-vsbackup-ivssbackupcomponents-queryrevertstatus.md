---
UID: NF:vsbackup.IVssBackupComponents.QueryRevertStatus
title: IVssBackupComponents::QueryRevertStatus (vsbackup.h)
description: Returns an IVssAsync interface pointer that can be used to determine the status of the revert operation. (IVssBackupComponents.QueryRevertStatus)
helpviewer_keywords: ["IVssBackupComponents interface [VSS]","QueryRevertStatus method","IVssBackupComponents.QueryRevertStatus","IVssBackupComponents::QueryRevertStatus","QueryRevertStatus","QueryRevertStatus method [VSS]","QueryRevertStatus method [VSS]","IVssBackupComponents interface","_win32_ivssbackupcomponents_queryrevertstatus","base.ivssbackupcomponents_queryrevertstatus","vsbackup/IVssBackupComponents::QueryRevertStatus"]
old-location: base\ivssbackupcomponents_queryrevertstatus.htm
tech.root: base
ms.assetid: f2e97723-98cb-401c-ab35-20c004f0a73d
ms.date: 12/05/2018
ms.keywords: IVssBackupComponents interface [VSS],QueryRevertStatus method, IVssBackupComponents.QueryRevertStatus, IVssBackupComponents::QueryRevertStatus, QueryRevertStatus, QueryRevertStatus method [VSS], QueryRevertStatus method [VSS],IVssBackupComponents interface, _win32_ivssbackupcomponents_queryrevertstatus, base.ivssbackupcomponents_queryrevertstatus, vsbackup/IVssBackupComponents::QueryRevertStatus
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
 - IVssBackupComponents::QueryRevertStatus
 - vsbackup/IVssBackupComponents::QueryRevertStatus
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
 - IVssBackupComponents.QueryRevertStatus
---

# IVssBackupComponents::QueryRevertStatus


## -description

The <b>QueryRevertStatus</b> method 
   returns an <a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> interface pointer that can be used 
   to determine the status of the revert operation.

## -parameters

### -param pwszVolume [in]

Null-terminated wide character string containing the name of the volume. The name must be in one of the following formats and must include a trailing backslash (\\): 
      

<ul>
<li>The path of a mounted folder, for example, Y:\MountX\</li>
<li>A drive letter, for example, D:\</li>
<li>A volume GUID path of the form \\?&#92;<i>Volume</i>{<i>GUID</i>}\ (where <i>GUID</i> identifies the volume)</li>
</ul>

### -param ppAsync [out]

Pointer to a location that will receive an <a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> 
      interface pointer that can be used to retrieve the status of the revert process. When the operation is complete, the caller must release the interface pointer by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

## -returns

This method can return one of these values.

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
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling process has insufficient privileges.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
There is an internal error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters passed is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The provider for the volume does not support revert operations.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
One of the required pointer parameters is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The <i>pwszVolume</i> parameter is not a valid volume.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_VOLUME_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Revert is not supported on this volume.

</td>
</tr>
</table>

## -remarks

The revert operation will continue even if the computer is rebooted, and cannot be canceled or undone, except 
    by restoring a backup created using another method. The 
    <a href="/windows/desktop/api/vss/nf-vss-ivssasync-querystatus">QueryStatus</a> method on the returned  
    <a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> interface cannot return 
    <b>VSS_S_ASYNC_CANCELLED</b> as the revert operation cannot be canceled after it has 
    started.

## -see-also

<a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-reverttosnapshot">IVssBackupComponents::RevertToSnapshot</a>
