---
UID: NF:xpsobjectmodel.IXpsOMFontResource.SetContent
title: IXpsOMFontResource::SetContent method
author: windows-driver-content
description: Sets the read-only stream to be associated with this resource.
old-location: xps\ixpsomfontresource_setcontent.htm
old-project: printdocs
ms.assetid: 87a9d003-9406-4c94-b814-4986d213ee47
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IXpsOMFontResource, IXpsOMFontResource interface [XPS Documents and Packaging], SetContent method, IXpsOMFontResource::SetContent, SetContent method [XPS Documents and Packaging], SetContent method [XPS Documents and Packaging], IXpsOMFontResource interface, SetContent,IXpsOMFontResource.SetContent, XPS_FONT_EMBEDDING_NORMAL, XPS_FONT_EMBEDDING_OBFUSCATED, XPS_FONT_EMBEDDING_RESTRICTED, xps.ixpsomfontresource_setcontent, xpsobjectmodel/IXpsOMFontResource::SetContent
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: XPS_INTERLEAVING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsobjectmodel.h
api_name:
-	IXpsOMFontResource.SetContent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMFontResource::SetContent method


## -description


Sets the read-only stream to be associated with this resource.


## -parameters




### -param sourceStream [in]

The read-only stream to be associated with this resource.


### -param embeddingOption [in]

The <a href="https://msdn.microsoft.com/9701b1c2-a909-410e-b05b-76bbd5bc8b44">XPS_FONT_EMBEDDING</a> value that describes how the resource is to be obfuscated.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XPS_FONT_EMBEDDING_NORMAL"></a><a id="xps_font_embedding_normal"></a><dl>
<dt><b>XPS_FONT_EMBEDDING_NORMAL</b></dt>
</dl>
</td>
<td width="60%">
Font resource is neither obfuscated nor restricted.

</td>
</tr>
<tr>
<td width="40%"><a id="XPS_FONT_EMBEDDING_OBFUSCATED"></a><a id="xps_font_embedding_obfuscated"></a><dl>
<dt><b>XPS_FONT_EMBEDDING_OBFUSCATED</b></dt>
</dl>
</td>
<td width="60%">
Font resource is obfuscated but not restricted.

</td>
</tr>
<tr>
<td width="40%"><a id="XPS_FONT_EMBEDDING_RESTRICTED"></a><a id="xps_font_embedding_restricted"></a><dl>
<dt><b>XPS_FONT_EMBEDDING_RESTRICTED</b></dt>
</dl>
</td>
<td width="60%">
Font resource is both obfuscated and restricted.

</td>
</tr>
</table>
 


### -param partName [in]

The part name to be assigned to this resource.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The calling method  should treat this stream as a single-threaded apartment (STA) model object and not re-enter any of the stream interface's methods.

The stream  assigned to this resource should not be obfuscated. Obfuscation of the font resource takes place during serialization.

Providing an obfuscated font stream while setting the <i>embeddingOption</i> to XPS_FONT_EMBEDDING_OBFUSCATED will result in a font that is not obfuscated in the serialized XPS document.

<i>partName</i> resets the part name for this object and is checked against the value of  <i>embeddingOption</i> for the proper obfuscation syntax.

Because <a href="https://msdn.microsoft.com/d512e862-e2d0-4cc8-a20a-bc3cfbfbcc47">GetStream</a> gets a clone of  the stream that is set by this method, the provided stream should have an efficient cloning method. A stream with an inefficient cloning method will reduce the performance of <b>GetStream</b>.




## -see-also




<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<a href="https://msdn.microsoft.com/dd0ce1c0-1c04-46a8-9075-93de9b3e3062">IXpsOMFontResource</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9701b1c2-a909-410e-b05b-76bbd5bc8b44">XPS_FONT_EMBEDDING</a>
 

 

