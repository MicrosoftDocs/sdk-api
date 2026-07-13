---
UID: NF:xpsobjectmodel.IXpsOMDocument.GetPageReferences
title: IXpsOMDocument::GetPageReferences (xpsobjectmodel.h)
description: Gets the IXpsOMPageReferenceCollection interface of the document, which allows virtualized access to its pages.
helpviewer_keywords: ["GetPageReferences","GetPageReferences method [XPS Documents and Packaging]","GetPageReferences method [XPS Documents and Packaging]","IXpsOMDocument interface","IXpsOMDocument interface [XPS Documents and Packaging]","GetPageReferences method","IXpsOMDocument.GetPageReferences","IXpsOMDocument::GetPageReferences","xps.ixpsomdocument_getpagereferences","xpsobjectmodel/IXpsOMDocument::GetPageReferences"]
old-location: xps\ixpsomdocument_getpagereferences.htm
tech.root: xps
ms.assetid: 65e8b20b-6a6b-4d24-86a1-b9d1833caa3c
ms.date: 12/05/2018
ms.keywords: GetPageReferences, GetPageReferences method [XPS Documents and Packaging], GetPageReferences method [XPS Documents and Packaging],IXpsOMDocument interface, IXpsOMDocument interface [XPS Documents and Packaging],GetPageReferences method, IXpsOMDocument.GetPageReferences, IXpsOMDocument::GetPageReferences, xps.ixpsomdocument_getpagereferences, xpsobjectmodel/IXpsOMDocument::GetPageReferences
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
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
 - IXpsOMDocument::GetPageReferences
 - xpsobjectmodel/IXpsOMDocument::GetPageReferences
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMDocument.GetPageReferences
---

# IXpsOMDocument::GetPageReferences


## -description

Gets the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection">IXpsOMPageReferenceCollection</a> interface of the document, which allows virtualized access to its pages.

## -parameters

### -param pageReferences [out, retval]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection">IXpsOMPageReferenceCollection</a> interface that contains a collection of page references for each page of the document. If there are no page references, the <b>IXpsOMPageReferenceCollection</b> returned in <i>pageReferences</i> will be empty and will have no elements.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pageReferences</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

To get the pages of a document, first get the list of <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference">IXpsOMPageReference</a> interfaces by calling <b>GetPageReferences</b>. Then, for each  <b>IXpsOMPageReference</b> interface, load a page by calling <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage">GetPage</a>.

If the document does not have any pages, the page reference collection returned in <i>pageReferences</i> will be empty. To get  the number of page references in the collection, call its <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereferencecollection-getcount">GetCount</a> method.

For an example of how this method can be used in a program, see <a href="/previous-versions/windows/desktop/dd372917(v=vs.85)">Navigate the XPS OM</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument">IXpsOMDocument</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference">IXpsOMPageReference</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection">IXpsOMPageReferenceCollection</a>



<a href="/previous-versions/windows/desktop/dd372917(v=vs.85)">Navigate the XPS OM</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>