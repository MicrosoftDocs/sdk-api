---
UID: NN:msctf.ITfCompositionView
title: ITfCompositionView (msctf.h)
description: The ITfCompositionView interface is implemented by the TSF manager and used by an application to obtain data about a composition view. An instance of this interface is provided by one of the ITfContextOwnerCompositionSink methods.
helpviewer_keywords: ["ITfCompositionView","ITfCompositionView interface [Text Services Framework]","ITfCompositionView interface [Text Services Framework]","described","_tsf_itfcompositionview_ref","msctf/ITfCompositionView","tsf.itfcompositionview"]
old-location: tsf\itfcompositionview.htm
tech.root: TSF
ms.assetid: 1c8aac3e-384e-402e-aae8-11e240083603
ms.date: 12/05/2018
ms.keywords: ITfCompositionView, ITfCompositionView interface [Text Services Framework], ITfCompositionView interface [Text Services Framework],described, _tsf_itfcompositionview_ref, msctf/ITfCompositionView, tsf.itfcompositionview
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
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfCompositionView
 - msctf/ITfCompositionView
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfCompositionView
---

# ITfCompositionView interface


## -description

The <b>ITfCompositionView</b> interface is implemented by the TSF manager and used by an application to obtain data about a composition view. An instance of this interface is provided by one of the <a href="/windows/desktop/api/msctf/nn-msctf-itfcontextownercompositionsink">ITfContextOwnerCompositionSink</a> methods.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfCompositionView</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfCompositionView</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfCompositionView</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msctf/nf-msctf-itfcompositionview-getownerclsid">GetOwnerClsid</a>
</td>
<td align="left" width="63%">
Obtains the class identifier of the text service that created the composition object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msctf/nf-msctf-itfcompositionview-getrange">GetRange</a>
</td>
<td align="left" width="63%">
Obtains a range object that contains the text covered by the composition.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfcontextownercompositionsink">ITfContextOwnerCompositionSink
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>