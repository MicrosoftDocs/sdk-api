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

# IXpsOMFontResource::SetContent


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
 

 

