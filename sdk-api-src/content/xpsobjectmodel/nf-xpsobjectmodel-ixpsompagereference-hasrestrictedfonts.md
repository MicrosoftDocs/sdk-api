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

# IXpsOMPageReference::HasRestrictedFonts


## -description


Gets a Boolean value that indicates whether the document sub-tree of the referenced page includes any Glyphs that have a font resource whose  <b>EmbeddingOption</b> property is set to <a href="https://msdn.microsoft.com/9701b1c2-a909-410e-b05b-76bbd5bc8b44">XPS_FONT_EMBEDDING_RESTRICTED</a>.


## -parameters




### -param restrictedFonts [out, retval]

A Boolean value that indicates whether the document sub-tree of the referenced page includes any <a href="https://msdn.microsoft.com/6d2cda65-c719-46f2-97c9-8aee7b5f84b9">IXpsOMGlyphs</a> interfaces that have a font resource whose  <b>EmbeddingOption</b> property is set to <a href="https://msdn.microsoft.com/9701b1c2-a909-410e-b05b-76bbd5bc8b44">XPS_FONT_EMBEDDING_RESTRICTED</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b><b>TRUE</b></b></dt>
</dl>
</td>
<td width="60%">
If the referenced page is loaded,  the page references at least one font resource whose <b>EmbeddingOption</b> property is set to <a href="https://msdn.microsoft.com/9701b1c2-a909-410e-b05b-76bbd5bc8b44">XPS_FONT_EMBEDDING_RESTRICTED</a>.

If the referenced page is not loaded, it has a relationship with at least one font resource whose <b>EmbeddingOption</b> property is set to   <a href="https://msdn.microsoft.com/9701b1c2-a909-410e-b05b-76bbd5bc8b44">XPS_FONT_EMBEDDING_RESTRICTED</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
If the referenced page is loaded,  the page does not reference any font resources whose <b>EmbeddingOption</b> property is set to <a href="https://msdn.microsoft.com/9701b1c2-a909-410e-b05b-76bbd5bc8b44">XPS_FONT_EMBEDDING_RESTRICTED</a>.

If the referenced page is not loaded, it does not have a relationship with a font resource whose <b>EmbeddingOption</b> property is set to   <a href="https://msdn.microsoft.com/9701b1c2-a909-410e-b05b-76bbd5bc8b44">XPS_FONT_EMBEDDING_RESTRICTED</a>.

</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

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
<i>restrictedFonts</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This value is not updated automatically. If fonts or glyphs are added or removed such that the value changes, <b>HasRestrictedFonts</b> must be called again to get the current value.




## -see-also




<a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9701b1c2-a909-410e-b05b-76bbd5bc8b44">XPS_FONT_EMBEDDING_RESTRICTED</a>
 

 

