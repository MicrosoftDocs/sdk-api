---
UID: NF:xpsobjectmodel.IXpsOMVisual.GetName
title: IXpsOMVisual::GetName (xpsobjectmodel.h)
description: Gets the Name property of the visual.
helpviewer_keywords: ["GetName","GetName method [XPS Documents and Packaging]","GetName method [XPS Documents and Packaging]","IXpsOMVisual interface","IXpsOMVisual interface [XPS Documents and Packaging]","GetName method","IXpsOMVisual.GetName","IXpsOMVisual::GetName","xps.ixpsomvisual_getname","xpsobjectmodel/IXpsOMVisual::GetName"]
old-location: xps\ixpsomvisual_getname.htm
tech.root: xps
ms.assetid: 0a8b592e-c80e-4a0f-b9a4-8c362da43ced
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [XPS Documents and Packaging], GetName method [XPS Documents and Packaging],IXpsOMVisual interface, IXpsOMVisual interface [XPS Documents and Packaging],GetName method, IXpsOMVisual.GetName, IXpsOMVisual::GetName, xps.ixpsomvisual_getname, xpsobjectmodel/IXpsOMVisual::GetName
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
 - IXpsOMVisual::GetName
 - xpsobjectmodel/IXpsOMVisual::GetName
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
 - IXpsOMVisual.GetName
---

# IXpsOMVisual::GetName


## -description

Gets the <b>Name</b> property of the visual.

## -parameters

### -param name [out, retval]

The <b>Name</b> property string. If  the <b>Name</b> property has not been set, a <b>NULL</b> pointer is returned.

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
<i>name</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method allocates the memory that is used by the string returned in <i>name</i>.  If <i>name</i> is not <b>NULL</b>, use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function  to free the memory.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>