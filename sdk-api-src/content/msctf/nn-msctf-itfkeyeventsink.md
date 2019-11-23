---
UID: NN:msctf.ITfKeyEventSink
title: ITfKeyEventSink (msctf.h)

description: The ITfKeyEventSink interface is implemented by a text service to receive keyboard and focus event notifications. To install this event sink, call ITfKeystrokeMgr::AdviseKeyEventSink.
old-location: tsf\itfkeyeventsink.htm
tech.root: TSF
ms.assetid: 5fa1344f-d8c4-40d1-99df-3c493673ad87

ms.date: 12/05/2018
ms.keywords: ITfKeyEventSink, ITfKeyEventSink interface [Text Services Framework], ITfKeyEventSink interface [Text Services Framework],described, _tsf_itfkeyeventsink_ref, msctf/ITfKeyEventSink, tsf.itfkeyeventsink
ms.topic: interface
f1_keywords: 
 - "msctf/ITfKeyEventSink"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfKeyEventSink
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfKeyEventSink interface


## -description


The <b>ITfKeyEventSink</b> interface is implemented by a text service to receive keyboard and focus event notifications. To install this event sink, call <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-advisekeyeventsink">ITfKeystrokeMgr::AdviseKeyEventSink</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfKeyEventSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfKeyEventSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfKeyEventSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeyeventsink-onkeydown">OnKeyDown</a>
</td>
<td align="left" width="63%">
Called when a key down event occurs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeyeventsink-onkeyup">OnKeyUp</a>
</td>
<td align="left" width="63%">
Called when a key up event occurs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeyeventsink-onpreservedkey">OnPreservedKey</a>
</td>
<td align="left" width="63%">
Called when a preserved key event occurs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeyeventsink-onsetfocus">OnSetFocus</a>
</td>
<td align="left" width="63%">
Called when a TSF text service receives or loses the keyboard focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeyeventsink-ontestkeydown">OnTestKeyDown</a>
</td>
<td align="left" width="63%">
Called to determine if a text service will handle a key down event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeyeventsink-ontestkeyup">OnTestKeyUp</a>
</td>
<td align="left" width="63%">
Called to determine if a text service will handle a key up event.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-advisekeyeventsink">ITfKeystrokeMgr::AdviseKeyEventSink
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

