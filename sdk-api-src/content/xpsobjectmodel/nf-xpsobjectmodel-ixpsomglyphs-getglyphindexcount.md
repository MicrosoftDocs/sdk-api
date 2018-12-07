---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.GetGlyphIndexCount
title: IXpsOMGlyphs::GetGlyphIndexCount
author: windows-sdk-content
description: Gets the number of Glyph indices.
old-location: xps\ixpsomglyphs_getglyphindexcount.htm
tech.root: printdocs
ms.assetid: ae37e602-4a47-4234-a8d7-c757f3498308
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetGlyphIndexCount, GetGlyphIndexCount method [XPS Documents and Packaging], GetGlyphIndexCount method [XPS Documents and Packaging],IXpsOMGlyphs interface, IXpsOMGlyphs interface [XPS Documents and Packaging],GetGlyphIndexCount method, IXpsOMGlyphs.GetGlyphIndexCount, IXpsOMGlyphs::GetGlyphIndexCount, xps.ixpsomglyphs_getglyphindexcount, xpsobjectmodel/IXpsOMGlyphs::GetGlyphIndexCount
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
 - IXpsOMGlyphs.GetGlyphIndexCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMGlyphs::GetGlyphIndexCount


## -description


Gets the number of Glyph indices.


## -parameters




### -param indexCount [out, retval]

The number of glyph  indices.


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
<i>indexCount</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks




<a href="https://msdn.microsoft.com/6698ae0b-3525-4612-8234-8ba4dd2870a0">GetGlyphIndices</a> gets the glyph indices.




## -see-also




<a href="https://msdn.microsoft.com/6698ae0b-3525-4612-8234-8ba4dd2870a0">GetGlyphIndices</a>



<a href="https://msdn.microsoft.com/6d2cda65-c719-46f2-97c9-8aee7b5f84b9">IXpsOMGlyphs</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

