---
UID: NN:msctf.ITfCleanupContextSink
title: ITfCleanupContextSink (msctf.h)
description: The ITfCleanupContextSink interface is implemented by a text service to receive notifications when a context cleanup operation occurs. This notification sink is installed by calling ITfSourceSingle::AdviseSingleSink with IID_ITfCleanupContextSink.helpviewer_keywords: ["ITfCleanupContextSink","ITfCleanupContextSink interface [Text Services Framework]","ITfCleanupContextSink interface [Text Services Framework]","described","_tsf_itfcleanupcontextsink_ref","msctf/ITfCleanupContextSink","tsf.itfcleanupcontextsink"]
old-location: tsf\itfcleanupcontextsink.htm
tech.root: TSF
ms.assetid: f88ebef7-2796-4076-892f-28fac6e143de
ms.date: 12/05/2018
ms.keywords: ITfCleanupContextSink, ITfCleanupContextSink interface [Text Services Framework], ITfCleanupContextSink interface [Text Services Framework],described, _tsf_itfcleanupcontextsink_ref, msctf/ITfCleanupContextSink, tsf.itfcleanupcontextsink
f1_keywords:
- msctf/ITfCleanupContextSink
dev_langs:
- c++
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
- ITfCleanupContextSink
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfCleanupContextSink interface


## -description


The <b>ITfCleanupContextSink</b> interface is implemented by a text service to receive notifications when a context cleanup operation occurs. This notification sink is installed by calling <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsourcesingle-advisesinglesink">ITfSourceSingle::AdviseSingleSink</a> with IID_ITfCleanupContextSink.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfCleanupContextSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfCleanupContextSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfCleanupContextSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext">OnCleanupContext</a>
</td>
<td align="left" width="63%">
Called during a context cleanup operation.

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



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsourcesingle-advisesinglesink">ITfSourceSingle::AdviseSingleSink
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-deactivate">ITfThreadMgr::Deactivate
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

