---
UID: NN:msctf.ITfCleanupContextDurationSink
title: ITfCleanupContextDurationSink (msctf.h)
description: The ITfCleanupContextDurationSink interface is implemented by a text service to receive notifications when a context cleanup operation is performed.
helpviewer_keywords: ["ITfCleanupContextDurationSink","ITfCleanupContextDurationSink interface [Text Services Framework]","ITfCleanupContextDurationSink interface [Text Services Framework]","described","_tsf_itfcleanupcontextdurationsink_ref","msctf/ITfCleanupContextDurationSink","tsf.itfcleanupcontextdurationsink"]
old-location: tsf\itfcleanupcontextdurationsink.htm
tech.root: TSF
ms.assetid: 2bbdc26a-5543-4de4-b347-2062be593c4b
ms.date: 12/05/2018
ms.keywords: ITfCleanupContextDurationSink, ITfCleanupContextDurationSink interface [Text Services Framework], ITfCleanupContextDurationSink interface [Text Services Framework],described, _tsf_itfcleanupcontextdurationsink_ref, msctf/ITfCleanupContextDurationSink, tsf.itfcleanupcontextdurationsink
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
 - ITfCleanupContextDurationSink
 - msctf/ITfCleanupContextDurationSink
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
 - ITfCleanupContextDurationSink
---

# ITfCleanupContextDurationSink interface


## -description

The <b>ITfCleanupContextDurationSink</b> interface is implemented by a text service to receive notifications when a context cleanup operation is performed. This notification sink is installed by calling <a href="/windows/desktop/api/msctf/nf-msctf-itfsourcesingle-advisesinglesink">ITfSourceSingle::AdviseSingleSink</a> with IID_ITfCleanupContextDurationSink.

## -inheritance

The <b>ITfCleanupContextDurationSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfCleanupContextDurationSink</b> also has these types of members:

## -remarks

A context cleanup occurs when:

<ul>
<li>The text service is deactivated while a context is still on the context stack. This can occur when the active text service is changed or when the active language changes while the text service is active.</li>
<li>
<a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-deactivate">ITfThreadMgr::Deactivate
            </a> is called while a context is still on the context stack.</li>
</ul>
A text service can use the notifications of this interface to prevent itself from performing any context initialization during the context cleanup operation.

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfsourcesingle-advisesinglesink">ITfSourceSingle::AdviseSingleSink
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-deactivate">ITfThreadMgr::Deactivate
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
