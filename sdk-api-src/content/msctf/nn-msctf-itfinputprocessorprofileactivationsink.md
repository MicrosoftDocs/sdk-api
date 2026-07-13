---
UID: NN:msctf.ITfInputProcessorProfileActivationSink
title: ITfInputProcessorProfileActivationSink (msctf.h)
description: The ITfInputProcessorProfileActivationSink interface is implemented by an application to receive notifications when the profile changes.
helpviewer_keywords: ["ITfInputProcessorProfileActivationSink","ITfInputProcessorProfileActivationSink interface [Text Services Framework]","ITfInputProcessorProfileActivationSink interface [Text Services Framework]","described","_tsf_itfinputprocessorprofileactivationsink_ref","msctf/ITfInputProcessorProfileActivationSink","tsf.itfinputprocessorprofileactivationsink"]
old-location: tsf\itfinputprocessorprofileactivationsink.htm
tech.root: TSF
ms.assetid: 97a6a820-8e0e-46b0-a359-da0a17fb4cae
ms.date: 12/05/2018
ms.keywords: ITfInputProcessorProfileActivationSink, ITfInputProcessorProfileActivationSink interface [Text Services Framework], ITfInputProcessorProfileActivationSink interface [Text Services Framework],described, _tsf_itfinputprocessorprofileactivationsink_ref, msctf/ITfInputProcessorProfileActivationSink, tsf.itfinputprocessorprofileactivationsink
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
 - ITfInputProcessorProfileActivationSink
 - msctf/ITfInputProcessorProfileActivationSink
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
 - ITfInputProcessorProfileActivationSink
---

# ITfInputProcessorProfileActivationSink interface


## -description

The <b>ITfInputProcessorProfileActivationSink</b> interface is implemented by an application to receive notifications when the profile changes.

## -inheritance

The <b>ITfInputProcessorProfileActivationSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfInputProcessorProfileActivationSink</b> also has these types of members:

## -remarks

To install this advise sink, obtain an <a href="/windows/desktop/api/msctf/nn-msctf-itfsource">ITfSource</a> object from an <a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgr">ITfThreadMgr</a> object by calling <b>ITfThreadMgr::QueryInterface</b> with <b>IID_ ITfSource</b>. Then call <a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a> with <b>IID_ITfInputProcessorProfileActivationSink</b>.
