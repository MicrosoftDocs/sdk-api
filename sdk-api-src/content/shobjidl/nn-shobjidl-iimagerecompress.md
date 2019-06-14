---
UID: NN:shobjidl.IImageRecompress
title: IImageRecompress (shobjidl.h)
author: windows-sdk-content
description: Exposes a method that recompress images.
old-location: shell\IImageRecompress.htm
tech.root: shell
ms.assetid: 48e07bc4-da70-406b-8024-3fa36416247f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IImageRecompress, IImageRecompress interface [Windows Shell], IImageRecompress interface [Windows Shell],described, _win32_IImageRecompress, shell.IImageRecompress, shobjidl/IImageRecompress
ms.topic: interface
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shimgvw.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shimgvw.dll
api_name:
 - IImageRecompress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IImageRecompress interface


## -description


Exposes a method that recompress images.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IImageRecompress</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IImageRecompress</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IImageRecompress</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iimagerecompress-recompressimage">RecompressImage</a>
</td>
<td align="left" width="63%">
Recompresses an image. Implemented in an
		<a href="https://docs.microsoft.com/windows/desktop/shell/known-folders">ImageRecompress</a> object, this method
		accepts x and y dimensions with a designation of quality. The method
		creates a stream containing the new image that has been recompressed
		to the	specified size.

</td>
</tr>
</table> 


## -remarks



Implement <b>IImageRecompress</b> if you are implementing
			an image object that may need recompressing. The
			<b>IImageRecompress</b> interface is implemented in the
			<a href="https://docs.microsoft.com/windows/desktop/shell/known-folders">ImageRecompress</a> object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/shell/known-folders">ImageRecompress</a>
 

 

