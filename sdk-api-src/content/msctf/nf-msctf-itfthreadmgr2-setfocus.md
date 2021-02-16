---
UID: NF:msctf.ITfThreadMgr2.SetFocus
title: ITfThreadMgr2::SetFocus (msctf.h)
description: Sets the input focus to the specified document manager.
helpviewer_keywords: ["ITfThreadMgr2 interface [Text Services Framework]","SetFocus method","ITfThreadMgr2.SetFocus","ITfThreadMgr2::SetFocus","SetFocus","SetFocus method [Text Services Framework]","SetFocus method [Text Services Framework]","ITfThreadMgr2 interface","msctf/ITfThreadMgr2::SetFocus","tsf.itfthreadmgr2_setfocus"]
old-location: tsf\itfthreadmgr2_setfocus.htm
tech.root: TSF
ms.assetid: 62BC0797-668D-4CA1-8313-338FF7F40D89
ms.date: 12/05/2018
ms.keywords: ITfThreadMgr2 interface [Text Services Framework],SetFocus method, ITfThreadMgr2.SetFocus, ITfThreadMgr2::SetFocus, SetFocus, SetFocus method [Text Services Framework], SetFocus method [Text Services Framework],ITfThreadMgr2 interface, msctf/ITfThreadMgr2::SetFocus, tsf.itfthreadmgr2_setfocus
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITfThreadMgr2::SetFocus
 - msctf/ITfThreadMgr2::SetFocus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.h
api_name:
 - ITfThreadMgr2.SetFocus
---

# ITfThreadMgr2::SetFocus


## -description

Sets the input focus to the specified document manager.

## -parameters

### -param pdimFocus [in]

Pointer to a <a href="/windows/desktop/api/msctf/nn-msctf-itfdocumentmgr">ITfDocumentMgr</a> interface that receives the input focus. This parameter cannot be <b>NULL</b>.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pdimFocus</i> is invalid.

</td>
</tr>
</table>

## -remarks

The application must call this method when the document window receives the input focus. If the application associates a window with a document manager using <a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-associatefocus">ITfThreadMgr::AssociateFocus</a>, the TSF manager calls this method for the application.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgr2">ITfThreadMgr2</a>