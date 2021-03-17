---
UID: NF:msctf.ITfRange.SetGravity
title: ITfRange::SetGravity (msctf.h)
description: ITfRange::SetGravity method
helpviewer_keywords: ["ITfRange interface [Text Services Framework]","SetGravity method","ITfRange.SetGravity","ITfRange::SetGravity","SetGravity","SetGravity method [Text Services Framework]","SetGravity method [Text Services Framework]","ITfRange interface","_tsf_itfrange_setgravity_ref","msctf/ITfRange::SetGravity","tsf.itfrange_setgravity"]
old-location: tsf\itfrange_setgravity.htm
tech.root: TSF
ms.assetid: f8be0458-cd14-471d-a138-0730f87374e0
ms.date: 12/05/2018
ms.keywords: ITfRange interface [Text Services Framework],SetGravity method, ITfRange.SetGravity, ITfRange::SetGravity, SetGravity, SetGravity method [Text Services Framework], SetGravity method [Text Services Framework],ITfRange interface, _tsf_itfrange_setgravity_ref, msctf/ITfRange::SetGravity, tsf.itfrange_setgravity
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
 - ITfRange::SetGravity
 - msctf/ITfRange::SetGravity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfRange.SetGravity
---

# ITfRange::SetGravity


## -description

Sets the gravity of the anchors in the object.

## -parameters

### -param ec [in]

Contains an edit cookie that identifies the edit context obtained from <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a> or <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.

### -param gStart [in]

Contains one of the <a href="/windows/win32/api/msctf/ne-msctf-tfgravity">TfGravity</a> values that specifies the gravity of the start anchor.

### -param gEnd [in]

Contains one of the <b>TfGravity</b> values that specifies the gravity of the end anchor.

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
</table>

## -see-also

<a href="/windows/desktop/TSF/ranges">Anchor Gravity</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfrange-getgravity">ITfRange::GetGravity</a>



<a href="/windows/win32/api/msctf/ne-msctf-tfgravity">TfGravity</a>