---
UID: NF:msctf.ITfMouseTracker.AdviseMouseSink
title: ITfMouseTracker::AdviseMouseSink (msctf.h)
description: ITfMouseTracker::AdviseMouseSink method
helpviewer_keywords: ["AdviseMouseSink","AdviseMouseSink method [Text Services Framework]","AdviseMouseSink method [Text Services Framework]","ITfMouseTracker interface","ITfMouseTracker interface [Text Services Framework]","AdviseMouseSink method","ITfMouseTracker.AdviseMouseSink","ITfMouseTracker::AdviseMouseSink","_tsf_itfmousetracker_advisemousesink_ref","msctf/ITfMouseTracker::AdviseMouseSink","tsf.itfmousetracker_advisemousesink"]
old-location: tsf\itfmousetracker_advisemousesink.htm
tech.root: TSF
ms.assetid: d73b2b9b-8904-4507-9b32-dcb8946fb887
ms.date: 12/05/2018
ms.keywords: AdviseMouseSink, AdviseMouseSink method [Text Services Framework], AdviseMouseSink method [Text Services Framework],ITfMouseTracker interface, ITfMouseTracker interface [Text Services Framework],AdviseMouseSink method, ITfMouseTracker.AdviseMouseSink, ITfMouseTracker::AdviseMouseSink, _tsf_itfmousetracker_advisemousesink_ref, msctf/ITfMouseTracker::AdviseMouseSink, tsf.itfmousetracker_advisemousesink
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
 - ITfMouseTracker::AdviseMouseSink
 - msctf/ITfMouseTracker::AdviseMouseSink
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
 - ITfMouseTracker.AdviseMouseSink
---

# ITfMouseTracker::AdviseMouseSink


## -description

Installs a mouse event sink.

## -parameters

### -param range [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> interface that specifies the range of text that the mouse sink is installed for.

### -param pSink [in]

Pointer to the <a href="/windows/desktop/api/msctf/nn-msctf-itfmousesink">ITfMouseSink</a> interface.

### -param pdwCookie [out]

Pointer to a DWORD value that receives a cookie that identifies the mouse event sink.

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
<dt><b>TF_E_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The context object is not on a document stack.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The context owner does not support mouse event sinks.

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

When the advise sink is installed, a mouse event that occurs over the range specified by <i>range</i> will result in the mouse event sink <a href="/windows/desktop/api/msctf/nf-msctf-itfmousesink-onmouseevent">ITfMouseSink::OnMouseEvent</a> call.

The value placed in <i>pdwCookie</i> must be saved and passed to <a href="/windows/desktop/api/msctf/nf-msctf-itfmousetracker-unadvisemousesink">ITfMouseTracker::UnadviseMouseSink</a> to remove the mouse event sink.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfmousesink">ITfMouseSink
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfmousesink-onmouseevent">ITfMouseSink::OnMouseEvent
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfmousetracker">ITfMouseTracker</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfmousetracker-unadvisemousesink">ITfMouseTracker::UnadviseMouseSink
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange
      </a>