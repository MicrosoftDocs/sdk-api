---
UID: NN:msctf.ITfContextOwnerCompositionSink
title: ITfContextOwnerCompositionSink (msctf.h)
description: The ITfContextOwnerCompositionSink interface is implemented by an application to receive composition-related notifications.
old-location: tsf\itfcontextownercompositionsink.htm
tech.root: TSF
ms.assetid: 4fea0a48-df5f-4f34-a3ea-d52883f6f8b1
ms.date: 12/05/2018
ms.keywords: ITfContextOwnerCompositionSink, ITfContextOwnerCompositionSink interface [Text Services Framework], ITfContextOwnerCompositionSink interface [Text Services Framework],described, _tsf_itfcontextownercompositionsink_ref, msctf/ITfContextOwnerCompositionSink, tsf.itfcontextownercompositionsink
f1_keywords:
- msctf/ITfContextOwnerCompositionSink
dev_langs:
- c++
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
req.dll: Msimtf.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- msimtf.dll
api_name:
- ITfContextOwnerCompositionSink
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfContextOwnerCompositionSink interface


## -description


The <b>ITfContextOwnerCompositionSink</b> interface is implemented by an application to receive composition-related notifications. When the application calls <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a>, the TSF manager queries the object for this interface. If the object supports this interface, the advise sink is installed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfContextOwnerCompositionSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfContextOwnerCompositionSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfContextOwnerCompositionSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionsink-onendcomposition">OnEndComposition</a>
</td>
<td align="left" width="63%">
Called when a composition is terminated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionsink-onstartcomposition">OnStartComposition</a>
</td>
<td align="left" width="63%">
Called when a composition is started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionsink-onupdatecomposition">OnUpdateComposition</a>
</td>
<td align="left" width="63%">
Called when an existing composition is changed.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

