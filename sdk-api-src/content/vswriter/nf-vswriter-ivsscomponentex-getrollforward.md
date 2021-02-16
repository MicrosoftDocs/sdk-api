---
UID: NF:vswriter.IVssComponentEx.GetRollForward
title: IVssComponentEx::GetRollForward (vswriter.h)
description: Obtains the roll-forward operation type for a component and obtains the restore point for a partial roll-forward operation.
helpviewer_keywords: ["GetRollForward","GetRollForward method","GetRollForward method","IVssComponentEx interface","IVssComponentEx interface","GetRollForward method","IVssComponentEx.GetRollForward","IVssComponentEx::GetRollForward","base.ivsscomponentex_getrollforward","vswriter/IVssComponentEx::GetRollForward"]
old-location: base\ivsscomponentex_getrollforward.htm
tech.root: base
ms.assetid: 4ba52c80-2229-4653-bd5b-85d9f11cd127
ms.date: 12/05/2018
ms.keywords: GetRollForward, GetRollForward method, GetRollForward method,IVssComponentEx interface, IVssComponentEx interface,GetRollForward method, IVssComponentEx.GetRollForward, IVssComponentEx::GetRollForward, base.ivsscomponentex_getrollforward, vswriter/IVssComponentEx::GetRollForward
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
 - IVssComponentEx::GetRollForward
 - vswriter/IVssComponentEx::GetRollForward
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
 - IVssComponentEx.GetRollForward
---

# IVssComponentEx::GetRollForward


## -description

Obtains the roll-forward operation type for a component and obtains the restore point for a partial roll-forward operation.

## -parameters

### -param pRollType [out]

A <a href="/windows/desktop/api/vss/ne-vss-vss_rollforward_type">VSS_ROLLFORWARD_TYPE</a> enumeration value indicating the type of roll-forward operation to be performed.

### -param pbstrPoint [out]

The address of a caller-allocated variable that receives a null-terminated wide character string specifying the roll-forward restore point.

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

The <b>GetRollForward</b> method can be called only during a restore operation.

If the call to <b>GetRollForward</b> is successful, the caller is responsible for freeing the string that  is returned in the <i>pRollType</i> parameter by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

A writer indicates that it supports this method by setting the <b>VSS_BS_ROLLFORWARD_RESTORE</b> flag in its backup schema mask.

For more 
      information, see <a href="/windows/desktop/VSS/setting-vss-restore-options">Setting VSS Restore 
      Options</a>.

## -see-also

<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex2-setrollforward">IVssBackupComponentsEx2::SetRollForward</a>



<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponentex">IVssComponentEx</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_backup_schema">VSS_BACKUP_SCHEMA</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_rollforward_type">VSS_ROLLFORWARD_TYPE</a>