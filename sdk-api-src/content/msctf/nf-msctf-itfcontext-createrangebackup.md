---
UID: NF:msctf.ITfContext.CreateRangeBackup
title: ITfContext::CreateRangeBackup (msctf.h)
description: ITfContext::CreateRangeBackup method
helpviewer_keywords: ["CreateRangeBackup","CreateRangeBackup method [Text Services Framework]","CreateRangeBackup method [Text Services Framework]","ITfContext interface","ITfContext interface [Text Services Framework]","CreateRangeBackup method","ITfContext.CreateRangeBackup","ITfContext::CreateRangeBackup","_tsf_itfcontext_createrangebackup_ref","msctf/ITfContext::CreateRangeBackup","tsf.itfcontext_createrangebackup"]
old-location: tsf\itfcontext_createrangebackup.htm
tech.root: TSF
ms.assetid: c3b52170-af1b-407b-9160-1265ae3c9afc
ms.date: 12/05/2018
ms.keywords: CreateRangeBackup, CreateRangeBackup method [Text Services Framework], CreateRangeBackup method [Text Services Framework],ITfContext interface, ITfContext interface [Text Services Framework],CreateRangeBackup method, ITfContext.CreateRangeBackup, ITfContext::CreateRangeBackup, _tsf_itfcontext_createrangebackup_ref, msctf/ITfContext::CreateRangeBackup, tsf.itfcontext_createrangebackup
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfContext::CreateRangeBackup
 - msctf/ITfContext::CreateRangeBackup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfContext.CreateRangeBackup
---

# ITfContext::CreateRangeBackup


## -description

Creates a backup of a range.

## -parameters

### -param ec [in]

Contains an edit cookie that identifies the edit session. This is the value passed to <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.

### -param pRange [in]

Pointer to the <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> object to be backed up.

### -param ppBackup [out]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrangebackup">ITfRangeBackup</a> interface pointer that receives the backup of <i>pRange</i>.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The cookie in <i>ec</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The context is not on a document stack.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

## -remarks

This method creates a copy of the range that it can use to restore the data in <a href="/windows/desktop/api/msctf/nf-msctf-itfrangebackup-restore">ITfRangeBackup::Restore</a>.

## -see-also

[ITfContext interface](nn-msctf-itfcontext.md), [ITfEditSession::DoEditSession](nf-msctf-itfeditsession-doeditsession.md), [ITfRange interface](nn-msctf-itfrange.md), [ITfRangeBackup interface](nn-msctf-itfrangebackup.md), [ITfRangeBackup::Restore](nf-msctf-itfrangebackup-restore.md), [Ranges: Clones and Backups](/windows/desktop/TSF/ranges)