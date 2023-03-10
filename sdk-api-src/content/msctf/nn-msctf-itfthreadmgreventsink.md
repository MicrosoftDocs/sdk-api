---
UID: NN:msctf.ITfThreadMgrEventSink
title: ITfThreadMgrEventSink (msctf.h)
description: The ITfThreadMgrEventSink interface is implemented by an application or TSF text service to receive notifications of certain thread manager events. Call the TSF manager ITfSource::AdviseSink with IID_ITfThreadMgrEventSink to install this advise sink.
helpviewer_keywords: ["ITfThreadMgrEventSink","ITfThreadMgrEventSink interface [Text Services Framework]","ITfThreadMgrEventSink interface [Text Services Framework]","described","_tsf_itfthreadmgreventsink_ref","msctf/ITfThreadMgrEventSink","tsf.itfthreadmgreventsink"]
old-location: tsf\itfthreadmgreventsink.htm
tech.root: TSF
ms.assetid: be2a3eb1-cb17-4d8b-a44d-ccb33749c8f6
ms.date: 12/05/2018
ms.keywords: ITfThreadMgrEventSink, ITfThreadMgrEventSink interface [Text Services Framework], ITfThreadMgrEventSink interface [Text Services Framework],described, _tsf_itfthreadmgreventsink_ref, msctf/ITfThreadMgrEventSink, tsf.itfthreadmgreventsink
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfThreadMgrEventSink
 - msctf/ITfThreadMgrEventSink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.h
api_name:
 - ITfThreadMgrEventSink
---

# ITfThreadMgrEventSink interface


## -description

The <b>ITfThreadMgrEventSink</b> interface is implemented by an application or TSF text service to receive notifications of certain thread manager events. Call the TSF manager <a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a> with IID_ITfThreadMgrEventSink to install this advise sink.

## -inheritance

The <b>ITfThreadMgrEventSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfThreadMgrEventSink</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
