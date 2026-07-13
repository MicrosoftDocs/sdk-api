---
UID: NN:msctf.ITfKeyTraceEventSink
title: ITfKeyTraceEventSink (msctf.h)
description: The ITfKeyTraceEventSink interface is implemented by an application or text service to receive key stroke event notifications before the event is processed by the target.
helpviewer_keywords: ["ITfKeyTraceEventSink","ITfKeyTraceEventSink interface [Text Services Framework]","ITfKeyTraceEventSink interface [Text Services Framework]","described","_tsf_itfkeytraceeventsink_ref","msctf/ITfKeyTraceEventSink","tsf.itfkeytraceeventsink"]
old-location: tsf\itfkeytraceeventsink.htm
tech.root: TSF
ms.assetid: 29785bae-59b8-4bbb-b899-44f6fc3e83bd
ms.date: 12/05/2018
ms.keywords: ITfKeyTraceEventSink, ITfKeyTraceEventSink interface [Text Services Framework], ITfKeyTraceEventSink interface [Text Services Framework],described, _tsf_itfkeytraceeventsink_ref, msctf/ITfKeyTraceEventSink, tsf.itfkeytraceeventsink
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
req.dll: Tiptsf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfKeyTraceEventSink
 - msctf/ITfKeyTraceEventSink
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
 - ITfKeyTraceEventSink
---

# ITfKeyTraceEventSink interface


## -description

The <b>ITfKeyTraceEventSink</b> interface is implemented by an application or text service to receive key stroke event notifications before the event is processed by the target. This advise sink is installed by calling the thread manager <a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a> method with IID_ITfKeyTraceEventSink.

## -inheritance

The <b>ITfKeyTraceEventSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfKeyTraceEventSink</b> also has these types of members:

## -remarks

The difference between <b>ITfKeyTraceEventSink</b> and <a href="/windows/desktop/api/msctf/nn-msctf-itfkeyeventsink">ITfKeyEventSink</a> events is that <b>ITfKeyTraceEventSink</b> events occur before any filtering or processing of the key event occurs. The <b>ITfKeyTraceEventSink</b> events also occur before the target application can process the key event.


#### Examples


```cpp

HRESULT hr;
ITfSource *pSource;

hr = pThreadMgr->QueryInterface(IID_ITfSource, (LPVOID*)&pSource);
if(SUCCEEDED(hr))
{
    hr = pSource->AdviseSink(IID_ITfKeyTraceEventSink, pKeyTraceEventSink, &m_dwKeyTraveEventSinkCookie);
    
    pSource->Release();
}

```



```cpp

HRESULT hr;
ITfSource *pSource;

hr = pThreadMgr->QueryInterface(IID_ITfSource, (LPVOID*)&pSource);
if(SUCCEEDED(hr))
{
    hr = pSource->UnadviseSink(m_dwKeyTraveEventSinkCookie);
    
    pSource->Release();
}

```

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfkeyeventsink">ITfKeyEventSink
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
