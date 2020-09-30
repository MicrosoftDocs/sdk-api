---
UID: NN:msctf.ITfMouseTrackerACP
title: ITfMouseTrackerACP (msctf.h)
description: The ITfMouseTrackerACP interface is implemented by an application to support mouse event sinks.
helpviewer_keywords: ["ITfMouseTrackerACP","ITfMouseTrackerACP interface [Text Services Framework]","ITfMouseTrackerACP interface [Text Services Framework]","described","_tsf_itfmousetrackeracp_ref","msctf/ITfMouseTrackerACP","tsf.itfmousetrackeracp"]
old-location: tsf\itfmousetrackeracp.htm
tech.root: TSF
ms.assetid: 6761cf80-60b1-4c3a-8c3f-f040fab60f24
ms.date: 12/05/2018
ms.keywords: ITfMouseTrackerACP, ITfMouseTrackerACP interface [Text Services Framework], ITfMouseTrackerACP interface [Text Services Framework],described, _tsf_itfmousetrackeracp_ref, msctf/ITfMouseTrackerACP, tsf.itfmousetrackeracp
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
 - ITfMouseTrackerACP
 - msctf/ITfMouseTrackerACP
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
 - ITfMouseTrackerACP
---

# ITfMouseTrackerACP interface


## -description

The <b>ITfMouseTrackerACP</b> interface is implemented by an application to support mouse event sinks. This interface is used by the TSF manager to add and remove mouse event sinks in an ACP-based application. The TSF manager obtains this interface by calling the application's ITextStoreACP::QueryInterface with IID_ITfMouseTrackerACP.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfMouseTrackerACP</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfMouseTrackerACP</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfMouseTrackerACP</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msctf/nf-msctf-itfmousetrackeracp-advisemousesink">AdviseMouseSink</a>
</td>
<td align="left" width="63%">
Called to install a mouse event sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msctf/nf-msctf-itfmousetrackeracp-unadvisemousesink">UnadviseMouseSink</a>
</td>
<td align="left" width="63%">
Called to remove a mouse event sink.

</td>
</tr>
</table>