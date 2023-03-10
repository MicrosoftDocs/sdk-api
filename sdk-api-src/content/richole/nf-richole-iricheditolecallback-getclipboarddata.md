---
UID: NF:richole.IRichEditOleCallback.GetClipboardData
title: IRichEditOleCallback::GetClipboardData (richole.h)
description: Allows the client to supply its own clipboard object.
helpviewer_keywords: ["GetClipboardData","GetClipboardData method [Windows Controls]","GetClipboardData method [Windows Controls]","IRichEditOleCallback interface","IRichEditOleCallback interface [Windows Controls]","GetClipboardData method","IRichEditOleCallback.GetClipboardData","IRichEditOleCallback::GetClipboardData","RECO_COPY","RECO_CUT","_win32_IRichEditOleCallback_GetClipboardData","_win32_IRichEditOleCallback_GetClipboardData_cpp","controls.IRichEditOleCallback_GetClipboardData","controls._win32_IRichEditOleCallback_GetClipboardData","richole/IRichEditOleCallback::GetClipboardData"]
old-location: controls\IRichEditOleCallback_GetClipboardData.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditolecallback\iricheditolecallbackgetclipboarddata.htm
ms.date: 12/05/2018
ms.keywords: GetClipboardData, GetClipboardData method [Windows Controls], GetClipboardData method [Windows Controls],IRichEditOleCallback interface, IRichEditOleCallback interface [Windows Controls],GetClipboardData method, IRichEditOleCallback.GetClipboardData, IRichEditOleCallback::GetClipboardData, RECO_COPY, RECO_CUT, _win32_IRichEditOleCallback_GetClipboardData, _win32_IRichEditOleCallback_GetClipboardData_cpp, controls.IRichEditOleCallback_GetClipboardData, controls._win32_IRichEditOleCallback_GetClipboardData, richole/IRichEditOleCallback::GetClipboardData
req.header: richole.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: 
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRichEditOleCallback::GetClipboardData
 - richole/IRichEditOleCallback::GetClipboardData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - IRichEditOleCallback.GetClipboardData
---

# IRichEditOleCallback::GetClipboardData


## -description

Allows the client to supply its own clipboard object.

## -parameters

### -param lpchrg

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-charrange">CHARRANGE</a>*</b>

The clipboard object range.

### -param reco

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

The clipboard operation flag can be one of these values.


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RECO_COPY"></a><a id="reco_copy"></a><dl>
<dt><b>RECO_COPY</b></dt>
</dl>
</td>
<td width="60%">
Copy to the clipboard.

</td>
</tr>
<tr>
<td width="40%"><a id="RECO_CUT"></a><a id="reco_cut"></a><dl>
<dt><b>RECO_CUT</b></dt>
</dl>
</td>
<td width="60%">
Cut to the clipboard.

</td>
</tr>
</table>

### -param lplpdataobj

Type: <b>LPDATAOBJECT*</b>

Pointer to the pointer variable that receives the address of the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> implementation representing the range specified in the 
					<i>lpchrg</i> parameter. The value of 
					<i>lplpdataobj</i> is ignored if an error is returned.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns <b>S_OK</b> on success. If the return value is <b>E_NOTIMPL</b>, the rich edit control created its own clipboard object. If the return value is a failure other than <b>E_NOTIMPL</b>, the operation failed.

## -see-also

<a href="/windows/desktop/api/richedit/ns-richedit-charrange">CHARRANGE</a>



<a href="/windows/desktop/api/richole/nn-richole-iricheditolecallback">IRichEditOleCallback</a>



<b>Reference</b>