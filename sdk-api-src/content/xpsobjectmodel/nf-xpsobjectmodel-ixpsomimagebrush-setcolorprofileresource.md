---
UID: NF:xpsobjectmodel.IXpsOMImageBrush.SetColorProfileResource
title: IXpsOMImageBrush::SetColorProfileResource (xpsobjectmodel.h)
description: Sets a pointer to the IXpsOMColorProfileResource interface, which contains the color profile resource that is associated with the image.
helpviewer_keywords: ["IXpsOMImageBrush interface [XPS Documents and Packaging]","SetColorProfileResource method","IXpsOMImageBrush.SetColorProfileResource","IXpsOMImageBrush::SetColorProfileResource","SetColorProfileResource","SetColorProfileResource method [XPS Documents and Packaging]","SetColorProfileResource method [XPS Documents and Packaging]","IXpsOMImageBrush interface","xps.ixpsomimagebrush_setcolorprofileresource","xpsobjectmodel/IXpsOMImageBrush::SetColorProfileResource"]
old-location: xps\ixpsomimagebrush_setcolorprofileresource.htm
tech.root: xps
ms.assetid: d18511b7-13ed-4528-9f3d-aef3bcadc403
ms.date: 12/05/2018
ms.keywords: IXpsOMImageBrush interface [XPS Documents and Packaging],SetColorProfileResource method, IXpsOMImageBrush.SetColorProfileResource, IXpsOMImageBrush::SetColorProfileResource, SetColorProfileResource, SetColorProfileResource method [XPS Documents and Packaging], SetColorProfileResource method [XPS Documents and Packaging],IXpsOMImageBrush interface, xps.ixpsomimagebrush_setcolorprofileresource, xpsobjectmodel/IXpsOMImageBrush::SetColorProfileResource
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
 - IXpsOMImageBrush::SetColorProfileResource
 - xpsobjectmodel/IXpsOMImageBrush::SetColorProfileResource
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
 - IXpsOMImageBrush.SetColorProfileResource
---

# IXpsOMImageBrush::SetColorProfileResource


## -description

Sets a pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresource">IXpsOMColorProfileResource</a> interface, which contains the color profile resource that is associated with the image.

## -parameters

### -param colorProfileResource [in]

The color profile resource that is associated with the image. A <b>NULL</b> pointer will release any previously set color profile resources.

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
<dt><b>XPS_E_NO_CUSTOM_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
<i>colorProfileResource</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresource">IXpsOMColorProfileResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush">IXpsOMImageBrush</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>