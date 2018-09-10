---
UID: NN:msctf.ITfKeyTraceEventSink
title: ITfKeyTraceEventSink
author: windows-sdk-content
description: The ITfKeyTraceEventSink interface is implemented by an application or text service to receive key stroke event notifications before the event is processed by the target.
old-location: tsf\itfkeytraceeventsink.htm
tech.root: TSF
ms.assetid: 29785bae-59b8-4bbb-b899-44f6fc3e83bd
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfKeyTraceEventSink, ITfKeyTraceEventSink interface [Text Services Framework], ITfKeyTraceEventSink interface [Text Services Framework],described, _tsf_itfkeytraceeventsink_ref, msctf/ITfKeyTraceEventSink, tsf.itfkeytraceeventsink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfKeyTraceEventSink interface


## -description


The <b>ITfKeyTraceEventSink</b> interface is implemented by an application or text service to receive key stroke event notifications before the event is processed by the target. This advise sink is installed by calling the thread manager <a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink</a> method with IID_ITfKeyTraceEventSink.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfKeyTraceEventSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfKeyTraceEventSink</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/826b45cd-a1ec-406c-bf7a-685a766484e3">OnKeyTraceDown</a>
</td>
<td align="left" width="63%">
Called when a key down event occurs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b86de82-2c27-4824-91bb-39001b5a19e7">OnKeyTraceUp</a>
</td>
<td align="left" width="63%">
Called when a key up event occurs.

</td>
</tr>
</table> 


## -remarks



The difference between <b>ITfKeyTraceEventSink</b> and <a href="https://msdn.microsoft.com/5fa1344f-d8c4-40d1-99df-3c493673ad87">ITfKeyEventSink</a> events is that <b>ITfKeyTraceEventSink</b> events occur before any filtering or processing of the key event occurs. The <b>ITfKeyTraceEventSink</b> events also occur before the target application can process the key event.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT hr;
ITfSource *pSource;

hr = pThreadMgr-&gt;QueryInterface(IID_ITfSource, (LPVOID*)&amp;pSource);
if(SUCCEEDED(hr))
{
    hr = pSource-&gt;AdviseSink(IID_ITfKeyTraceEventSink, pKeyTraceEventSink, &amp;m_dwKeyTraveEventSinkCookie);
    
    pSource-&gt;Release();
}
</pre>
</td>
</tr>
</table></span></div>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT hr;
ITfSource *pSource;

hr = pThreadMgr-&gt;QueryInterface(IID_ITfSource, (LPVOID*)&amp;pSource);
if(SUCCEEDED(hr))
{
    hr = pSource-&gt;UnadviseSink(m_dwKeyTraveEventSinkCookie);
    
    pSource-&gt;Release();
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5fa1344f-d8c4-40d1-99df-3c493673ad87">ITfKeyEventSink
      </a>



<a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

