---
UID: NN:msctf.ITfUIElementSink
title: ITfUIElementSink (msctf.h)
description: The ITfUIElementSink interface is implemented by an application to receive notifications when the UI element is changed.
helpviewer_keywords: ["ITfUIElementSink","ITfUIElementSink interface [Text Services Framework]","ITfUIElementSink interface [Text Services Framework]","described","_tsf_itfuielementsink_ref","msctf/ITfUIElementSink","tsf.itfuielementsink"]
old-location: tsf\itfuielementsink.htm
tech.root: TSF
ms.assetid: 8f77b3bc-2e47-4966-8030-d05a626ee00a
ms.date: 12/05/2018
ms.keywords: ITfUIElementSink, ITfUIElementSink interface [Text Services Framework], ITfUIElementSink interface [Text Services Framework],described, _tsf_itfuielementsink_ref, msctf/ITfUIElementSink, tsf.itfuielementsink
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfUIElementSink
 - msctf/ITfUIElementSink
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
 - ITfUIElementSink
---

# ITfUIElementSink interface


## -description

The <b>ITfUIElementSink</b> interface is implemented by an application to receive notifications when the UI element is changed.

## -inheritance

The <b>ITfUIElementSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfUIElementSink</b> also has these types of members:

## -remarks

To install this advise sink, obtain an <a href="/windows/desktop/api/msctf/nn-msctf-itfsource">ITfSource</a> object from an <a href="/windows/desktop/api/msctf/nn-msctf-itfuielementmgr">ITfUIElementMgr</a> object by calling <b>ITfUIElementMgr::QueryInterface</b> with IID_ ITfSource. Then call <a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a> with IID_ ITfUIElementSink.
