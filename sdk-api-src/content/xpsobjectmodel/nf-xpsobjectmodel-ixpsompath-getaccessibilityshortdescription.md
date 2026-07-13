---
UID: NF:xpsobjectmodel.IXpsOMPath.GetAccessibilityShortDescription
title: IXpsOMPath::GetAccessibilityShortDescription (xpsobjectmodel.h)
description: Gets the short textual description of the object's contents.
helpviewer_keywords: ["GetAccessibilityShortDescription","GetAccessibilityShortDescription method [XPS Documents and Packaging]","GetAccessibilityShortDescription method [XPS Documents and Packaging]","IXpsOMPath interface","IXpsOMPath interface [XPS Documents and Packaging]","GetAccessibilityShortDescription method","IXpsOMPath.GetAccessibilityShortDescription","IXpsOMPath::GetAccessibilityShortDescription","xps.ixpsompath_getaccessibilityshortdescription","xpsobjectmodel/IXpsOMPath::GetAccessibilityShortDescription"]
old-location: xps\ixpsompath_getaccessibilityshortdescription.htm
tech.root: xps
ms.assetid: 0124d37a-74c1-4f8b-9d91-c12e92cd5e8c
ms.date: 12/05/2018
ms.keywords: GetAccessibilityShortDescription, GetAccessibilityShortDescription method [XPS Documents and Packaging], GetAccessibilityShortDescription method [XPS Documents and Packaging],IXpsOMPath interface, IXpsOMPath interface [XPS Documents and Packaging],GetAccessibilityShortDescription method, IXpsOMPath.GetAccessibilityShortDescription, IXpsOMPath::GetAccessibilityShortDescription, xps.ixpsompath_getaccessibilityshortdescription, xpsobjectmodel/IXpsOMPath::GetAccessibilityShortDescription
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
 - IXpsOMPath::GetAccessibilityShortDescription
 - xpsobjectmodel/IXpsOMPath::GetAccessibilityShortDescription
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
 - IXpsOMPath.GetAccessibilityShortDescription
---

# IXpsOMPath::GetAccessibilityShortDescription


## -description

Gets the short textual description of the object's contents. This  description is used by accessibility clients to describe the object.

## -parameters

### -param shortDescription [out, retval]

The short textual description of the object's contents. If this text has not been set, a <b>NULL</b> pointer will be returned.

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
<i>shortDescription</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The value that is returned in <i>shortDescription</i> is the value of the <b>AutomationProperties.Name</b> attribute of the <b>Path</b> element in the document markup.



This method allocates the memory used by the string that is returned in <i>shortDescription</i>.  If <i>shortDescription</i> is not <b>NULL</b>, use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function  to free the memory.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath">IXpsOMPath</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>