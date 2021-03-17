---
UID: NF:msctf.ITfMouseTracker.UnadviseMouseSink
title: ITfMouseTracker::UnadviseMouseSink (msctf.h)
description: ITfMouseTracker::UnadviseMouseSink method
helpviewer_keywords: ["ITfMouseTracker interface [Text Services Framework]","UnadviseMouseSink method","ITfMouseTracker.UnadviseMouseSink","ITfMouseTracker::UnadviseMouseSink","UnadviseMouseSink","UnadviseMouseSink method [Text Services Framework]","UnadviseMouseSink method [Text Services Framework]","ITfMouseTracker interface","_tsf_itfmousetracker_unadvisemousesink_ref","msctf/ITfMouseTracker::UnadviseMouseSink","tsf.itfmousetracker_unadvisemousesink"]
old-location: tsf\itfmousetracker_unadvisemousesink.htm
tech.root: TSF
ms.assetid: 7707b7ce-662b-43e5-ada4-ba42eec56ede
ms.date: 12/05/2018
ms.keywords: ITfMouseTracker interface [Text Services Framework],UnadviseMouseSink method, ITfMouseTracker.UnadviseMouseSink, ITfMouseTracker::UnadviseMouseSink, UnadviseMouseSink, UnadviseMouseSink method [Text Services Framework], UnadviseMouseSink method [Text Services Framework],ITfMouseTracker interface, _tsf_itfmousetracker_unadvisemousesink_ref, msctf/ITfMouseTracker::UnadviseMouseSink, tsf.itfmousetracker_unadvisemousesink
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
 - ITfMouseTracker::UnadviseMouseSink
 - msctf/ITfMouseTracker::UnadviseMouseSink
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
 - ITfMouseTracker.UnadviseMouseSink
---

# ITfMouseTracker::UnadviseMouseSink


## -description

Uninstalls a mouse event sink.

## -parameters

### -param dwCookie [in]

Specifies the mouse advise sink identifier. This value is obtained by a call to <a href="/windows/desktop/api/msctf/nf-msctf-itfmousetracker-advisemousesink">ITfMouseTracker::AdviseMouseSink</a>.

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
</table>

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfmousetracker">ITfMouseTracker</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfmousetracker-advisemousesink">ITfMouseTracker::AdviseMouseSink
      </a>