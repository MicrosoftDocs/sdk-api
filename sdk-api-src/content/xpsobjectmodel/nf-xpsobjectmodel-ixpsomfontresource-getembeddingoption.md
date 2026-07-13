---
UID: NF:xpsobjectmodel.IXpsOMFontResource.GetEmbeddingOption
title: IXpsOMFontResource::GetEmbeddingOption (xpsobjectmodel.h)
description: Gets the embedding option that will be applied when the resource is serialized.
helpviewer_keywords: ["GetEmbeddingOption","GetEmbeddingOption method [XPS Documents and Packaging]","GetEmbeddingOption method [XPS Documents and Packaging]","IXpsOMFontResource interface","IXpsOMFontResource interface [XPS Documents and Packaging]","GetEmbeddingOption method","IXpsOMFontResource.GetEmbeddingOption","IXpsOMFontResource::GetEmbeddingOption","XPS_FONT_EMBEDDING_NORMAL","XPS_FONT_EMBEDDING_OBFUSCATED","XPS_FONT_EMBEDDING_RESTRICTED","xps.ixpsomfontresource_getembeddingoption","xpsobjectmodel/IXpsOMFontResource::GetEmbeddingOption"]
old-location: xps\ixpsomfontresource_getembeddingoption.htm
tech.root: xps
ms.assetid: 8c4b3741-2c9c-4964-ae51-53dd738e8d9b
ms.date: 12/05/2018
ms.keywords: GetEmbeddingOption, GetEmbeddingOption method [XPS Documents and Packaging], GetEmbeddingOption method [XPS Documents and Packaging],IXpsOMFontResource interface, IXpsOMFontResource interface [XPS Documents and Packaging],GetEmbeddingOption method, IXpsOMFontResource.GetEmbeddingOption, IXpsOMFontResource::GetEmbeddingOption, XPS_FONT_EMBEDDING_NORMAL, XPS_FONT_EMBEDDING_OBFUSCATED, XPS_FONT_EMBEDDING_RESTRICTED, xps.ixpsomfontresource_getembeddingoption, xpsobjectmodel/IXpsOMFontResource::GetEmbeddingOption
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsOMFontResource::GetEmbeddingOption
 - xpsobjectmodel/IXpsOMFontResource::GetEmbeddingOption
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMFontResource.GetEmbeddingOption
---

# IXpsOMFontResource::GetEmbeddingOption


## -description

Gets the embedding option that will be applied when the resource is serialized.

## -parameters

### -param embeddingOption [out, retval]

The stream's embedding option.

The <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_font_embedding">XPS_FONT_EMBEDDING</a> value describes how the resource is obfuscated. The following possible values are returned in this parameter:

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

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource">IXpsOMFontResource</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_font_embedding">XPS_FONT_EMBEDDING</a>