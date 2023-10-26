---
UID: NF:xpsobjectmodel.IXpsOMVisual.GetHyperlinkNavigateUri
title: IXpsOMVisual::GetHyperlinkNavigateUri (xpsobjectmodel.h)
description: Gets a pointer to the IUri interface to which this visual object links.
helpviewer_keywords: ["GetHyperlinkNavigateUri","GetHyperlinkNavigateUri method [XPS Documents and Packaging]","GetHyperlinkNavigateUri method [XPS Documents and Packaging]","IXpsOMVisual interface","IXpsOMVisual interface [XPS Documents and Packaging]","GetHyperlinkNavigateUri method","IXpsOMVisual.GetHyperlinkNavigateUri","IXpsOMVisual::GetHyperlinkNavigateUri","xps.ixpsomvisual_gethyperlinknavigateuri","xpsobjectmodel/IXpsOMVisual::GetHyperlinkNavigateUri"]
old-location: xps\ixpsomvisual_gethyperlinknavigateuri.htm
tech.root: xps
ms.assetid: 297ddac1-8383-423a-8e47-7b4466e7e5d1
ms.date: 12/05/2018
ms.keywords: GetHyperlinkNavigateUri, GetHyperlinkNavigateUri method [XPS Documents and Packaging], GetHyperlinkNavigateUri method [XPS Documents and Packaging],IXpsOMVisual interface, IXpsOMVisual interface [XPS Documents and Packaging],GetHyperlinkNavigateUri method, IXpsOMVisual.GetHyperlinkNavigateUri, IXpsOMVisual::GetHyperlinkNavigateUri, xps.ixpsomvisual_gethyperlinknavigateuri, xpsobjectmodel/IXpsOMVisual::GetHyperlinkNavigateUri
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
 - IXpsOMVisual::GetHyperlinkNavigateUri
 - xpsobjectmodel/IXpsOMVisual::GetHyperlinkNavigateUri
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
 - IXpsOMVisual.GetHyperlinkNavigateUri
---

# IXpsOMVisual::GetHyperlinkNavigateUri


## -description

Gets a pointer to the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775038(v=vs.85)">IUri</a> interface  to which this visual object links.

## -parameters

### -param hyperlinkUri [out, retval]

A pointer to the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775038(v=vs.85)">IUri</a> interface that contains the destination URI for the link. 
				If  a URI has not been set for this object, a <b>NULL</b> pointer is returned.

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
<i>hyperlinkUri</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>