---
UID: NF:xpsobjectmodel.IXpsOMCanvas.GetAccessibilityLongDescription
title: IXpsOMCanvas::GetAccessibilityLongDescription (xpsobjectmodel.h)
description: Gets the long (detailed) textual description of the object's contents. (IXpsOMCanvas.GetAccessibilityLongDescription)
helpviewer_keywords: ["GetAccessibilityLongDescription","GetAccessibilityLongDescription method [XPS Documents and Packaging]","GetAccessibilityLongDescription method [XPS Documents and Packaging]","IXpsOMCanvas interface","IXpsOMCanvas interface [XPS Documents and Packaging]","GetAccessibilityLongDescription method","IXpsOMCanvas.GetAccessibilityLongDescription","IXpsOMCanvas::GetAccessibilityLongDescription","xps.ixpsomcanvas_getaccessibilitylongdescription","xpsobjectmodel/IXpsOMCanvas::GetAccessibilityLongDescription"]
old-location: xps\ixpsomcanvas_getaccessibilitylongdescription.htm
tech.root: xps
ms.assetid: af2ea930-973e-4921-a6c8-192fa5bf4f9b
ms.date: 12/05/2018
ms.keywords: GetAccessibilityLongDescription, GetAccessibilityLongDescription method [XPS Documents and Packaging], GetAccessibilityLongDescription method [XPS Documents and Packaging],IXpsOMCanvas interface, IXpsOMCanvas interface [XPS Documents and Packaging],GetAccessibilityLongDescription method, IXpsOMCanvas.GetAccessibilityLongDescription, IXpsOMCanvas::GetAccessibilityLongDescription, xps.ixpsomcanvas_getaccessibilitylongdescription, xpsobjectmodel/IXpsOMCanvas::GetAccessibilityLongDescription
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
 - IXpsOMCanvas::GetAccessibilityLongDescription
 - xpsobjectmodel/IXpsOMCanvas::GetAccessibilityLongDescription
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
 - IXpsOMCanvas.GetAccessibilityLongDescription
---

# IXpsOMCanvas::GetAccessibilityLongDescription


## -description

Gets the long (detailed) textual description of the object's contents. This text is used by accessibility clients to describe the object.

## -parameters

### -param longDescription [out, retval]

The long (detailed) textual description of the object's contents. A <b>NULL</b> pointer is returned if this text has not been set.

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
<i>longDescription</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The property returned by this method corresponds to the <b>AutomationProperties.HelpText</b> attribute of the <b>Canvas</b> element in the document markup.

This method allocates the memory used by the string that is returned in <i>longDescription</i>.  If <i>longDescription</i> is not <b>NULL</b>, use the  <b>SignatureDefinitions</b>   function to free the memory.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas">IXpsOMCanvas</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
