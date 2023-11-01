---
UID: NF:xpsobjectmodel.IXpsOMPage.GetBleedBox
title: IXpsOMPage::GetBleedBox (xpsobjectmodel.h)
description: Gets the dimensions of the page's bleed box.
helpviewer_keywords: ["GetBleedBox","GetBleedBox method [XPS Documents and Packaging]","GetBleedBox method [XPS Documents and Packaging]","IXpsOMPage interface","IXpsOMPage interface [XPS Documents and Packaging]","GetBleedBox method","IXpsOMPage.GetBleedBox","IXpsOMPage::GetBleedBox","xps.ixpsompage_getbleedbox","xpsobjectmodel/IXpsOMPage::GetBleedBox"]
old-location: xps\ixpsompage_getbleedbox.htm
tech.root: xps
ms.assetid: 2ce82a0e-b01c-4c1e-8907-31f51dc51f10
ms.date: 12/05/2018
ms.keywords: GetBleedBox, GetBleedBox method [XPS Documents and Packaging], GetBleedBox method [XPS Documents and Packaging],IXpsOMPage interface, IXpsOMPage interface [XPS Documents and Packaging],GetBleedBox method, IXpsOMPage.GetBleedBox, IXpsOMPage::GetBleedBox, xps.ixpsompage_getbleedbox, xpsobjectmodel/IXpsOMPage::GetBleedBox
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
 - IXpsOMPage::GetBleedBox
 - xpsobjectmodel/IXpsOMPage::GetBleedBox
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
 - IXpsOMPage.GetBleedBox
---

# IXpsOMPage::GetBleedBox


## -description

Gets the dimensions of the page's bleed box.

## -parameters

### -param bleedBox [out, retval]

The dimensions of the bleed box.

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
<i>bleedBox</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The default bleed box of a page is:

<table>
<tr>
<th>
<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_rect">XPS_RECT</a> field</th>
<th>Default value</th>
</tr>
<tr>
<td>x</td>
<td>0</td>
</tr>
<tr>
<td>y</td>
<td>0</td>
</tr>
<tr>
<td>width</td>
<td>pageDimension.width</td>
</tr>
<tr>
<td>height</td>
<td>pageDimension.height</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_rect">XPS_RECT</a>