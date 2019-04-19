---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.GetGlyphMappingCount
title: IXpsOMGlyphs::GetGlyphMappingCount (xpsobjectmodel.h)
author: windows-sdk-content
description: Gets the number of glyph mappings.
old-location: xps\ixpsomglyphs_getglyphmappingcount.htm
tech.root: printdocs
ms.assetid: 6c580aaf-72ed-4eff-b26e-8438d64f29e2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetGlyphMappingCount, GetGlyphMappingCount method [XPS Documents and Packaging], GetGlyphMappingCount method [XPS Documents and Packaging],IXpsOMGlyphs interface, IXpsOMGlyphs interface [XPS Documents and Packaging],GetGlyphMappingCount method, IXpsOMGlyphs.GetGlyphMappingCount, IXpsOMGlyphs::GetGlyphMappingCount, xps.ixpsomglyphs_getglyphmappingcount, xpsobjectmodel/IXpsOMGlyphs::GetGlyphMappingCount
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
 - IXpsOMGlyphs.GetGlyphMappingCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMGlyphs::GetGlyphMappingCount


## -description


Gets the number of glyph mappings.


## -parameters




### -param glyphMappingCount [out, retval]

The number of glyph mappings.


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
<i>glyphMappingCount</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks




<a href="https://msdn.microsoft.com/c7cf4352-f08a-43cb-a063-5d369017a887">GetGlyphMappings</a> gets the glyph mappings.




## -see-also




<a href="https://msdn.microsoft.com/c7cf4352-f08a-43cb-a063-5d369017a887">GetGlyphMappings</a>



<a href="https://msdn.microsoft.com/6d2cda65-c719-46f2-97c9-8aee7b5f84b9">IXpsOMGlyphs</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

