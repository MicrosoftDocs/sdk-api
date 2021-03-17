---
UID: NF:txlogpub.ILog.TruncatePrefix
title: ILog::TruncatePrefix (txlogpub.h)
description: Throws away the specified prefix of the log, making it no longer retrievable.
helpviewer_keywords: ["ILog interface [COM]","TruncatePrefix method","ILog.TruncatePrefix","ILog::TruncatePrefix","TruncatePrefix","TruncatePrefix method [COM]","TruncatePrefix method [COM]","ILog interface","_com_ilog_truncateprefix","com.ilog_truncateprefix","txlogpub/ILog::TruncatePrefix"]
old-location: com\ilog_truncateprefix.htm
tech.root: com
ms.assetid: 079c05b3-19ad-401d-ad5c-1095e897799f
ms.date: 12/05/2018
ms.keywords: ILog interface [COM],TruncatePrefix method, ILog.TruncatePrefix, ILog::TruncatePrefix, TruncatePrefix, TruncatePrefix method [COM], TruncatePrefix method [COM],ILog interface, _com_ilog_truncateprefix, com.ilog_truncateprefix, txlogpub/ILog::TruncatePrefix
req.header: txlogpub.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Txlogpub.idl
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
 - ILog::TruncatePrefix
 - txlogpub/ILog::TruncatePrefix
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Txlogpub.h
api_name:
 - ILog.TruncatePrefix
---

# ILog::TruncatePrefix


## -description

Throws away the specified prefix of the log, making it no longer retrievable.

## -parameters

### -param lsnFirstToKeep [in]

The LSN of the first record not to be thrown away. If this parameter is 0, the entire log is emptied.

## -returns

This method can return the following values, as well as other <b>HRESULT</b> values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The log was successfully truncated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>lsnFirstToKeep</i> is outside the current limits of the log. See <a href="/windows/desktop/api/txlogpub/nf-txlogpub-ilog-getloglimits">ILog::GetLogLimits</a>.

</td>
</tr>
</table>

## -remarks

This request is only a hint to the log implementation. The log is free to ignore the request, or to retain more than was strictly requested. Many <a href="/windows/desktop/api/txlogpub/nn-txlogpub-ilog">ILog</a> implementations will follow this latter option.

## -see-also

<a href="/windows/desktop/api/txlogpub/nn-txlogpub-ilog">ILog</a>