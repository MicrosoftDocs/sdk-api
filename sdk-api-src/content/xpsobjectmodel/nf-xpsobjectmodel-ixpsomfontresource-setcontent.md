---
UID: NF:xpsobjectmodel.IXpsOMFontResource.SetContent
title: IXpsOMFontResource::SetContent (xpsobjectmodel.h)
description: Sets the read-only stream to be associated with this resource. (IXpsOMFontResource.SetContent)
helpviewer_keywords: ["IXpsOMFontResource interface [XPS Documents and Packaging]","SetContent method","IXpsOMFontResource.SetContent","IXpsOMFontResource::SetContent","SetContent","SetContent method [XPS Documents and Packaging]","SetContent method [XPS Documents and Packaging]","IXpsOMFontResource interface","XPS_FONT_EMBEDDING_NORMAL","XPS_FONT_EMBEDDING_OBFUSCATED","XPS_FONT_EMBEDDING_RESTRICTED","xps.ixpsomfontresource_setcontent","xpsobjectmodel/IXpsOMFontResource::SetContent"]
old-location: xps\ixpsomfontresource_setcontent.htm
tech.root: xps
ms.assetid: 87a9d003-9406-4c94-b814-4986d213ee47
ms.date: 12/05/2018
ms.keywords: IXpsOMFontResource interface [XPS Documents and Packaging],SetContent method, IXpsOMFontResource.SetContent, IXpsOMFontResource::SetContent, SetContent, SetContent method [XPS Documents and Packaging], SetContent method [XPS Documents and Packaging],IXpsOMFontResource interface, XPS_FONT_EMBEDDING_NORMAL, XPS_FONT_EMBEDDING_OBFUSCATED, XPS_FONT_EMBEDDING_RESTRICTED, xps.ixpsomfontresource_setcontent, xpsobjectmodel/IXpsOMFontResource::SetContent
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
 - IXpsOMFontResource::SetContent
 - xpsobjectmodel/IXpsOMFontResource::SetContent
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
 - IXpsOMFontResource.SetContent
---

# IXpsOMFontResource::SetContent


## -description

Sets the read-only stream to be associated with this resource.

## -parameters

### -param sourceStream [in]

The read-only stream to be associated with this resource.

### -param embeddingOption [in]

The <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_font_embedding">XPS_FONT_EMBEDDING</a> value that describes how the resource is to be obfuscated.

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

Because <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomfontresource-getstream">GetStream</a> gets a clone of  the stream that is set by this method, the provided stream should have an efficient cloning method. A stream with an inefficient cloning method will reduce the performance of <b>GetStream</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource">IXpsOMFontResource</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_font_embedding">XPS_FONT_EMBEDDING</a>
