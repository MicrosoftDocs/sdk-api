---
UID: NN:msctf.ITfContextKeyEventSink
title: ITfContextKeyEventSink (msctf.h)
description: The ITfContextKeyEventSink interface is implemented by a text service to receive keyboard event notifications that occur in an input context.
helpviewer_keywords: ["ITfContextKeyEventSink","ITfContextKeyEventSink interface [Text Services Framework]","ITfContextKeyEventSink interface [Text Services Framework]","described","_tsf_itfcontextkeyeventsink_ref","msctf/ITfContextKeyEventSink","tsf.itfcontextkeyeventsink"]
old-location: tsf\itfcontextkeyeventsink.htm
tech.root: TSF
ms.assetid: 26fc5d8a-e24e-414e-a355-c1f89251f6bd
ms.date: 12/05/2018
ms.keywords: ITfContextKeyEventSink, ITfContextKeyEventSink interface [Text Services Framework], ITfContextKeyEventSink interface [Text Services Framework],described, _tsf_itfcontextkeyeventsink_ref, msctf/ITfContextKeyEventSink, tsf.itfcontextkeyeventsink
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
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfContextKeyEventSink
 - msctf/ITfContextKeyEventSink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mscandui.dll
api_name:
 - ITfContextKeyEventSink
---

# ITfContextKeyEventSink interface


## -description

The <b>ITfContextKeyEventSink</b> interface is implemented by a text service to receive keyboard event notifications that occur in an input context. This keyboard event sink differs from the <a href="/windows/desktop/api/msctf/nn-msctf-itfkeyeventsink">ITfKeyEventSink</a> keyboard event sink in that the keyboard events are passed to <b>ITfContextKeyEventSink</b> after having been preprocessed by the <b>ITfKeyEventSink</b> event sink. Preserved key events and filtered key events are not passed to the <b>ITfContextKeyEventSink</b> event sink.

This event sink is installed by <a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a> with IID_ITfContextKeyEventSink.

## -inheritance

The <b>ITfContextKeyEventSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfContextKeyEventSink</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfsource">ITfSource
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
