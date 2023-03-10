---
UID: NF:msctf.ITfMouseTrackerACP.AdviseMouseSink
title: ITfMouseTrackerACP::AdviseMouseSink (msctf.h)
description: ITfMouseTrackerACP::AdviseMouseSink method
helpviewer_keywords: ["AdviseMouseSink","AdviseMouseSink method [Text Services Framework]","AdviseMouseSink method [Text Services Framework]","ITfMouseTrackerACP interface","ITfMouseTrackerACP interface [Text Services Framework]","AdviseMouseSink method","ITfMouseTrackerACP.AdviseMouseSink","ITfMouseTrackerACP::AdviseMouseSink","_tsf_itfmousetrackeracp_advisemousesink_ref","msctf/ITfMouseTrackerACP::AdviseMouseSink","tsf.itfmousetrackeracp_advisemousesink"]
old-location: tsf\itfmousetrackeracp_advisemousesink.htm
tech.root: TSF
ms.assetid: 365538cd-0f18-45ce-91c2-ee3255b7fa93
ms.date: 12/05/2018
ms.keywords: AdviseMouseSink, AdviseMouseSink method [Text Services Framework], AdviseMouseSink method [Text Services Framework],ITfMouseTrackerACP interface, ITfMouseTrackerACP interface [Text Services Framework],AdviseMouseSink method, ITfMouseTrackerACP.AdviseMouseSink, ITfMouseTrackerACP::AdviseMouseSink, _tsf_itfmousetrackeracp_advisemousesink_ref, msctf/ITfMouseTrackerACP::AdviseMouseSink, tsf.itfmousetrackeracp_advisemousesink
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
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfMouseTrackerACP::AdviseMouseSink
 - msctf/ITfMouseTrackerACP::AdviseMouseSink
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
 - ITfMouseTrackerACP.AdviseMouseSink
---

# ITfMouseTrackerACP::AdviseMouseSink


## -description

Called to install a mouse event sink.

## -parameters

### -param range [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> interface that specifies the range of text that the mouse sink is installed for.

### -param pSink [in]

Pointer to the <a href="/windows/desktop/api/msctf/nn-msctf-itfmousesink">ITfMouseSink</a> interface. The application must increment this object reference count and save the interface.

### -param pdwCookie [out]

Pointer to a DWORD that receives a cookie that identifies the mouse event sink.

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
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The application does not support mouse event sinks.

</td>
</tr>
</table>

## -remarks

When this advise sink is installed, a mouse event that occurs over the range specified by <i>range</i> will result in the mouse event sink <a href="/windows/desktop/api/msctf/nf-msctf-itfmousesink-onmouseevent">ITfMouseSink::OnMouseEvent</a> method being called.

The value placed in <i>pdwCookie</i> will be saved by the caller and passed to the <a href="/windows/desktop/api/msctf/nf-msctf-itfmousetrackeracp-unadvisemousesink">ITfMouseTrackerACP::UnadviseMouseSink</a> method to remove the mouse event sink.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfmousesink">ITfMouseSink
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfmousesink-onmouseevent">ITfMouseSink::OnMouseEvent
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfmousetrackeracp">ITfMouseTrackerACP</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfmousetrackeracp-unadvisemousesink">ITfMouseTrackerACP::UnadviseMouseSink
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange
      </a>