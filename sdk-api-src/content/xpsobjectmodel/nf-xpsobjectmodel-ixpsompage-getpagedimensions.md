---
UID: NF:xpsobjectmodel.IXpsOMPage.GetPageDimensions
title: IXpsOMPage::GetPageDimensions (xpsobjectmodel.h)
description: Gets the page dimensions.
helpviewer_keywords: ["GetPageDimensions","GetPageDimensions method [XPS Documents and Packaging]","GetPageDimensions method [XPS Documents and Packaging]","IXpsOMPage interface","IXpsOMPage interface [XPS Documents and Packaging]","GetPageDimensions method","IXpsOMPage.GetPageDimensions","IXpsOMPage::GetPageDimensions","xps.ixpsompage_getpagedimensions","xpsobjectmodel/IXpsOMPage::GetPageDimensions"]
old-location: xps\ixpsompage_getpagedimensions.htm
tech.root: xps
ms.assetid: 24a81c7a-f048-4347-8023-96ed85bec2a1
ms.date: 12/05/2018
ms.keywords: GetPageDimensions, GetPageDimensions method [XPS Documents and Packaging], GetPageDimensions method [XPS Documents and Packaging],IXpsOMPage interface, IXpsOMPage interface [XPS Documents and Packaging],GetPageDimensions method, IXpsOMPage.GetPageDimensions, IXpsOMPage::GetPageDimensions, xps.ixpsompage_getpagedimensions, xpsobjectmodel/IXpsOMPage::GetPageDimensions
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
 - IXpsOMPage::GetPageDimensions
 - xpsobjectmodel/IXpsOMPage::GetPageDimensions
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
 - IXpsOMPage.GetPageDimensions
---

# IXpsOMPage::GetPageDimensions


## -description

Gets the page dimensions.

## -parameters

### -param pageDimensions [out, retval]

The page dimensions.

Size is described in XPS units. There are 96 XPS units per inch.  For example, the dimensions of an 8.5" by 11.0" page are 816 by 1,056 XPS units.

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
<i>pageDimensions</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The default page size is passed to <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpage">IXpsOMObjectFactory::CreatePage</a>  in the <i>pageDimensions</i> parameter.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_size">XPS_SIZE</a>