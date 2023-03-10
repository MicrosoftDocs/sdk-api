---
UID: NF:msctf.ITfMouseTrackerACP.UnadviseMouseSink
title: ITfMouseTrackerACP::UnadviseMouseSink (msctf.h)
description: ITfMouseTrackerACP::UnadviseMouseSink method
helpviewer_keywords: ["ITfMouseTrackerACP interface [Text Services Framework]","UnadviseMouseSink method","ITfMouseTrackerACP.UnadviseMouseSink","ITfMouseTrackerACP::UnadviseMouseSink","UnadviseMouseSink","UnadviseMouseSink method [Text Services Framework]","UnadviseMouseSink method [Text Services Framework]","ITfMouseTrackerACP interface","_tsf_itfmousetrackeracp_unadvisemousesink_ref","msctf/ITfMouseTrackerACP::UnadviseMouseSink","tsf.itfmousetrackeracp_unadvisemousesink"]
old-location: tsf\itfmousetrackeracp_unadvisemousesink.htm
tech.root: TSF
ms.assetid: 6c753e09-f67a-45d6-b2f9-c08d5c05c04d
ms.date: 12/05/2018
ms.keywords: ITfMouseTrackerACP interface [Text Services Framework],UnadviseMouseSink method, ITfMouseTrackerACP.UnadviseMouseSink, ITfMouseTrackerACP::UnadviseMouseSink, UnadviseMouseSink, UnadviseMouseSink method [Text Services Framework], UnadviseMouseSink method [Text Services Framework],ITfMouseTrackerACP interface, _tsf_itfmousetrackeracp_unadvisemousesink_ref, msctf/ITfMouseTrackerACP::UnadviseMouseSink, tsf.itfmousetrackeracp_unadvisemousesink
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
 - ITfMouseTrackerACP::UnadviseMouseSink
 - msctf/ITfMouseTrackerACP::UnadviseMouseSink
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
 - ITfMouseTrackerACP.UnadviseMouseSink
---

# ITfMouseTrackerACP::UnadviseMouseSink


## -description

Called to remove a mouse event sink.

## -parameters

### -param dwCookie [in]

Specifies the mouse advise sink identifier. This value is obtained by a call to <a href="/windows/desktop/api/msctf/nf-msctf-itfmousetrackeracp-advisemousesink">ITfMouseTrackerACP::AdviseMouseSink</a>.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The application does not support mouse event sinks.

</td>
</tr>
</table>

## -remarks

The application must release the <a href="/windows/desktop/api/msctf/nn-msctf-itfmousesink">ITfMouseSink</a> supplied in the <b>ITfMouseTrackerACP::AdviseMouseSink</b> call associated with <i>dwCookie</i>.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfmousesink">ITfMouseSink
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfmousetrackeracp">ITfMouseTrackerACP</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfmousetrackeracp-advisemousesink">ITfMouseTrackerACP::AdviseMouseSink
      </a>