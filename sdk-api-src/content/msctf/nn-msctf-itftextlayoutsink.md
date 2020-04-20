---
UID: NN:msctf.ITfTextLayoutSink
title: ITfTextLayoutSink (msctf.h)
description: The ITfTextLayoutSink interface supports the context layout change by an application. Install this advise sink by calling ITfSource::AdviseSink with IID_ITfTextLayoutSink. A text service can optionally implement this interface.helpviewer_keywords: ["ITfTextLayoutSink","ITfTextLayoutSink interface [Text Services Framework]","ITfTextLayoutSink interface [Text Services Framework]","described","_tsf_itftextlayoutsink_ref","msctf/ITfTextLayoutSink","tsf.itftextlayoutsink"]
old-location: tsf\itftextlayoutsink.htm
tech.root: TSF
ms.assetid: 370e30a8-6eed-448a-87c7-7fd01e9973c6
ms.date: 12/05/2018
ms.keywords: ITfTextLayoutSink, ITfTextLayoutSink interface [Text Services Framework], ITfTextLayoutSink interface [Text Services Framework],described, _tsf_itftextlayoutsink_ref, msctf/ITfTextLayoutSink, tsf.itftextlayoutsink
f1_keywords:
- msctf/ITfTextLayoutSink
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
- ITfTextLayoutSink
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfTextLayoutSink interface


## -description


The <b>ITfTextLayoutSink</b> interface supports the context layout change by an application. Install this advise sink by calling <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a> with IID_ITfTextLayoutSink. A text service can optionally implement this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfTextLayoutSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfTextLayoutSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfTextLayoutSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itftextlayoutsink-onlayoutchange">OnLayoutChange</a>
</td>
<td align="left" width="63%">
Receives a notification when the layout of a context view changes.

</td>
</tr>
</table> 


## -remarks



TSF does not currently support multiple views; some features of this interface are limited.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcontextview">ITfContextView
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

