---
UID: NF:xpsobjectmodel.IXpsOMVisual.SetName
title: IXpsOMVisual::SetName (xpsobjectmodel.h)
description: Sets the Name property of the visual.
helpviewer_keywords: ["IXpsOMVisual interface [XPS Documents and Packaging]","SetName method","IXpsOMVisual.SetName","IXpsOMVisual::SetName","SetName","SetName method [XPS Documents and Packaging]","SetName method [XPS Documents and Packaging]","IXpsOMVisual interface","xps.ixpsomvisual_setname","xpsobjectmodel/IXpsOMVisual::SetName"]
old-location: xps\ixpsomvisual_setname.htm
tech.root: xps
ms.assetid: 8bf30b4c-bddf-4ca8-91c6-af739125829c
ms.date: 12/05/2018
ms.keywords: IXpsOMVisual interface [XPS Documents and Packaging],SetName method, IXpsOMVisual.SetName, IXpsOMVisual::SetName, SetName, SetName method [XPS Documents and Packaging], SetName method [XPS Documents and Packaging],IXpsOMVisual interface, xps.ixpsomvisual_setname, xpsobjectmodel/IXpsOMVisual::SetName
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
 - IXpsOMVisual::SetName
 - xpsobjectmodel/IXpsOMVisual::SetName
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
 - IXpsOMVisual.SetName
---

# IXpsOMVisual::SetName


## -description

Sets the <b>Name</b>  property of the visual.

## -parameters

### -param name [in]

The name of the visual. A <b>NULL</b> pointer clears the <b>Name</b> property.

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
<dt><b>XPS_E_INVALID_NAME</b></dt>
</dl>
</td>
<td width="60%">
According to the <a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>, the string that is passed in <i>name</i>  is not a valid name.
              

</td>
</tr>
</table>

## -remarks

Names must be unique.

Clearing the <b>Name</b> property by passing a <b>NULL</b> pointer in <i>name</i> sets the <b>IsHyperlinkTarget</b> property to <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>