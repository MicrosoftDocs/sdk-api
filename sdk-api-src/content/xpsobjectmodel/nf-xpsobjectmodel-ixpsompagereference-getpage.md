---
UID: NF:xpsobjectmodel.IXpsOMPageReference.GetPage
title: IXpsOMPageReference::GetPage (xpsobjectmodel.h)
description: Gets a pointer to the IXpsOMPage interface that contains the page.
helpviewer_keywords: ["GetPage","GetPage method [XPS Documents and Packaging]","GetPage method [XPS Documents and Packaging]","IXpsOMPageReference interface","IXpsOMPageReference interface [XPS Documents and Packaging]","GetPage method","IXpsOMPageReference.GetPage","IXpsOMPageReference::GetPage","xps.ixpsompagereference_getpage","xpsobjectmodel/IXpsOMPageReference::GetPage"]
old-location: xps\ixpsompagereference_getpage.htm
tech.root: xps
ms.assetid: 0004217f-f379-4175-bbce-eea93d96f37f
ms.date: 12/05/2018
ms.keywords: GetPage, GetPage method [XPS Documents and Packaging], GetPage method [XPS Documents and Packaging],IXpsOMPageReference interface, IXpsOMPageReference interface [XPS Documents and Packaging],GetPage method, IXpsOMPageReference.GetPage, IXpsOMPageReference::GetPage, xps.ixpsompagereference_getpage, xpsobjectmodel/IXpsOMPageReference::GetPage
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
 - IXpsOMPageReference::GetPage
 - xpsobjectmodel/IXpsOMPageReference::GetPage
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
 - IXpsOMPageReference.GetPage
---

# IXpsOMPageReference::GetPage


## -description

Gets a pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a> interface that contains the page.

## -parameters

### -param page [out, retval]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a> interface of the page. If a page has not been set, a <b>NULL</b> pointer is returned.

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
<i>document</i> is <b>NULL</b>.

</td>
</tr>
</table>
 

This method calls the <a href="/previous-versions/windows/desktop/opc/packaging">Packaging</a> API. For information about the Packaging API return values, see <a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>.

## -remarks

If a page has not been set but the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage">IXpsOMPackage</a> interface that contains the page's reference has loaded from an XPS package, this method will load and return the page. If a page has not been set and the <b>IXpsOMPackage</b> interface that contains this page reference has not loaded from an XPS package, a <b>NULL</b> pointer will be returned.

Depending on the page's contents, this call might take some time to return and it might also  cause unexpected changes in  other objects in the document tree. For example, if the page has remote resource dictionary references, the remote resource dictionary might get modified.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference">IXpsOMPageReference</a>



<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-discardpage">IXpsOMPageReference::DiscardPage</a>



<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-setpage">IXpsOMPageReference::SetPage</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>