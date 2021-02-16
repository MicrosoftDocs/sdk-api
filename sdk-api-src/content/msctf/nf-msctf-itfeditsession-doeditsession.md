---
UID: NF:msctf.ITfEditSession.DoEditSession
title: ITfEditSession::DoEditSession (msctf.h)
description: ITfEditSession::DoEditSession method
helpviewer_keywords: ["DoEditSession","DoEditSession method [Text Services Framework]","DoEditSession method [Text Services Framework]","ITfEditSession interface","ITfEditSession interface [Text Services Framework]","DoEditSession method","ITfEditSession.DoEditSession","ITfEditSession::DoEditSession","_tsf_itfeditsession_doeditsession_ref","msctf/ITfEditSession::DoEditSession","tsf.itfeditsession_doeditsession"]
old-location: tsf\itfeditsession_doeditsession.htm
tech.root: TSF
ms.assetid: f89b2676-9a69-492f-be8a-96e4436d594c
ms.date: 12/05/2018
ms.keywords: DoEditSession, DoEditSession method [Text Services Framework], DoEditSession method [Text Services Framework],ITfEditSession interface, ITfEditSession interface [Text Services Framework],DoEditSession method, ITfEditSession.DoEditSession, ITfEditSession::DoEditSession, _tsf_itfeditsession_doeditsession_ref, msctf/ITfEditSession::DoEditSession, tsf.itfeditsession_doeditsession
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Tipskins.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfEditSession::DoEditSession
 - msctf/ITfEditSession::DoEditSession
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tipskins.dll
api_name:
 - ITfEditSession.DoEditSession
---

# ITfEditSession::DoEditSession


## -description

Called to enable a text service to read and/or modify the contents of a context.

## -parameters

### -param ec [in]

Contains a <a href="/windows/desktop/TSF/tfeditcookie">TfEditCookie</a> value that uniquely identifies the edit session. This cookie is used to access the context with methods such as <a href="/windows/desktop/api/msctf/nf-msctf-itfrange-gettext">ITfRange::GetText</a>.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-requesteditsession">ITfContext::RequestEditSession
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfeditsession">ITfEditSession
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfrange-gettext">ITfRange::GetText</a>



<a href="/windows/desktop/TSF/tfeditcookie">TfEditCookie
      </a>