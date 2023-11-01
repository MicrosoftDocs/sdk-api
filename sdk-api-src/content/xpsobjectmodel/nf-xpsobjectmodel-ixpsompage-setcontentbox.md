---
UID: NF:xpsobjectmodel.IXpsOMPage.SetContentBox
title: IXpsOMPage::SetContentBox (xpsobjectmodel.h)
description: Sets the dimensions of the page's content box.
helpviewer_keywords: ["IXpsOMPage interface [XPS Documents and Packaging]","SetContentBox method","IXpsOMPage.SetContentBox","IXpsOMPage::SetContentBox","SetContentBox","SetContentBox method [XPS Documents and Packaging]","SetContentBox method [XPS Documents and Packaging]","IXpsOMPage interface","xps.ixpsompage_setcontentbox","xpsobjectmodel/IXpsOMPage::SetContentBox"]
old-location: xps\ixpsompage_setcontentbox.htm
tech.root: xps
ms.assetid: 5262ce99-8112-4f4f-a173-5927341b4a2e
ms.date: 12/05/2018
ms.keywords: IXpsOMPage interface [XPS Documents and Packaging],SetContentBox method, IXpsOMPage.SetContentBox, IXpsOMPage::SetContentBox, SetContentBox, SetContentBox method [XPS Documents and Packaging], SetContentBox method [XPS Documents and Packaging],IXpsOMPage interface, xps.ixpsompage_setcontentbox, xpsobjectmodel/IXpsOMPage::SetContentBox
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
 - IXpsOMPage::SetContentBox
 - xpsobjectmodel/IXpsOMPage::SetContentBox
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
 - IXpsOMPage.SetContentBox
---

# IXpsOMPage::SetContentBox


## -description

Sets the dimensions of the page's content box.

## -parameters

### -param contentBox [in]

The dimensions of the page's content box.

<table>
<tr>
<th><i>contentBox</i> field</th>
<th>Valid values</th>
</tr>
<tr>
<td><i>contentBox.width</i></td>
<td>Greater than or equal to 0.0 and less than or equal to  (pageDimensions.width - contentBox.x).</td>
</tr>
<tr>
<td><i>contentBox.height</i></td>
<td>Greater than or equal to 0.0 and less than or equal to (pageDimensions.height - contentBox.y).</td>
</tr>
<tr>
<td><i>contentBox.x</i></td>
<td>Greater than or equal to 0.0 and less than pageDimensions.width.</td>
</tr>
<tr>
<td><i>contentBox.y</i></td>
<td>Greater than or equal to 0.0 and less than pageDimensions.height.</td>
</tr>
</table>

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
<i>contentBox</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_INVALID_CONTENT_BOX</b></dt>
</dl>
</td>
<td width="60%">
The rectangle specified by <i>contentBox</i> contains one or more values that are not valid.

</td>
</tr>
</table>

## -remarks

The content box specifies where ink appears on the page.

The content box dimensions are not checked against the page dimensions until the page is serialized.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_rect">XPS_RECT</a>