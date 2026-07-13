---
UID: NF:xpsobjectmodel.IXpsOMPage.GetVisuals
title: IXpsOMPage::GetVisuals (xpsobjectmodel.h)
description: Gets a pointer to an IXpsOMVisualCollection interface that contains a collection of the page's visual objects.
helpviewer_keywords: ["GetVisuals","GetVisuals method [XPS Documents and Packaging]","GetVisuals method [XPS Documents and Packaging]","IXpsOMPage interface","IXpsOMPage interface [XPS Documents and Packaging]","GetVisuals method","IXpsOMPage.GetVisuals","IXpsOMPage::GetVisuals","xps.ixpsompage_getvisuals","xpsobjectmodel/IXpsOMPage::GetVisuals"]
old-location: xps\ixpsompage_getvisuals.htm
tech.root: xps
ms.assetid: 8181513f-2a5d-4b43-aa40-7f886a8af7f7
ms.date: 12/05/2018
ms.keywords: GetVisuals, GetVisuals method [XPS Documents and Packaging], GetVisuals method [XPS Documents and Packaging],IXpsOMPage interface, IXpsOMPage interface [XPS Documents and Packaging],GetVisuals method, IXpsOMPage.GetVisuals, IXpsOMPage::GetVisuals, xps.ixpsompage_getvisuals, xpsobjectmodel/IXpsOMPage::GetVisuals
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
 - IXpsOMPage::GetVisuals
 - xpsobjectmodel/IXpsOMPage::GetVisuals
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
 - IXpsOMPage.GetVisuals
---

# IXpsOMPage::GetVisuals


## -description

Gets a pointer to an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection">IXpsOMVisualCollection</a> interface that contains a collection  of the page's visual objects.

## -parameters

### -param visuals [out, retval]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection">IXpsOMVisualCollection</a>  interface that contains a collection  of the page's visual objects.

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
<i>visuals</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>