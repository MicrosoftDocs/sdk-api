---
UID: NF:xpsobjectmodel.IXpsOMImageBrush.SetImageResource
title: IXpsOMImageBrush::SetImageResource (xpsobjectmodel.h)
description: Sets a pointer to the IXpsOMImageResource interface that contains the image resource to be used as the source for the brush.
helpviewer_keywords: ["IXpsOMImageBrush interface [XPS Documents and Packaging]","SetImageResource method","IXpsOMImageBrush.SetImageResource","IXpsOMImageBrush::SetImageResource","SetImageResource","SetImageResource method [XPS Documents and Packaging]","SetImageResource method [XPS Documents and Packaging]","IXpsOMImageBrush interface","xps.ixpsomimagebrush_setimageresource","xpsobjectmodel/IXpsOMImageBrush::SetImageResource"]
old-location: xps\ixpsomimagebrush_setimageresource.htm
tech.root: xps
ms.assetid: 2c3c5189-0090-48c7-bc36-c9014758b968
ms.date: 12/05/2018
ms.keywords: IXpsOMImageBrush interface [XPS Documents and Packaging],SetImageResource method, IXpsOMImageBrush.SetImageResource, IXpsOMImageBrush::SetImageResource, SetImageResource, SetImageResource method [XPS Documents and Packaging], SetImageResource method [XPS Documents and Packaging],IXpsOMImageBrush interface, xps.ixpsomimagebrush_setimageresource, xpsobjectmodel/IXpsOMImageBrush::SetImageResource
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
 - IXpsOMImageBrush::SetImageResource
 - xpsobjectmodel/IXpsOMImageBrush::SetImageResource
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
 - IXpsOMImageBrush.SetImageResource
---

# IXpsOMImageBrush::SetImageResource


## -description

Sets a pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a> interface that contains the image resource to be used as the source for the brush.

## -parameters

### -param imageResource [in]

The image resource to be used as the source for the brush. This parameter must not be a <b>NULL</b> pointer.

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
<i>imageResource</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_NO_CUSTOM_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
<i>imageResource</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>

## -remarks

The image resource must be of type JPEG, PNG, TIFF 6.0, or HD  Photo.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush">IXpsOMImageBrush</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type">XPS_IMAGE_TYPE</a>