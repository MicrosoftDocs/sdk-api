---
UID: NN:msctf.ITfKeyTraceEventSink
title: ITfKeyTraceEventSink (msctf.h)
description: The ITfKeyTraceEventSink interface is implemented by an application or text service to receive key stroke event notifications before the event is processed by the target.
old-location: tsf\itfkeytraceeventsink.htm
tech.root: TSF
ms.assetid: 29785bae-59b8-4bbb-b899-44f6fc3e83bd
ms.date: 12/05/2018
ms.keywords: ITfKeyTraceEventSink, ITfKeyTraceEventSink interface [Text Services Framework], ITfKeyTraceEventSink interface [Text Services Framework],described, _tsf_itfkeytraceeventsink_ref, msctf/ITfKeyTraceEventSink, tsf.itfkeytraceeventsink
ms.topic: interface
f1_keywords:
- msctf/ITfKeyTraceEventSink
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
req.dll: Tiptsf.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- tiptsf.dll
api_name:
- ITfKeyTraceEventSink
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfKeyTraceEventSink interface


## -description


The <b>ITfKeyTraceEventSink</b> interface is implemented by an application or text service to receive key stroke event notifications before the event is processed by the target. This advise sink is installed by calling the thread manager <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a> method with IID_ITfKeyTraceEventSink.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfKeyTraceEventSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfKeyTraceEventSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfKeyTraceEventSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeytraceeventsink-onkeytracedown">OnKeyTraceDown</a>
</td>
<td align="left" width="63%">
Called when a key down event occurs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeytraceeventsink-onkeytraceup">OnKeyTraceUp</a>
</td>
<td align="left" width="63%">
Called when a key up event occurs.

</td>
</tr>
</table> 


## -remarks



The difference between <b>ITfKeyTraceEventSink</b> and <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfkeyeventsink">ITfKeyEventSink</a> events is that <b>ITfKeyTraceEventSink</b> events occur before any filtering or processing of the key event occurs. The <b>ITfKeyTraceEventSink</b> events also occur before the target application can process the key event.


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




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfkeyeventsink">ITfKeyEventSink
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

