---
UID: NN:msctf.ITfComposition
title: ITfComposition (msctf.h)
description: The ITfComposition interface is implemented by the TSF manager and is used by a text service to obtain data about and terminate a composition. An instance of this interface is provided by the ITfContextComposition::StartComposition method.
old-location: tsf\itfcomposition.htm
tech.root: TSF
ms.assetid: b1eb5782-13e3-4cbb-8c37-ce7219d1e838
ms.date: 12/05/2018
ms.keywords: ITfComposition, ITfComposition interface [Text Services Framework], ITfComposition interface [Text Services Framework],described, _tsf_itfcomposition_ref, msctf/ITfComposition, tsf.itfcomposition
ms.topic: interface
f1_keywords:
- msctf/ITfComposition
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
req.dll: Msctf.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- msctf.dll
api_name:
- ITfComposition
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfComposition interface


## -description


The <b>ITfComposition</b> interface is implemented by the TSF manager and is used by a text service to obtain data about and terminate a <a href="https://docs.microsoft.com/windows/desktop/TSF/compositions">composition</a>. An instance of this interface is provided by the <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextcomposition-startcomposition">ITfContextComposition::StartComposition</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfComposition</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfComposition</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfComposition</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcomposition-endcomposition">EndComposition</a>
</td>
<td align="left" width="63%">
Terminates a composition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcomposition-getrange">GetRange</a>
</td>
<td align="left" width="63%">
Obtains a range object that contains the text covered by the composition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcomposition-shiftend">ShiftEnd</a>
</td>
<td align="left" width="63%">
Moves the end anchor of a composition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcomposition-shiftstart">ShiftStart</a>
</td>
<td align="left" width="63%">
Moves the start anchor of a composition.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/TSF/compositions">Compositions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextcomposition-startcomposition">ITfContextComposition::StartComposition
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

