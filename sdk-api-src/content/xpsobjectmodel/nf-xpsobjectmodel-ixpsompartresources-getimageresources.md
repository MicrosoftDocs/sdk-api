---
UID: NF:xpsobjectmodel.IXpsOMPartResources.GetImageResources
title: IXpsOMPartResources::GetImageResources (xpsobjectmodel.h)
description: Gets the IXpsOMImageResourceCollection interface that contains the images that are used in the XPS document.
helpviewer_keywords: ["GetImageResources","GetImageResources method [XPS Documents and Packaging]","GetImageResources method [XPS Documents and Packaging]","IXpsOMPartResources interface","IXpsOMPartResources interface [XPS Documents and Packaging]","GetImageResources method","IXpsOMPartResources.GetImageResources","IXpsOMPartResources::GetImageResources","xps.ixpsompartresources_getimageresources","xpsobjectmodel/IXpsOMPartResources::GetImageResources"]
old-location: xps\ixpsompartresources_getimageresources.htm
tech.root: xps
ms.assetid: d30281b7-0b2c-4240-813b-a53c8acb819c
ms.date: 12/05/2018
ms.keywords: GetImageResources, GetImageResources method [XPS Documents and Packaging], GetImageResources method [XPS Documents and Packaging],IXpsOMPartResources interface, IXpsOMPartResources interface [XPS Documents and Packaging],GetImageResources method, IXpsOMPartResources.GetImageResources, IXpsOMPartResources::GetImageResources, xps.ixpsompartresources_getimageresources, xpsobjectmodel/IXpsOMPartResources::GetImageResources
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
 - IXpsOMPartResources::GetImageResources
 - xpsobjectmodel/IXpsOMPartResources::GetImageResources
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
 - IXpsOMPartResources.GetImageResources
---

# IXpsOMPartResources::GetImageResources


## -description

Gets the  <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresourcecollection">IXpsOMImageResourceCollection</a> interface that contains the images that are used in the XPS document.

## -parameters

### -param imageResources [out, retval]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresourcecollection">IXpsOMImageResourceCollection</a> interface that contains the images that are used in the XPS document.

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
<i>imageResources</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

After loading and parsing the resource into the XPS OM, this method might return an error that applies to another resource. This occurs because all of the relationships are parsed when a resource is loaded.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresourcecollection">IXpsOMImageResourceCollection</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources">IXpsOMPartResources</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>