---
UID: NN:shobjidl.IImageRecompress
title: IImageRecompress (shobjidl.h)
description: Exposes a method that recompress images.
helpviewer_keywords: ["IImageRecompress","IImageRecompress interface [Windows Shell]","IImageRecompress interface [Windows Shell]","described","_win32_IImageRecompress","shell.IImageRecompress","shobjidl/IImageRecompress"]
old-location: shell\IImageRecompress.htm
tech.root: shell
ms.assetid: 48e07bc4-da70-406b-8024-3fa36416247f
ms.date: 12/05/2018
ms.keywords: IImageRecompress, IImageRecompress interface [Windows Shell], IImageRecompress interface [Windows Shell],described, _win32_IImageRecompress, shell.IImageRecompress, shobjidl/IImageRecompress
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IImageRecompress
 - shobjidl/IImageRecompress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shimgvw.dll
api_name:
 - IImageRecompress
---

# IImageRecompress interface


## -description

Exposes a method that recompress images.

## -inheritance

The <b>IImageRecompress</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IImageRecompress</b> also has these types of members:

## -remarks

Implement <b>IImageRecompress</b> if you are implementing
			an image object that may need recompressing. The
			<b>IImageRecompress</b> interface is implemented in the
			<a href="/windows/desktop/shell/known-folders">ImageRecompress</a> object.

## -see-also

<a href="/windows/desktop/shell/known-folders">ImageRecompress</a>
