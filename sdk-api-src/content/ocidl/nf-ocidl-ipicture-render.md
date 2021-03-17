---
UID: NF:ocidl.IPicture.Render
title: IPicture::Render (ocidl.h)
description: Renders (draws) a specified portion of the picture defined by the offset (xSrc,ySrc) of the source picture and the dimensions to copy (cxSrc,xySrc).
helpviewer_keywords: ["IPicture interface [COM]","Render method","IPicture.Render","IPicture::Render","Render","Render method [COM]","Render method [COM]","IPicture interface","_ctrl_ipicture_render","com.ipicture_render","ocidl/IPicture::Render"]
old-location: com\ipicture_render.htm
tech.root: com
ms.assetid: 45164225-2e0f-4415-a99c-dc0257d606d3
ms.date: 12/05/2018
ms.keywords: IPicture interface [COM],Render method, IPicture.Render, IPicture::Render, Render, Render method [COM], Render method [COM],IPicture interface, _ctrl_ipicture_render, com.ipicture_render, ocidl/IPicture::Render
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - IPicture::Render
 - ocidl/IPicture::Render
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IPicture.Render
---

# IPicture::Render


## -description

Renders (draws) a specified portion of the picture defined by the offset (<i>xSrc</i>,<i>ySrc</i>) of the source picture and the dimensions to copy (<i>cxSrc</i>,<i>xySrc</i>). This picture is rendered onto the specified device context, positioned at the point (<i>x</i>,<i>y</i>), and scaled to the dimensions (<i>cx</i>,<i>cy</i>). The <i>prcWBounds</i> parameter specifies the position of this rendering if the destination device context is itself a metafile. Such information is necessary to place one metafile in another. For more information, see the <i>prcWBounds</i> parameter of <a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw">IViewObject2::Draw</a>.

## -parameters

### -param hDC [in]

A handle of the device context on which to render the image.

### -param x [in]

The horizontal coordinate in <i>hdc</i> at which to place the rendered image.

### -param y [in]

The vertical coordinate in <i>hdc</i> at which to place the rendered image.

### -param cx [in]

The horizontal dimension (width) of the destination rectangle.

### -param cy [in]

The vertical dimension (height) of the destination rectangle

### -param xSrc [in]

The horizontal offset in the source picture from which to start copying.

### -param ySrc [in]

The vertical offset in the source picture from which to start copying.

### -param cxSrc [in]

The horizontal extent to copy from the source picture.

### -param cySrc [in]

The vertical extent to copy from the source picture.

### -param pRcWBounds [in]

A pointer to a rectangle containing the position of the destination within a metafile device context if <i>hdc</i> is a metafile DC. Cannot be <b>NULL</b> in such cases.

## -returns

This method supports the standard return values E_FAIL, E_INVALIDARG, and E_OUTOFMEMORY, as well as the following:

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
The picture was rendered successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>prcWBounds</i> is not valid when <i>hdc</i> contains a metafile device context.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CTL_E_INVALIDPROPERTYVALUE</b></dt>
</dl>
</td>
<td width="60%">
The parameter <i>cx</i>, <i>cy</i>, <i>cxSrc</i>, or <i>cySrc</i> has a value of zero.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipicture">IPicture</a>