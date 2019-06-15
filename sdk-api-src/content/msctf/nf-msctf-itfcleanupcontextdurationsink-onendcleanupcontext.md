---
UID: NF:msctf.ITfCleanupContextDurationSink.OnEndCleanupContext
title: ITfCleanupContextDurationSink::OnEndCleanupContext (msctf.h)
author: windows-sdk-content
description: ITfCleanupContextDurationSink::OnEndCleanupContext method
old-location: tsf\itfcleanupcontextdurationsink_onendcleanupcontext.htm
tech.root: TSF
ms.assetid: d7af4584-9c77-40cd-a83d-7b6fd3945b17
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfCleanupContextDurationSink interface [Text Services Framework],OnEndCleanupContext method, ITfCleanupContextDurationSink.OnEndCleanupContext, ITfCleanupContextDurationSink::OnEndCleanupContext, OnEndCleanupContext, OnEndCleanupContext method [Text Services Framework], OnEndCleanupContext method [Text Services Framework],ITfCleanupContextDurationSink interface, _tsf_itfcleanupcontextdurationsink_onendcleanupcontext_ref, msctf/ITfCleanupContextDurationSink::OnEndCleanupContext, tsf.itfcleanupcontextdurationsink_onendcleanupcontext
ms.topic: method
f1_keywords: ["msctf/ITfCleanupContextDurationSink.OnEndCleanupContext"]
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
 - ITfCleanupContextDurationSink.OnEndCleanupContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfCleanupContextDurationSink::OnEndCleanupContext


## -description




## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A context cleanup occurs when:

<ul>
<li>The text service is deactivated while a context is still on the context stack. This can occur when the active text service is changed or when the active language changes while the text service is active.</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-deactivate">ITfThreadMgr::Deactivate
            </a> is called while a context is still on the context stack.</li>
</ul>

<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcleanupcontextdurationsink-onstartcleanupcontext">ITfCleanupContextDurationSink::OnStartCleanupContext
        </a> is called just before the TSF manager begins making <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext">ITfCleanupContextSink::OnCleanupContext</a> notifications. When all of the OnCleanupContext notifications complete, the TSF manager calls <b>OnEndCleanupContext</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcleanupcontextdurationsink">ITfCleanupContextDurationSink</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcleanupcontextdurationsink-onstartcleanupcontext">ITfCleanupContextDurationSink::OnStartCleanupContext
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext">ITfCleanupContextSink::OnCleanupContext
      </a>
 

 

