---
UID: NF:xpsobjectmodel.IXpsOMPage.SetPageDimensions
title: IXpsOMPage::SetPageDimensions (xpsobjectmodel.h)
description: Sets dimensions of the page.
helpviewer_keywords: ["IXpsOMPage interface [XPS Documents and Packaging]","SetPageDimensions method","IXpsOMPage.SetPageDimensions","IXpsOMPage::SetPageDimensions","SetPageDimensions","SetPageDimensions method [XPS Documents and Packaging]","SetPageDimensions method [XPS Documents and Packaging]","IXpsOMPage interface","pageDimensions.height","pageDimensions.width","xps.ixpsompage_setpagedimensions","xpsobjectmodel/IXpsOMPage::SetPageDimensions"]
old-location: xps\ixpsompage_setpagedimensions.htm
tech.root: xps
ms.assetid: 4ae0a584-afa2-4288-82f8-c52c46de390f
ms.date: 12/05/2018
ms.keywords: IXpsOMPage interface [XPS Documents and Packaging],SetPageDimensions method, IXpsOMPage.SetPageDimensions, IXpsOMPage::SetPageDimensions, SetPageDimensions, SetPageDimensions method [XPS Documents and Packaging], SetPageDimensions method [XPS Documents and Packaging],IXpsOMPage interface, pageDimensions.height, pageDimensions.width, xps.ixpsompage_setpagedimensions, xpsobjectmodel/IXpsOMPage::SetPageDimensions
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
 - IXpsOMPage::SetPageDimensions
 - xpsobjectmodel/IXpsOMPage::SetPageDimensions
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
 - IXpsOMPage.SetPageDimensions
---

# IXpsOMPage::SetPageDimensions


## -description

Sets dimensions of the page.

## -parameters

### -param pageDimensions [in]

Dimensions of the page.

Size is described in XPS units. There are 96 XPS units per inch.  For example, the dimensions of an 8.5" by 11.0" page are 816 by 1,056 XPS units.

The  <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_size">XPS_SIZE</a> structure has the following properties:



###### 0 ≤ value )



###### 0 ≤ value )

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
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_INVALID_PAGE_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The page size specified in <i>pageDimensions</i> contains one or more  values that are not allowed.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_size">XPS_SIZE</a>