---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.SetFontFaceIndex
title: IXpsOMGlyphs::SetFontFaceIndex (xpsobjectmodel.h)
author: windows-sdk-content
description: Sets the index of the font face to be used.
old-location: xps\ixpsomglyphs_setfontfaceindex.htm
tech.root: printdocs
ms.assetid: 9430474d-b874-47c7-b916-089280da8873
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IXpsOMGlyphs interface [XPS Documents and Packaging],SetFontFaceIndex method, IXpsOMGlyphs.SetFontFaceIndex, IXpsOMGlyphs::SetFontFaceIndex, SetFontFaceIndex, SetFontFaceIndex method [XPS Documents and Packaging], SetFontFaceIndex method [XPS Documents and Packaging],IXpsOMGlyphs interface, xps.ixpsomglyphs_setfontfaceindex, xpsobjectmodel/IXpsOMGlyphs::SetFontFaceIndex
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
 - IXpsOMGlyphs.SetFontFaceIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMGlyphs::SetFontFaceIndex


## -description


Sets the index of the font face to be used.

This value is only used when <a href="https://msdn.microsoft.com/6ecca6a0-eb47-4511-898d-cf097a78d6f0">GetFontResource</a> returns an <a href="https://msdn.microsoft.com/dd0ce1c0-1c04-46a8-9075-93de9b3e3062">IXpsOMFontResource</a> interface that  represents a <b>TrueType</b> font collection.


## -parameters




### -param fontFaceIndex [in]

The index value of the font face to be used.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>fontFaceIndex</i> is not valid; it must be an integer that is greater than or equal to –1.

</td>
</tr>
</table>
 




## -remarks



The default value of the font face index property is –1, which means that a font index has not been set or the font resource is not a  <b>TrueType</b> font collection.

If this value is specified and is not –1, "#&lt;Index&gt;" is appended to the Font URI during serialization. Here, &lt;Index&gt; is the value that is set by <b>SetFontFaceIndex</b>.

The following markup of a FixedPage shows the result of setting the <i>fontFaceIndex</i> to 1. Notice that the <b>FontUri</b> attribute of the <b>Glyphs</b> element has a value of <code>../Resources/Fonts/Font.TTF#1</code>, which includes the index of the font face.

<pre class="syntax" xml:space="preserve"><code>    &lt;FixedPage Height="1056" Width="816" xml:lang="en-US"
    xmlns="http://schemas.microsoft.com/xps/2005/06"&gt;
      &lt;Glyphs
      OriginX="96"
      OriginY="96"
      UnicodeString="This is Page 1!"
      FontUri="../Resources/Fonts/Font.TTF#1"
      FontRenderingEmSize="16" /&gt;
    &lt;/FixedPage&gt;</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/6d2cda65-c719-46f2-97c9-8aee7b5f84b9">IXpsOMGlyphs</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

