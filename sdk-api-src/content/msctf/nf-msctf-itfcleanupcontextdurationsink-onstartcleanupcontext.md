---
UID: NF:msctf.ITfCleanupContextDurationSink.OnStartCleanupContext
title: ITfCleanupContextDurationSink::OnStartCleanupContext (msctf.h)
author: windows-sdk-content
description: ITfCleanupContextDurationSink::OnStartCleanupContext method
old-location: tsf\itfcleanupcontextdurationsink_onstartcleanupcontext.htm
tech.root: TSF
ms.assetid: a35aa7b1-273d-47ff-a705-298393f4abd2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfCleanupContextDurationSink interface [Text Services Framework],OnStartCleanupContext method, ITfCleanupContextDurationSink.OnStartCleanupContext, ITfCleanupContextDurationSink::OnStartCleanupContext, OnStartCleanupContext, OnStartCleanupContext method [Text Services Framework], OnStartCleanupContext method [Text Services Framework],ITfCleanupContextDurationSink interface, _tsf_itfcleanupcontextdurationsink_onstartcleanupcontext_ref, msctf/ITfCleanupContextDurationSink::OnStartCleanupContext, tsf.itfcleanupcontextdurationsink_onstartcleanupcontext
ms.topic: method
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
 - ITfCleanupContextDurationSink.OnStartCleanupContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfCleanupContextDurationSink::OnStartCleanupContext


## -description




## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A context cleanup occurs when:

<ul>
<li>The text service is deactivated while a context is still on the context stack. This can occur when the active text service is changed or when the active language changes while the text service is active.</li>
<li>
<a href="https://msdn.microsoft.com/7293fbfa-c385-4713-80b2-760e54dbf4c1">ITfThreadMgr::Deactivate
            </a> is called while a context is still on the context stack.</li>
</ul>
This method is called just before the TSF manager begins making <a href="https://msdn.microsoft.com/6af597e6-f997-4b28-8994-a8dbabcaaa68">ITfCleanupContextSink::OnCleanupContext</a> notifications. When all of the OnCleanupContext notifications complete, the TSF manager calls <a href="https://msdn.microsoft.com/d7af4584-9c77-40cd-a83d-7b6fd3945b17">ITfCleanupContextDurationSink::OnEndCleanupContext</a>.




## -see-also




<a href="https://msdn.microsoft.com/2bbdc26a-5543-4de4-b347-2062be593c4b">ITfCleanupContextDurationSink</a>



<a href="https://msdn.microsoft.com/d7af4584-9c77-40cd-a83d-7b6fd3945b17">ITfCleanupContextDurationSink::OnEndCleanupContext
      </a>



<a href="https://msdn.microsoft.com/6af597e6-f997-4b28-8994-a8dbabcaaa68">ITfCleanupContextSink::OnCleanupContext
      </a>
 

 

