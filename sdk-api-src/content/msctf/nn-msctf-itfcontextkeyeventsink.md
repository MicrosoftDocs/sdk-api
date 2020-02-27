---
UID: NN:msctf.ITfContextKeyEventSink
title: ITfContextKeyEventSink (msctf.h)
description: The ITfContextKeyEventSink interface is implemented by a text service to receive keyboard event notifications that occur in an input context.
old-location: tsf\itfcontextkeyeventsink.htm
tech.root: TSF
ms.assetid: 26fc5d8a-e24e-414e-a355-c1f89251f6bd
ms.date: 12/05/2018
ms.keywords: ITfContextKeyEventSink, ITfContextKeyEventSink interface [Text Services Framework], ITfContextKeyEventSink interface [Text Services Framework],described, _tsf_itfcontextkeyeventsink_ref, msctf/ITfContextKeyEventSink, tsf.itfcontextkeyeventsink
f1_keywords:
- msctf/ITfContextKeyEventSink
dev_langs:
- c++
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
req.dll: Mscandui.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mscandui.dll
api_name:
- ITfContextKeyEventSink
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfContextKeyEventSink interface


## -description


The <b>ITfContextKeyEventSink</b> interface is implemented by a text service to receive keyboard event notifications that occur in an input context. This keyboard event sink differs from the <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfkeyeventsink">ITfKeyEventSink</a> keyboard event sink in that the keyboard events are passed to <b>ITfContextKeyEventSink</b> after having been preprocessed by the <b>ITfKeyEventSink</b> event sink. Preserved key events and filtered key events are not passed to the <b>ITfContextKeyEventSink</b> event sink.

This event sink is installed by <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a> with IID_ITfContextKeyEventSink.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfContextKeyEventSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfContextKeyEventSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfContextKeyEventSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextkeyeventsink-onkeydown">OnKeyDown</a>
</td>
<td align="left" width="63%">
Called when a key down event occurs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextkeyeventsink-onkeyup">OnKeyUp</a>
</td>
<td align="left" width="63%">
Called when a key up event occurs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextkeyeventsink-ontestkeydown">OnTestKeyDown</a>
</td>
<td align="left" width="63%">
Called to determine if a text service will handle a key down event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextkeyeventsink-ontestkeyup">OnTestKeyUp</a>
</td>
<td align="left" width="63%">
Called to determine if a text service will handle a key up event.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfsource">ITfSource
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

