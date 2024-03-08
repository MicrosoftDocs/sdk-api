---
UID: NF:xpsobjectmodel.IXpsOMVisual.SetOpacity
title: IXpsOMVisual::SetOpacity (xpsobjectmodel.h)
description: Sets the opacity value of the visual.
helpviewer_keywords: ["IXpsOMVisual interface [XPS Documents and Packaging]","SetOpacity method","IXpsOMVisual.SetOpacity","IXpsOMVisual::SetOpacity","SetOpacity","SetOpacity method [XPS Documents and Packaging]","SetOpacity method [XPS Documents and Packaging]","IXpsOMVisual interface","xps.ixpsomvisual_setopacity","xpsobjectmodel/IXpsOMVisual::SetOpacity"]
old-location: xps\ixpsomvisual_setopacity.htm
tech.root: xps
ms.assetid: 2a29aee3-f11b-41e7-a871-3be3d5994409
ms.date: 12/05/2018
ms.keywords: IXpsOMVisual interface [XPS Documents and Packaging],SetOpacity method, IXpsOMVisual.SetOpacity, IXpsOMVisual::SetOpacity, SetOpacity, SetOpacity method [XPS Documents and Packaging], SetOpacity method [XPS Documents and Packaging],IXpsOMVisual interface, xps.ixpsomvisual_setopacity, xpsobjectmodel/IXpsOMVisual::SetOpacity
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
 - IXpsOMVisual::SetOpacity
 - xpsobjectmodel/IXpsOMVisual::SetOpacity
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
 - IXpsOMVisual.SetOpacity
---

# IXpsOMVisual::SetOpacity


## -description

Sets the opacity value of the visual.

## -parameters

### -param opacity [in]

The opacity value to be set for the visual. 

The range of allowed values for this parameter is 0.0  to 1.0; with 0.0 the visual is completely transparent, and with 1.0 it is completely opaque.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>opacity</i> contains a value that is not allowed.
              

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>