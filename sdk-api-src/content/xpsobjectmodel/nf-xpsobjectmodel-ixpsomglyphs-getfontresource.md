---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.GetFontResource
title: IXpsOMGlyphs::GetFontResource (xpsobjectmodel.h)

description: Gets a pointer to the IXpsOMFontResource interface of the font resource object required for this text.
old-location: xps\ixpsomglyphs_getfontresource.htm
tech.root: printdocs
ms.assetid: 6ecca6a0-eb47-4511-898d-cf097a78d6f0

ms.date: 12/05/2018
ms.keywords: GetFontResource, GetFontResource method [XPS Documents and Packaging], GetFontResource method [XPS Documents and Packaging],IXpsOMGlyphs interface, IXpsOMGlyphs interface [XPS Documents and Packaging],GetFontResource method, IXpsOMGlyphs.GetFontResource, IXpsOMGlyphs::GetFontResource, xps.ixpsomglyphs_getfontresource, xpsobjectmodel/IXpsOMGlyphs::GetFontResource
ms.topic: method
f1_keywords: 
 - "xpsobjectmodel/IXpsOMGlyphs.GetFontResource"
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
 - IXpsOMGlyphs.GetFontResource
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMGlyphs::GetFontResource


## -description


Gets a pointer to the  <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource">IXpsOMFontResource</a> interface of the font resource object required for this text.


## -parameters




### -param fontResource [out, retval]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource">IXpsOMFontResource</a> interface of the font resource.


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
<i>fontResource</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



After loading and parsing the resource into the XPS OM, this method might return an error that applies to another resource. This occurs because all of the relationships are parsed when a resource is loaded.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource">IXpsOMFontResource</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
 

 

