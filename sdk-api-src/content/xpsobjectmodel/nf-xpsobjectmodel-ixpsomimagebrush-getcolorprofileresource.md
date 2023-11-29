---
UID: NF:xpsobjectmodel.IXpsOMImageBrush.GetColorProfileResource
title: IXpsOMImageBrush::GetColorProfileResource (xpsobjectmodel.h)
description: Gets a pointer to the IXpsOMColorProfileResource interface, which contains the color profile resource that is associated with the image.
helpviewer_keywords: ["GetColorProfileResource","GetColorProfileResource method [XPS Documents and Packaging]","GetColorProfileResource method [XPS Documents and Packaging]","IXpsOMImageBrush interface","IXpsOMImageBrush interface [XPS Documents and Packaging]","GetColorProfileResource method","IXpsOMImageBrush.GetColorProfileResource","IXpsOMImageBrush::GetColorProfileResource","xps.ixpsomimagebrush_getcolorprofileresource","xpsobjectmodel/IXpsOMImageBrush::GetColorProfileResource"]
old-location: xps\ixpsomimagebrush_getcolorprofileresource.htm
tech.root: xps
ms.assetid: 7472f84b-cd14-4b9f-8ea9-69e743319d05
ms.date: 12/05/2018
ms.keywords: GetColorProfileResource, GetColorProfileResource method [XPS Documents and Packaging], GetColorProfileResource method [XPS Documents and Packaging],IXpsOMImageBrush interface, IXpsOMImageBrush interface [XPS Documents and Packaging],GetColorProfileResource method, IXpsOMImageBrush.GetColorProfileResource, IXpsOMImageBrush::GetColorProfileResource, xps.ixpsomimagebrush_getcolorprofileresource, xpsobjectmodel/IXpsOMImageBrush::GetColorProfileResource
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
 - IXpsOMImageBrush::GetColorProfileResource
 - xpsobjectmodel/IXpsOMImageBrush::GetColorProfileResource
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
 - IXpsOMImageBrush.GetColorProfileResource
---

# IXpsOMImageBrush::GetColorProfileResource


## -description

Gets a pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresource">IXpsOMColorProfileResource</a> interface, which  contains the color profile resource that is associated with the image.

## -parameters

### -param colorProfileResource [out, retval]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresource">IXpsOMColorProfileResource</a> interface that contains the color profile resource that is associated with the image. If no color profile resource has been set, a <b>NULL</b> pointer is returned.

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
<i>colorProfileResource</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

After loading and parsing the resource into the XPS OM, this method might return an error that applies to another resource. This occurs because all of the relationships are parsed when a resource is loaded.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresource">IXpsOMColorProfileResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush">IXpsOMImageBrush</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>