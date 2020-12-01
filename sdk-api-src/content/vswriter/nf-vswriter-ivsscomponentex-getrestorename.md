---
UID: NF:vswriter.IVssComponentEx.GetRestoreName
title: IVssComponentEx::GetRestoreName (vswriter.h)
description: Obtains the logical name assigned to a component that is being restored.
helpviewer_keywords: ["GetRestoreName","GetRestoreName method","GetRestoreName method","IVssComponentEx interface","IVssComponentEx interface","GetRestoreName method","IVssComponentEx.GetRestoreName","IVssComponentEx::GetRestoreName","base.ivsscomponentex_getrestorename","vswriter/IVssComponentEx::GetRestoreName"]
old-location: base\ivsscomponentex_getrestorename.htm
tech.root: base
ms.assetid: a544bcc1-6a42-4cda-824c-2b027b8a4a6f
ms.date: 12/05/2018
ms.keywords: GetRestoreName, GetRestoreName method, GetRestoreName method,IVssComponentEx interface, IVssComponentEx interface,GetRestoreName method, IVssComponentEx.GetRestoreName, IVssComponentEx::GetRestoreName, base.ivsscomponentex_getrestorename, vswriter/IVssComponentEx::GetRestoreName
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssComponentEx::GetRestoreName
 - vswriter/IVssComponentEx::GetRestoreName
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
 - IVssComponentEx.GetRestoreName
---

# IVssComponentEx::GetRestoreName


## -description

Obtains the logical name assigned to a component that is being restored.

## -parameters

### -param pbstrName [out]

The address of a caller-allocated variable that receives a null-terminated wide character string containing the restore name for the component.

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
The operation was successful.

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
</table>

## -remarks

The <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex2-setrestorename">GetRestoreName</a> method can only be called during a restore operation.

If the call to <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex2-setrestorename">GetRestoreName</a> is successful, the caller is responsible for freeing the string that  is returned in the <i>pbstrName</i> parameter by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

A writer indicates that it supports this method by setting the <b>VSS_BS_RESTORE_RENAME</b> flag in its backup schema mask.

For more 
      information, see <a href="/windows/desktop/VSS/setting-vss-restore-options">Setting VSS Restore 
      Options</a>.

## -see-also

<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex2-setrestorename">IVssBackupComponentsEx2::SetRestoreName</a>



<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponentex">IVssComponentEx</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_backup_schema">VSS_BACKUP_SCHEMA</a>