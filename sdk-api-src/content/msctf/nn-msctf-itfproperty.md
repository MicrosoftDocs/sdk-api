---
UID: NN:msctf.ITfProperty
title: ITfProperty (msctf.h)
description: The ITfProperty interface is implemented by the TSF manager and used by a client (application or text service) to modify a property value.
old-location: tsf\itfproperty.htm
tech.root: TSF
ms.assetid: 72bd92f9-d82e-4994-82ad-0989e987903b
ms.date: 12/05/2018
ms.keywords: ITfProperty, ITfProperty interface [Text Services Framework], ITfProperty interface [Text Services Framework],described, _tsf_itfproperty_ref, msctf/ITfProperty, tsf.itfproperty
f1_keywords:
- msctf/ITfProperty
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
- ITfProperty
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfProperty interface


## -description


The <b>ITfProperty</b> interface is implemented by the TSF manager and used by a client (application or text service) to modify a property value.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfProperty</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfProperty</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfProperty</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfproperty-clear">Clear</a>
</td>
<td align="left" width="63%">
Empties the property value over the specified range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfproperty-findrange">FindRange</a>
</td>
<td align="left" width="63%">
Obtains a range that covers the text that contains a non-empty value for the property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfproperty-setvalue">SetValue</a>
</td>
<td align="left" width="63%">
Sets the value of the property for a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfproperty-setvaluestore">SetValueStore</a>
</td>
<td align="left" width="63%">
Sets the value of the property for a range of text using a property store object.

</td>
</tr>
</table> 


## -remarks



An instance of this interface is obtained in various ways, such as <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty">ITfContext::GetProperty</a> or <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next">IEnumTfProperties::Next</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next">IEnumTfProperties::Next
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty">ITfContext::GetProperty
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty">ITfReadOnlyProperty
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

