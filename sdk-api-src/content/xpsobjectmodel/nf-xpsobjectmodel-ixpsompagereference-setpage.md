---
UID: NF:xpsobjectmodel.IXpsOMPageReference.SetPage
title: IXpsOMPageReference::SetPage (xpsobjectmodel.h)
description: Sets the IXpsOMPage interface of the page reference.
helpviewer_keywords: ["IXpsOMPageReference interface [XPS Documents and Packaging]","SetPage method","IXpsOMPageReference.SetPage","IXpsOMPageReference::SetPage","SetPage","SetPage method [XPS Documents and Packaging]","SetPage method [XPS Documents and Packaging]","IXpsOMPageReference interface","xps.ixpsompagereference_setpage","xpsobjectmodel/IXpsOMPageReference::SetPage"]
old-location: xps\ixpsompagereference_setpage.htm
tech.root: xps
ms.assetid: 7d1381ad-6ac8-4ea4-99a2-8bc5d95773c7
ms.date: 12/05/2018
ms.keywords: IXpsOMPageReference interface [XPS Documents and Packaging],SetPage method, IXpsOMPageReference.SetPage, IXpsOMPageReference::SetPage, SetPage, SetPage method [XPS Documents and Packaging], SetPage method [XPS Documents and Packaging],IXpsOMPageReference interface, xps.ixpsompagereference_setpage, xpsobjectmodel/IXpsOMPageReference::SetPage
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
 - IXpsOMPageReference::SetPage
 - xpsobjectmodel/IXpsOMPageReference::SetPage
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
 - IXpsOMPageReference.SetPage
---

# IXpsOMPageReference::SetPage


## -description

Sets the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a> interface of the page reference.

## -parameters

### -param page [in]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a> interface pointer of the page.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

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
<i>page</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_NO_CUSTOM_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
<i>page</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>

## -remarks

The page added by this method can be empty or fully constructed.

 If the incoming page has references to remote dictionary objects, those objects will not be imported into the document object by this call. They must be added in a separate call to the <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-setdictionaryresource">IXpsOMPage::SetDictionaryResource</a> or <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-setdictionaryresource">IXpsOMCanvas::SetDictionaryResource</a> method.

If a page has been set, the calling method must first release that  page before calling  <b>SetPage</b> with a new page. To explain, once <b>SetPage</b> has been called with a new page, the original page cannot be discarded even if it still exists in the package.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference">IXpsOMPageReference</a>



<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-discardpage">IXpsOMPageReference::DiscardPage</a>



<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage">IXpsOMPageReference::GetPage</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>