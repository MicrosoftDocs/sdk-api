---
UID: NN:msctf.ITfContextComposition
title: ITfContextComposition
author: windows-sdk-content
description: The ITfContextComposition interface is implemented by the TSF manager and is used by a text service to create and manipulate compositions. An instance of this interface is provided by ITfContext::QueryInterface with IID_ITfContextComposition.
old-location: tsf\itfcontextcomposition.htm
old-project: TSF
ms.assetid: cf02c50c-dca8-47ad-b8ff-0fa3884db674
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: ITfContextComposition, ITfContextComposition interface [Text Services Framework], ITfContextComposition interface [Text Services Framework],described, _tsf_itfcontextcomposition_ref, msctf/ITfContextComposition, tsf.itfcontextcomposition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TF_DA_ATTR_INFO
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
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfContextComposition interface


## -description


The <b>ITfContextComposition</b> interface is implemented by the TSF manager and is used by a text service to create and manipulate compositions. An instance of this interface is provided by <b>ITfContext::QueryInterface</b> with IID_ITfContextComposition.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfContextComposition</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfContextComposition</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/230daf27-2655-4d67-b183-cd0f0c855298">EnumCompositions</a>
</td>
<td align="left" width="63%">
Creates an enumerator object that contains all compositions in the context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5a7bd54-3b8f-44fd-ae6e-1415cc69c49e">FindComposition</a>
</td>
<td align="left" width="63%">
Creates an enumerator object that contains all compositions that intersect a specified range of text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aab84e6c-39c7-438e-b4f0-1d174473aa02">StartComposition</a>
</td>
<td align="left" width="63%">
Creates a new composition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54182932-f749-4de0-a536-0f2f29d7664c">TakeOwnership</a>
</td>
<td align="left" width="63%">
Not currently implemented.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

