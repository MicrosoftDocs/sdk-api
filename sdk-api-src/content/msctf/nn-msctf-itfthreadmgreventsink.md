---
UID: NN:msctf.ITfThreadMgrEventSink
title: ITfThreadMgrEventSink
author: windows-sdk-content
description: The ITfThreadMgrEventSink interface is implemented by an application or TSF text service to receive notifications of certain thread manager events. Call the TSF manager ITfSource::AdviseSink with IID_ITfThreadMgrEventSink to install this advise sink.
old-location: tsf\itfthreadmgreventsink.htm
old-project: TSF
ms.assetid: be2a3eb1-cb17-4d8b-a44d-ccb33749c8f6
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: ITfThreadMgrEventSink, ITfThreadMgrEventSink interface [Text Services Framework], ITfThreadMgrEventSink interface [Text Services Framework],described, _tsf_itfthreadmgreventsink_ref, msctf/ITfThreadMgrEventSink, tsf.itfthreadmgreventsink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.h
api_name:
 - ITfThreadMgrEventSink
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfThreadMgrEventSink interface


## -description


The <b>ITfThreadMgrEventSink</b> interface is implemented by an application or TSF text service to receive notifications of certain thread manager events. Call the TSF manager <a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink</a> with IID_ITfThreadMgrEventSink to install this advise sink.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfThreadMgrEventSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfThreadMgrEventSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfThreadMgrEventSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18586e51-66b6-4071-88b4-9b92d5449a45">OnInitDocumentMgr</a>
</td>
<td align="left" width="63%">
Called when the first context is added to the context stack

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de07d7cf-db91-44e0-a0b2-4de26262552f">OnPopContext</a>
</td>
<td align="left" width="63%">
Called when a context is removed from the context stack

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80fbb861-1a12-4a9a-8f96-332c2f736f2d">OnPushContext</a>
</td>
<td align="left" width="63%">
Called when a context is added to the context stack

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c8f2b0a-5b56-4814-bed4-6875a09de176">OnSetFocus</a>
</td>
<td align="left" width="63%">
Called when a document view receives or loses the focus

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da4532e4-aa00-41af-8dfc-1880dc5b3b22">OnUninitDocumentMgr</a>
</td>
<td align="left" width="63%">
Called when the last context is removed from the context stack

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

