---
UID: NF:xpsobjectmodel.IXpsOMCoreProperties.GetCategory
title: IXpsOMCoreProperties::GetCategory (xpsobjectmodel.h)
description: Gets the category property.
helpviewer_keywords: ["GetCategory","GetCategory method [XPS Documents and Packaging]","GetCategory method [XPS Documents and Packaging]","IXpsOMCoreProperties interface","IXpsOMCoreProperties interface [XPS Documents and Packaging]","GetCategory method","IXpsOMCoreProperties.GetCategory","IXpsOMCoreProperties::GetCategory","xps.ixpsomcoreproperties_getcategory","xpsobjectmodel/IXpsOMCoreProperties::GetCategory"]
old-location: xps\ixpsomcoreproperties_getcategory.htm
tech.root: xps
ms.assetid: 97b1b0ca-a2e7-4835-aece-c2cc23481530
ms.date: 12/05/2018
ms.keywords: GetCategory, GetCategory method [XPS Documents and Packaging], GetCategory method [XPS Documents and Packaging],IXpsOMCoreProperties interface, IXpsOMCoreProperties interface [XPS Documents and Packaging],GetCategory method, IXpsOMCoreProperties.GetCategory, IXpsOMCoreProperties::GetCategory, xps.ixpsomcoreproperties_getcategory, xpsobjectmodel/IXpsOMCoreProperties::GetCategory
f1_keywords:
- xpsobjectmodel/IXpsOMCoreProperties.GetCategory
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- xpsobjectmodel.h
api_name:
- IXpsOMCoreProperties.GetCategory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMCoreProperties::GetCategory


## -description


Gets the <b>category</b> property.


## -parameters




### -param category [out, retval]

The string that is read from the <b>category</b> property.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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
<i>category</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The <b>category</b> property contains categorization of the content.

This method allocates the memory used by the string that is returned in <i>category</i>.  If <i>category</i> is not <b>NULL</b>, use the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function  to free the memory.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a>



<a href="https://www.ecma-international.org/publications/standards/Ecma-376.htm">Standard ECMA-376, Office Open XML File Formats</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
 

 

