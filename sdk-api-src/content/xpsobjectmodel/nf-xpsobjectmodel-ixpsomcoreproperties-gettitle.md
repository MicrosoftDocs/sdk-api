---
UID: NF:xpsobjectmodel.IXpsOMCoreProperties.GetTitle
title: IXpsOMCoreProperties::GetTitle (xpsobjectmodel.h)
description: Gets the title property.helpviewer_keywords: ["GetTitle","GetTitle method [XPS Documents and Packaging]","GetTitle method [XPS Documents and Packaging]","IXpsOMCoreProperties interface","IXpsOMCoreProperties interface [XPS Documents and Packaging]","GetTitle method","IXpsOMCoreProperties.GetTitle","IXpsOMCoreProperties::GetTitle","xps.ixpsomcoreproperties_gettitle","xpsobjectmodel/IXpsOMCoreProperties::GetTitle"]
old-location: xps\ixpsomcoreproperties_gettitle.htm
tech.root: printdocs
ms.assetid: 32551dd2-2d6e-4aaa-864b-4c922a90fc27
ms.date: 12/05/2018
ms.keywords: GetTitle, GetTitle method [XPS Documents and Packaging], GetTitle method [XPS Documents and Packaging],IXpsOMCoreProperties interface, IXpsOMCoreProperties interface [XPS Documents and Packaging],GetTitle method, IXpsOMCoreProperties.GetTitle, IXpsOMCoreProperties::GetTitle, xps.ixpsomcoreproperties_gettitle, xpsobjectmodel/IXpsOMCoreProperties::GetTitle
f1_keywords:
- xpsobjectmodel/IXpsOMCoreProperties.GetTitle
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
- IXpsOMCoreProperties.GetTitle
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMCoreProperties::GetTitle


## -description


Gets the <b>title</b> property.


## -parameters




### -param title [out, retval]

The string that is read from the <b>title</b> property.


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
<i>title</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The <b>title</b> property contains the resource's name.

This method allocates the memory used by the string that is returned in <i>title</i>.  If <i>title</i> is not <b>NULL</b>, use the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function  to free the memory.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a>



<a href="https://www.ecma-international.org/publications/standards/Ecma-376.htm">Standard ECMA-376, Office Open XML File Formats</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
 

 

