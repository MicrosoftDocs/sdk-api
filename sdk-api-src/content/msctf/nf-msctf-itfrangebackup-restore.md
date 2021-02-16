---
UID: NF:msctf.ITfRangeBackup.Restore
title: ITfRangeBackup::Restore (msctf.h)
description: ITfRangeBackup::Restore method
helpviewer_keywords: ["ITfRangeBackup interface [Text Services Framework]","Restore method","ITfRangeBackup.Restore","ITfRangeBackup::Restore","Restore","Restore method [Text Services Framework]","Restore method [Text Services Framework]","ITfRangeBackup interface","_tsf_itfrangebackup_restore_ref","msctf/ITfRangeBackup::Restore","tsf.itfrangebackup_restore"]
old-location: tsf\itfrangebackup_restore.htm
tech.root: TSF
ms.assetid: bb168504-34c0-4d30-826e-61926fd10a2a
ms.date: 12/05/2018
ms.keywords: ITfRangeBackup interface [Text Services Framework],Restore method, ITfRangeBackup.Restore, ITfRangeBackup::Restore, Restore, Restore method [Text Services Framework], Restore method [Text Services Framework],ITfRangeBackup interface, _tsf_itfrangebackup_restore_ref, msctf/ITfRangeBackup::Restore, tsf.itfrangebackup_restore
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
 - ITfRangeBackup::Restore
 - msctf/ITfRangeBackup::Restore
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
 - ITfRangeBackup.Restore
---

# ITfRangeBackup::Restore


## -description

Restores a specified range object into the TSF context.

## -parameters

### -param ec [in]

Contains an edit cookie that identifies the edit session. This is the value passed to <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.

### -param pRange [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> object that receives the backup information. If this parameter is <b>NULL</b>, the backup information is restored into a copy of the range originally backed up by <b>ITfContext::CreateRangeBackup</b>.

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
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The edit cookie specified by <i>ec</i> is invalid.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pRange</i> is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-createrangebackup">ITfContext::CreateRangeBackup
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrangebackup">ITfRangeBackup</a>



<a href="/windows/desktop/TSF/ranges">Ranges: Clones and Backups</a>