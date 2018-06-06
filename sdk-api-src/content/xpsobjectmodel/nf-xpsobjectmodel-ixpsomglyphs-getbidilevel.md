---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.GetBidiLevel
title: IXpsOMGlyphs::GetBidiLevel
author: windows-sdk-content
description: Gets the level of bidirectional text.
old-location: xps\ixpsomglyphs_getbidilevel.htm
old-project: printdocs
ms.assetid: 17110bb7-1ae9-41ef-aed1-8f1c00569825
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: GetBidiLevel, GetBidiLevel method [XPS Documents and Packaging], GetBidiLevel method [XPS Documents and Packaging],IXpsOMGlyphs interface, IXpsOMGlyphs interface [XPS Documents and Packaging],GetBidiLevel method, IXpsOMGlyphs.GetBidiLevel, IXpsOMGlyphs::GetBidiLevel, xps.ixpsomglyphs_getbidilevel, xpsobjectmodel/IXpsOMGlyphs::GetBidiLevel
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: XPS_INTERLEAVING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMGlyphs.GetBidiLevel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMGlyphs::GetBidiLevel


## -description


Gets the level of bidirectional text.


## -parameters




### -param bidiLevel [out, retval]

The level of bidirectional text.

Range: 0–61


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
<i>bidiLevel</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The bidirectional text level, or <b>BidiLevel</b>,  specifies the nesting level of the Unicode bidirectional algorithm. Even values imply the left-to-right layout and odd values the right-to-left layout, which places the run origin on the right side of the first glyph. Advance widths that are positive     will move to the left, allowing subsequent glyphs to be placed to the left of the previous glyph.

The range of allowed values for this property is between 0 and 61, inclusive, and the default value is 0.




## -see-also




<a href="https://msdn.microsoft.com/6d2cda65-c719-46f2-97c9-8aee7b5f84b9">IXpsOMGlyphs</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

