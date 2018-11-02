---
UID: NF:strmif.IDrawVideoImage.DrawVideoImageBegin
title: IDrawVideoImage::DrawVideoImageBegin
author: windows-sdk-content
description: Note  This interface has been deprecated. New applications should not use it. The DrawVideoImageBegin method turns off DirectDraw in preparation for a call to the DrawVideoImageDraw method.
old-location: dshow\idrawvideoimage_drawvideoimagebegin.htm
tech.root: DirectShow
ms.assetid: a39125b3-15b1-428d-aa64-c1b2bccf616a
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: DrawVideoImageBegin, DrawVideoImageBegin method [DirectShow], DrawVideoImageBegin method [DirectShow],IDrawVideoImage interface, IDrawVideoImage interface [DirectShow],DrawVideoImageBegin method, IDrawVideoImage.DrawVideoImageBegin, IDrawVideoImage::DrawVideoImageBegin, IDrawVideoImageDrawVideoImageBegin, dshow.idrawvideoimage_drawvideoimagebegin, strmif/IDrawVideoImage::DrawVideoImageBegin
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IDrawVideoImage.DrawVideoImageBegin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDrawVideoImage::DrawVideoImageBegin


## -description



<div class="alert"><b>Note</b>  This interface has been deprecated. New applications should not use it.</div>
<div> </div>
The <code>DrawVideoImageBegin</code> method turns off DirectDraw in preparation for a call to the <b>DrawVideoImageDraw</b> method.




## -parameters






## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ff412213-60e5-43d8-8cb1-e7ae8b3ca1bc">IDrawVideoImage Interface</a>



<a href="https://msdn.microsoft.com/cecc3ae4-f1fa-437e-b967-c54fca10b27c">IDrawVideoImage::DrawVideoImageDraw</a>
 

 

