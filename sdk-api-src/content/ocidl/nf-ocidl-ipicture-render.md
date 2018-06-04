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

# IPicture::Render


## -description


Renders (draws) a specified portion of the picture defined by the offset (<i>xSrc</i>,<i>ySrc</i>) of the source picture and the dimensions to copy (<i>cxSrc</i>,<i>xySrc</i>). This picture is rendered onto the specified device context, positioned at the point (<i>x</i>,<i>y</i>), and scaled to the dimensions (<i>cx</i>,<i>cy</i>). The <i>prcWBounds</i> parameter specifies the position of this rendering if the destination device context is itself a metafile. Such information is necessary to place one metafile in another. For more information, see the <i>prcWBounds</i> parameter of <a href="https://msdn.microsoft.com/913593ff-07fe-44bd-88dc-8e58da82089b">IViewObject2::Draw</a>.


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




<a href="https://msdn.microsoft.com/42e3cd0e-2413-494a-8be8-2952089e02d2">IPicture</a>
 

 

