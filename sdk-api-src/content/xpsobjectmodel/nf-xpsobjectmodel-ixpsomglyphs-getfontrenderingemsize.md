---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.GetFontRenderingEmSize
title: IXpsOMGlyphs::GetFontRenderingEmSize
author: windows-sdk-content
description: Gets the font size.
old-location: xps\ixpsomglyphs_getfontrenderingemsize.htm
tech.root: printdocs
ms.assetid: be1c6eff-20ef-49d3-929e-3595b421bcb9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetFontRenderingEmSize, GetFontRenderingEmSize method [XPS Documents and Packaging], GetFontRenderingEmSize method [XPS Documents and Packaging],IXpsOMGlyphs interface, IXpsOMGlyphs interface [XPS Documents and Packaging],GetFontRenderingEmSize method, IXpsOMGlyphs.GetFontRenderingEmSize, IXpsOMGlyphs::GetFontRenderingEmSize, xps.ixpsomglyphs_getfontrenderingemsize, xpsobjectmodel/IXpsOMGlyphs::GetFontRenderingEmSize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IXpsOMGlyphs.GetFontRenderingEmSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMGlyphs::GetFontRenderingEmSize


## -description


Gets the font size.


## -parameters




### -param fontRenderingEmSize [out, retval]

The  font size.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>.

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
<i>fontRenderingEmSize</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The em size that is returned in <i>fontRenderingEmSize</i> specifies the font size in the drawing surface units. The drawing surface units are expressed as floating-point values in the effective coordinate space.

In new glyph objects, the default value of <i>fontRenderingEmSize</i> is 10.0.

If the value of <i>fontRenderingEmSize</i> is 0.0, no text is displayed.




## -see-also




<a href="https://msdn.microsoft.com/6d2cda65-c719-46f2-97c9-8aee7b5f84b9">IXpsOMGlyphs</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

