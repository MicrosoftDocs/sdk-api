---
UID: NF:richole.IRichEditOle.GetClipboardData
title: IRichEditOle::GetClipboardData (richole.h)
description: Retrieves a clipboard object for a range in an edit control.
helpviewer_keywords: ["GetClipboardData","GetClipboardData method [Windows Controls]","GetClipboardData method [Windows Controls]","IRichEditOle interface","IRichEditOle interface [Windows Controls]","GetClipboardData method","IRichEditOle.GetClipboardData","IRichEditOle::GetClipboardData","_win32_IRichEditOle_GetClipboardData","_win32_IRichEditOle_GetClipboardData_cpp","controls.IRichEditOle_GetClipboardData","controls._win32_IRichEditOle_GetClipboardData","richole/IRichEditOle::GetClipboardData"]
old-location: controls\IRichEditOle_GetClipboardData.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditole\iricheditolegetclipboarddata.htm
ms.date: 12/05/2018
ms.keywords: GetClipboardData, GetClipboardData method [Windows Controls], GetClipboardData method [Windows Controls],IRichEditOle interface, IRichEditOle interface [Windows Controls],GetClipboardData method, IRichEditOle.GetClipboardData, IRichEditOle::GetClipboardData, _win32_IRichEditOle_GetClipboardData, _win32_IRichEditOle_GetClipboardData_cpp, controls.IRichEditOle_GetClipboardData, controls._win32_IRichEditOle_GetClipboardData, richole/IRichEditOle::GetClipboardData
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
 - IRichEditOle::GetClipboardData
 - richole/IRichEditOle::GetClipboardData
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
 - IRichEditOle.GetClipboardData
---

# IRichEditOle::GetClipboardData


## -description

Retrieves a clipboard object for a range in an edit control.

## -parameters

### -param lpchrg

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-charrange">CHARRANGE</a>*</b>

The range for which to create the clipboard object.

### -param reco

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Unused.

### -param lplpdataobj

Type: <b>LPDATAOBJECT*</b>

The <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface of the clipboard object representing the range specified in the 
					<i>lpchrg</i> parameter.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns <b>S_OK</b> on success. If the method fails, it can return one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
There was an invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not enough memory to do the operation.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/richedit/ns-richedit-charrange">CHARRANGE</a>



<a href="/windows/desktop/api/richole/nn-richole-iricheditole">IRichEditOle</a>



<b>Reference</b>