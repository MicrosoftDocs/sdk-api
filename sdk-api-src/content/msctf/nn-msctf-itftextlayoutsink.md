---
UID: NN:msctf.ITfTextLayoutSink
title: ITfTextLayoutSink (msctf.h)
description: The ITfTextLayoutSink interface supports the context layout change by an application. Install this advise sink by calling ITfSource::AdviseSink with IID_ITfTextLayoutSink. A text service can optionally implement this interface.
helpviewer_keywords: ["ITfTextLayoutSink","ITfTextLayoutSink interface [Text Services Framework]","ITfTextLayoutSink interface [Text Services Framework]","described","_tsf_itftextlayoutsink_ref","msctf/ITfTextLayoutSink","tsf.itftextlayoutsink"]
old-location: tsf\itftextlayoutsink.htm
tech.root: TSF
ms.assetid: 370e30a8-6eed-448a-87c7-7fd01e9973c6
ms.date: 12/05/2018
ms.keywords: ITfTextLayoutSink, ITfTextLayoutSink interface [Text Services Framework], ITfTextLayoutSink interface [Text Services Framework],described, _tsf_itftextlayoutsink_ref, msctf/ITfTextLayoutSink, tsf.itftextlayoutsink
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
req.dll: Tiptsf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfTextLayoutSink
 - msctf/ITfTextLayoutSink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tiptsf.dll
api_name:
 - ITfTextLayoutSink
---

# ITfTextLayoutSink interface


## -description

The <b>ITfTextLayoutSink</b> interface supports the context layout change by an application. Install this advise sink by calling <a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a> with IID_ITfTextLayoutSink. A text service can optionally implement this interface.

## -inheritance

The <b>ITfTextLayoutSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfTextLayoutSink</b> also has these types of members:

## -remarks

TSF does not currently support multiple views; some features of this interface are limited.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfcontextview">ITfContextView
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
