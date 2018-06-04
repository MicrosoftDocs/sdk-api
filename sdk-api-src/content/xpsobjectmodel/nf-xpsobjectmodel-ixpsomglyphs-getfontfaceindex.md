---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IXpsOMGlyphs::GetFontFaceIndex


## -description


Gets the index of the font face to be used.

This value is only used when <a href="https://msdn.microsoft.com/6ecca6a0-eb47-4511-898d-cf097a78d6f0">GetFontResource</a> returns an <a href="https://msdn.microsoft.com/dd0ce1c0-1c04-46a8-9075-93de9b3e3062">IXpsOMFontResource</a> interface that  represents a <b>TrueType</b> font collection.


## -parameters




### -param fontFaceIndex [out, retval]

The index value of the font face. If the font face has not been set, –1 is returned.


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
<i>fontFaceIndex</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The font resource is obtained by calling the <a href="https://msdn.microsoft.com/6ecca6a0-eb47-4511-898d-cf097a78d6f0">GetFontResource</a> method.

If a font face has not been set or is not supported by the font, a value of –1 is returned in <i>fontFaceIndex</i>. When the glyph is loaded from an existing XPS document file, a <i>fontFaceIndex</i> value of –1 indicates that the <b>FontUri</b> attribute did not include a <b>#index</b> fragment.

In the following markup of a FixedPage, the <b>FontUri</b> attribute of the <b>Glyphs</b> element has a value of <code>../Resources/Fonts/Font.TTF#1</code>. In this case, <b>GetFontFaceIndex</b>  would return a value of 1 in <i>fontFaceIndex</i>.

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




<a href="https://msdn.microsoft.com/6ecca6a0-eb47-4511-898d-cf097a78d6f0">GetFontResource</a>



<a href="https://msdn.microsoft.com/dd0ce1c0-1c04-46a8-9075-93de9b3e3062">IXpsOMFontResource</a>



<a href="https://msdn.microsoft.com/6d2cda65-c719-46f2-97c9-8aee7b5f84b9">IXpsOMGlyphs</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

