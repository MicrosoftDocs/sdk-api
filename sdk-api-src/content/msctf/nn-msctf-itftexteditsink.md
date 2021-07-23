---
UID: NN:msctf.ITfTextEditSink
title: ITfTextEditSink (msctf.h)
description: The ITfTextEditSink interface supports completion of an edit session that involves read/write access.
helpviewer_keywords: ["ITfTextEditSink","ITfTextEditSink interface [Text Services Framework]","ITfTextEditSink interface [Text Services Framework]","described","_tsf_itftexteditsink_ref","msctf/ITfTextEditSink","tsf.itftexteditsink"]
old-location: tsf\itftexteditsink.htm
tech.root: TSF
ms.assetid: 50f44525-eb3a-4db2-90c2-3e0c6c6146e3
ms.date: 12/05/2018
ms.keywords: ITfTextEditSink, ITfTextEditSink interface [Text Services Framework], ITfTextEditSink interface [Text Services Framework],described, _tsf_itftexteditsink_ref, msctf/ITfTextEditSink, tsf.itftexteditsink
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
req.dll: Imekrcic.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfTextEditSink
 - msctf/ITfTextEditSink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imekrcic.dll
api_name:
 - ITfTextEditSink
---

# ITfTextEditSink interface


## -description

The <b>ITfTextEditSink</b> interface supports completion of an edit session that involves read/write access. Install this advise sink by calling <a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a> with IID_ITfTextEditSink. A text service or application can optionally implement this interface.

## -inheritance

The <b>ITfTextEditSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfTextEditSink</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-requesteditsession">ITfContext::RequestEditSession
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
