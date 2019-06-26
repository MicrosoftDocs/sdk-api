---
UID: NN:msctf.ITfContextComposition
title: ITfContextComposition (msctf.h)
author: windows-sdk-content
description: The ITfContextComposition interface is implemented by the TSF manager and is used by a text service to create and manipulate compositions. An instance of this interface is provided by ITfContext::QueryInterface with IID_ITfContextComposition.
old-location: tsf\itfcontextcomposition.htm
tech.root: TSF
ms.assetid: cf02c50c-dca8-47ad-b8ff-0fa3884db674
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfContextComposition, ITfContextComposition interface [Text Services Framework], ITfContextComposition interface [Text Services Framework],described, _tsf_itfcontextcomposition_ref, msctf/ITfContextComposition, tsf.itfcontextcomposition
ms.topic: interface
f1_keywords: 
 - "msctf/ITfContextComposition"
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
 - ITfContextComposition
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfContextComposition interface


## -description


The <b>ITfContextComposition</b> interface is implemented by the TSF manager and is used by a text service to create and manipulate compositions. An instance of this interface is provided by <b>ITfContext::QueryInterface</b> with IID_ITfContextComposition.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfContextComposition</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfContextComposition</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfContextComposition</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextcomposition-enumcompositions">EnumCompositions</a>
</td>
<td align="left" width="63%">
Creates an enumerator object that contains all compositions in the context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextcomposition-findcomposition">FindComposition</a>
</td>
<td align="left" width="63%">
Creates an enumerator object that contains all compositions that intersect a specified range of text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextcomposition-startcomposition">StartComposition</a>
</td>
<td align="left" width="63%">
Creates a new composition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextcomposition-takeownership">TakeOwnership</a>
</td>
<td align="left" width="63%">
Not currently implemented.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

