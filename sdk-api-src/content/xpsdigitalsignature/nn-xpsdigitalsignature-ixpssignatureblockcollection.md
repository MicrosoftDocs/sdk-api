---
UID: NN:xpsdigitalsignature.IXpsSignatureBlockCollection
title: IXpsSignatureBlockCollection (xpsdigitalsignature.h)
description: A collection of IXpsSignatureBlock interfaces.
helpviewer_keywords: ["IXpsSignatureBlockCollection","IXpsSignatureBlockCollection interface [XPS Documents and Packaging]","IXpsSignatureBlockCollection interface [XPS Documents and Packaging]","described","xps.ixpssignatureblockcollection","xpsdigitalsignature/IXpsSignatureBlockCollection"]
old-location: xps\ixpssignatureblockcollection.htm
tech.root: xps
ms.assetid: e8f7be84-389e-40cf-a093-83417ba184c7
ms.date: 12/05/2018
ms.keywords: IXpsSignatureBlockCollection, IXpsSignatureBlockCollection interface [XPS Documents and Packaging], IXpsSignatureBlockCollection interface [XPS Documents and Packaging],described, xps.ixpssignatureblockcollection, xpsdigitalsignature/IXpsSignatureBlockCollection
req.header: xpsdigitalsignature.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsDigitalSignature.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsSignatureBlockCollection
 - xpsdigitalsignature/IXpsSignatureBlockCollection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsdigitalsignature.h
api_name:
 - IXpsSignatureBlockCollection
---

# IXpsSignatureBlockCollection interface

## -description

A collection of <a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a> interfaces.

## -inheritance

The <b>IXpsSignatureBlockCollection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXpsSignatureBlockCollection</b> also has these types of members:

The <b>IXpsSignatureBlockCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignatureblockcollection-getat">GetAt</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a> interface pointer from a specified location in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignatureblockcollection-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of <a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a> interface pointers in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignatureblockcollection-removeat">RemoveAt</a>
</td>
<td align="left" width="63%">
Removes and releases an <a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a> interface pointer from a specified location in the collection.

</td>
</tr>
</table>

The <b>IXpsSignatureBlockCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignatureblockcollection-getat">GetAt</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a> interface pointer from a specified location in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignatureblockcollection-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of <a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a> interface pointers in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignatureblockcollection-removeat">RemoveAt</a>
</td>
<td align="left" width="63%">
Removes and releases an <a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a> interface pointer from a specified location in the collection.

</td>
</tr>
</table>

## -remarks

This interface cannot exist independently from the signature manager from which it was instantiated.

For more information about the collection methods, see  <a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock">IXpsSignatureBlock</a>



<a href="/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
