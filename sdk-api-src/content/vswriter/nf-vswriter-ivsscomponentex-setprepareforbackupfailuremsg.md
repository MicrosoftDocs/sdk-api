---
UID: NF:vswriter.IVssComponentEx.SetPrepareForBackupFailureMsg
title: IVssComponentEx::SetPrepareForBackupFailureMsg (vswriter.h)
description: Sets a PrepareForBackup failure message string for a component.
helpviewer_keywords: ["IVssComponentEx interface","SetPrepareForBackupFailureMsg method","IVssComponentEx.SetPrepareForBackupFailureMsg","IVssComponentEx::SetPrepareForBackupFailureMsg","SetPrepareForBackupFailureMsg","SetPrepareForBackupFailureMsg method","SetPrepareForBackupFailureMsg method","IVssComponentEx interface","base.ivsscomponentex_setprepareforbackupfailuremsg","vswriter/IVssComponentEx::SetPrepareForBackupFailureMsg"]
old-location: base\ivsscomponentex_setprepareforbackupfailuremsg.htm
tech.root: base
ms.assetid: b2c48c06-8bfc-431b-aab3-89ec9b30a9a0
ms.date: 12/05/2018
ms.keywords: IVssComponentEx interface,SetPrepareForBackupFailureMsg method, IVssComponentEx.SetPrepareForBackupFailureMsg, IVssComponentEx::SetPrepareForBackupFailureMsg, SetPrepareForBackupFailureMsg, SetPrepareForBackupFailureMsg method, SetPrepareForBackupFailureMsg method,IVssComponentEx interface, base.ivsscomponentex_setprepareforbackupfailuremsg, vswriter/IVssComponentEx::SetPrepareForBackupFailureMsg
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
 - IVssComponentEx::SetPrepareForBackupFailureMsg
 - vswriter/IVssComponentEx::SetPrepareForBackupFailureMsg
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
 - IVssComponentEx.SetPrepareForBackupFailureMsg
---

# IVssComponentEx::SetPrepareForBackupFailureMsg


## -description

Sets a <a href="/windows/desktop/VSS/vssgloss-p">PrepareForBackup</a> failure message string for a component.

This method can only be called by a writer's <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparebackup">CVssWriter::OnPrepareBackup</a> method.

## -parameters

### -param wszFailureMsg [in]

The address of a caller-allocated <b>NULL</b>-terminated wide character string containing the failure message that describes an error that occurred 
      while processing a <a href="/windows/desktop/VSS/vssgloss-p">PrepareForBackup</a> 
      event.

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
The failure message was successfully set.

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
This method was not called by a writer's <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparebackup">CVssWriter::OnPrepareBackup</a> method.

</td>
</tr>
</table>

## -remarks

The failure message that is set by 
<b>SetPrepareForBackupFailureMsg</b> applies to all files in the component and any subcomponents.

## -see-also

<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparebackup">CVssWriter::OnPrepareBackup</a>



<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponentex">IVssComponentEx</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg">IVssComponentEx::GetPrepareForBackupFailureMsg</a>