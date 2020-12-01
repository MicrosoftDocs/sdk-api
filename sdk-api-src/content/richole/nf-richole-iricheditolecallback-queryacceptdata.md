---
UID: NF:richole.IRichEditOleCallback.QueryAcceptData
title: IRichEditOleCallback::QueryAcceptData (richole.h)
description: During a paste operation or a drag event, determines if the data that is pasted or dragged should be accepted.
helpviewer_keywords: ["IRichEditOleCallback interface [Windows Controls]","QueryAcceptData method","IRichEditOleCallback.QueryAcceptData","IRichEditOleCallback::QueryAcceptData","QueryAcceptData","QueryAcceptData method [Windows Controls]","QueryAcceptData method [Windows Controls]","IRichEditOleCallback interface","RECO_DROP","RECO_PASTE","_win32_IRichEditOleCallback_QueryAcceptData","_win32_IRichEditOleCallback_QueryAcceptData_cpp","controls.IRichEditOleCallback_QueryAcceptData","controls._win32_IRichEditOleCallback_QueryAcceptData","richole/IRichEditOleCallback::QueryAcceptData"]
old-location: controls\IRichEditOleCallback_QueryAcceptData.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditolecallback\iricheditolecallbackqueryacceptdata.htm
ms.date: 12/05/2018
ms.keywords: IRichEditOleCallback interface [Windows Controls],QueryAcceptData method, IRichEditOleCallback.QueryAcceptData, IRichEditOleCallback::QueryAcceptData, QueryAcceptData, QueryAcceptData method [Windows Controls], QueryAcceptData method [Windows Controls],IRichEditOleCallback interface, RECO_DROP, RECO_PASTE, _win32_IRichEditOleCallback_QueryAcceptData, _win32_IRichEditOleCallback_QueryAcceptData_cpp, controls.IRichEditOleCallback_QueryAcceptData, controls._win32_IRichEditOleCallback_QueryAcceptData, richole/IRichEditOleCallback::QueryAcceptData
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
 - IRichEditOleCallback::QueryAcceptData
 - richole/IRichEditOleCallback::QueryAcceptData
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
 - IRichEditOleCallback.QueryAcceptData
---

# IRichEditOleCallback::QueryAcceptData


## -description

During a paste operation or a drag event, determines if the data that is pasted or dragged should be accepted.

## -parameters

### -param lpdataobj

Type: <b>LPDATAOBJECT</b>

The data object being pasted or dragged.

### -param lpcfFormat

Type: <b>CLIPFORMAT*</b>

The clipboard format that will be used for the paste or drop operation. If the value pointed to by 
					<i>lpcfFormat</i> is zero, the best available format will be used. If the callback changes the value pointed to by 
					<i>lpcfFormat</i>, the rich edit control only uses that format and the operation will fail if the format is not available.

### -param reco

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

A clipboard operation flag, which can be one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RECO_DROP"></a><a id="reco_drop"></a><dl>
<dt><b>RECO_DROP</b></dt>
</dl>
</td>
<td width="60%">
Drop operation (drag-and-drop).

</td>
</tr>
<tr>
<td width="40%"><a id="RECO_PASTE"></a><a id="reco_paste"></a><dl>
<dt><b>RECO_PASTE</b></dt>
</dl>
</td>
<td width="60%">
Paste from the clipboard.

</td>
</tr>
</table>

### -param fReally

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Indicates whether the drag-drop is actually happening or if it is just a query. A nonzero value indicates the paste or drop is actually happening. A zero value indicates the operation is just a query, such as for 
					<a href="/windows/desktop/Controls/em-canpaste">EM_CANPASTE</a>.

### -param hMetaPict

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HGLOBAL</a></b>

Handle to a metafile containing the icon view of an object if <b>DVASPECT_ICON</b> is being imposed on an object by a paste special operation.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns <b>S_OK</b> on success. See Remarks.

## -remarks

 On failure, the rich edit control refuses the data and terminates the operation. Otherwise, the control checks the data itself for acceptable formats. A success code other than <b>S_OK</b> means that the callback either checked the data itself (if <i>fReally</i> is <b>FALSE</b>) or imported the data itself (if <i>fReally</i> is <b>TRUE</b>). If the application returns a success code other than <b>S_OK</b>, the control does not check the read-only state of the edit control.

## -see-also

<a href="/windows/desktop/api/richole/nn-richole-iricheditolecallback">IRichEditOleCallback</a>