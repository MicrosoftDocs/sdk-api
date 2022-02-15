---
UID: NN:msctf.ITfCleanupContextSink
title: ITfCleanupContextSink (msctf.h)
description: The ITfCleanupContextSink interface is implemented by a text service to receive notifications when a context cleanup operation occurs. This notification sink is installed by calling ITfSourceSingle::AdviseSingleSink with IID_ITfCleanupContextSink.
helpviewer_keywords: ["ITfCleanupContextSink","ITfCleanupContextSink interface [Text Services Framework]","ITfCleanupContextSink interface [Text Services Framework]","described","_tsf_itfcleanupcontextsink_ref","msctf/ITfCleanupContextSink","tsf.itfcleanupcontextsink"]
old-location: tsf\itfcleanupcontextsink.htm
tech.root: TSF
ms.assetid: f88ebef7-2796-4076-892f-28fac6e143de
ms.date: 12/05/2018
ms.keywords: ITfCleanupContextSink, ITfCleanupContextSink interface [Text Services Framework], ITfCleanupContextSink interface [Text Services Framework],described, _tsf_itfcleanupcontextsink_ref, msctf/ITfCleanupContextSink, tsf.itfcleanupcontextsink
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
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfCleanupContextSink
 - msctf/ITfCleanupContextSink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imekrcic.dll
api_name:
 - ITfCleanupContextSink
---

# ITfCleanupContextSink interface


## -description

The <b>ITfCleanupContextSink</b> interface is implemented by a text service to receive notifications when a context cleanup operation occurs. This notification sink is installed by calling <a href="/windows/desktop/api/msctf/nf-msctf-itfsourcesingle-advisesinglesink">ITfSourceSingle::AdviseSingleSink</a> with IID_ITfCleanupContextSink.

## -inheritance

The <b>ITfCleanupContextSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfCleanupContextSink</b> also has these types of members:

## -remarks

A context cleanup occurs when:

<ul>
<li>The text service is deactivated while a context is still on the context stack. This can occur when the active text service is changed or when the active language changes while the text service is active.</li>
<li>
<a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-deactivate">ITfThreadMgr::Deactivate
            </a> is called while a context is still on the context stack.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfsourcesingle-advisesinglesink">ITfSourceSingle::AdviseSingleSink
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-deactivate">ITfThreadMgr::Deactivate
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
