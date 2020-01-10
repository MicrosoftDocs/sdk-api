---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.Clone
title: IXpsOMGlyphs::Clone (xpsobjectmodel.h)
description: Makes a deep copy of the interface.
old-location: xps\ixpsomglyphs_clone.htm
tech.root: printdocs
ms.assetid: 5c402f5a-1d7c-4d2d-87de-954ceba59b51
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [XPS Documents and Packaging], Clone method [XPS Documents and Packaging],IXpsOMGlyphs interface, IXpsOMGlyphs interface [XPS Documents and Packaging],Clone method, IXpsOMGlyphs.Clone, IXpsOMGlyphs::Clone, xps.ixpsomglyphs_clone, xpsobjectmodel/IXpsOMGlyphs::Clone
f1_keywords:
- xpsobjectmodel/IXpsOMGlyphs.Clone
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
- IXpsOMGlyphs.Clone
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMGlyphs::Clone


## -description


Makes a deep copy of the interface.


## -parameters




### -param glyphs [out, retval]

A pointer to the copy of the interface.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>glyphs</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method does not update any of the resource pointers in the copy of the interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
 

 

