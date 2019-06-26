---
UID: NN:msctf.ITfThreadMgrEventSink
title: ITfThreadMgrEventSink (msctf.h)
author: windows-sdk-content
description: The ITfThreadMgrEventSink interface is implemented by an application or TSF text service to receive notifications of certain thread manager events. Call the TSF manager ITfSource::AdviseSink with IID_ITfThreadMgrEventSink to install this advise sink.
old-location: tsf\itfthreadmgreventsink.htm
tech.root: TSF
ms.assetid: be2a3eb1-cb17-4d8b-a44d-ccb33749c8f6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfThreadMgrEventSink, ITfThreadMgrEventSink interface [Text Services Framework], ITfThreadMgrEventSink interface [Text Services Framework],described, _tsf_itfthreadmgreventsink_ref, msctf/ITfThreadMgrEventSink, tsf.itfthreadmgreventsink
ms.topic: interface
f1_keywords: 
 - "msctf/ITfThreadMgrEventSink"
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
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfThreadMgrEventSink interface


## -description


The <b>ITfThreadMgrEventSink</b> interface is implemented by an application or TSF text service to receive notifications of certain thread manager events. Call the TSF manager <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a> with IID_ITfThreadMgrEventSink to install this advise sink.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfThreadMgrEventSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfThreadMgrEventSink</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgreventsink-oninitdocumentmgr">OnInitDocumentMgr</a>
</td>
<td align="left" width="63%">
Called when the first context is added to the context stack

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgreventsink-onpopcontext">OnPopContext</a>
</td>
<td align="left" width="63%">
Called when a context is removed from the context stack

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgreventsink-onpushcontext">OnPushContext</a>
</td>
<td align="left" width="63%">
Called when a context is added to the context stack

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgreventsink-onsetfocus">OnSetFocus</a>
</td>
<td align="left" width="63%">
Called when a document view receives or loses the focus

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgreventsink-onuninitdocumentmgr">OnUninitDocumentMgr</a>
</td>
<td align="left" width="63%">
Called when the last context is removed from the context stack

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

