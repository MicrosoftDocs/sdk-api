---
UID: NF:vsbackup.CreateVssBackupComponents
title: CreateVssBackupComponents function (vsbackup.h)
description: The CreateVssBackupComponents function (vsbackup.h) creates an IVssBackupComponents interface object and returns a pointer to it.
helpviewer_keywords: ["CreateVssBackupComponents","CreateVssBackupComponents function [VSS]","CreateVssBackupComponentsInternal","_win32_createvssbackupcomponents","base.createvssbackupcomponents","vsbackup/CreateVssBackupComponents","vsbackup/CreateVssBackupComponentsInternal"]
old-location: base\createvssbackupcomponents.htm
tech.root: base
ms.assetid: 5531e57a-49e0-42e9-abf0-e8a4849ccac6
ms.date: 08/09/2022
ms.keywords: CreateVssBackupComponents, CreateVssBackupComponents function [VSS], CreateVssBackupComponentsInternal, _win32_createvssbackupcomponents, base.createvssbackupcomponents, vsbackup/CreateVssBackupComponents, vsbackup/CreateVssBackupComponentsInternal
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
req.dll: VssApi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateVssBackupComponents
 - vsbackup/CreateVssBackupComponents
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - VssApi.dll
 - Ext-MS-Win-Fs-VssAPI-L1-1-0.dll
api_name:
 - CreateVssBackupComponents
 - CreateVssBackupComponentsInternal
---

# CreateVssBackupComponents function


## -description

The <b>CreateVssBackupComponents</b> function 
    creates an <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a> 
    interface object and returns a pointer to it.
<div class="alert"><b>Note</b>  This function is exported as  <b>CreateVssBackupComponentsInternal</b>, but you should call <b>CreateVssBackupComponents</b>, not <b>CreateVssBackupComponentsInternal</b>.</div><div> </div>

## -parameters

### -param ppBackup [out]

Doubly indirect pointer to the created 
      <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a> interface object.

## -returns

The return values listed here are in addition to the normal COM <b>HRESULT</b>s that may be returned at any time 
       from the function.

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
Successfully returned a pointer to an 
        <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a> 
        interface.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory or other system resources.

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

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. <b>E_UNEXPECTED</b> is used instead.

</td>
</tr>
</table>

## -remarks

The calling application is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> to release the 
    resources held by the returned 
    <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a> when it is no 
    longer needed.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>
