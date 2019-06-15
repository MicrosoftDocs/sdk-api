---
UID: NN:msctf.ITfCleanupContextDurationSink
title: ITfCleanupContextDurationSink (msctf.h)
author: windows-sdk-content
description: The ITfCleanupContextDurationSink interface is implemented by a text service to receive notifications when a context cleanup operation is performed.
old-location: tsf\itfcleanupcontextdurationsink.htm
tech.root: TSF
ms.assetid: 2bbdc26a-5543-4de4-b347-2062be593c4b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfCleanupContextDurationSink, ITfCleanupContextDurationSink interface [Text Services Framework], ITfCleanupContextDurationSink interface [Text Services Framework],described, _tsf_itfcleanupcontextdurationsink_ref, msctf/ITfCleanupContextDurationSink, tsf.itfcleanupcontextdurationsink
ms.topic: interface
f1_keywords: ["msctf/ITfCleanupContextDurationSink"]
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
req.dll: Imekrcic.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imekrcic.dll
api_name:
 - ITfCleanupContextDurationSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfCleanupContextDurationSink interface


## -description


The <b>ITfCleanupContextDurationSink</b> interface is implemented by a text service to receive notifications when a context cleanup operation is performed. This notification sink is installed by calling <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsourcesingle-advisesinglesink">ITfSourceSingle::AdviseSingleSink</a> with IID_ITfCleanupContextDurationSink.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfCleanupContextDurationSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfCleanupContextDurationSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfCleanupContextDurationSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcleanupcontextdurationsink-onendcleanupcontext">OnEndCleanupContext</a>
</td>
<td align="left" width="63%">
Called when a context cleanup operation completes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcleanupcontextdurationsink-onstartcleanupcontext">OnStartCleanupContext</a>
</td>
<td align="left" width="63%">
Called when a context cleanup operation is about to begin.

</td>
</tr>
</table> 


## -remarks



A context cleanup occurs when:

<ul>
<li>The text service is deactivated while a context is still on the context stack. This can occur when the active text service is changed or when the active language changes while the text service is active.</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-deactivate">ITfThreadMgr::Deactivate
            </a> is called while a context is still on the context stack.</li>
</ul>
A text service can use the notifications of this interface to prevent itself from performing any context initialization during the context cleanup operation.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsourcesingle-advisesinglesink">ITfSourceSingle::AdviseSingleSink
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-deactivate">ITfThreadMgr::Deactivate
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

