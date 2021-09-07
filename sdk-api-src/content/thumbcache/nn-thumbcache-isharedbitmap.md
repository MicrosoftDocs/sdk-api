---
UID: NN:thumbcache.ISharedBitmap
title: ISharedBitmap (thumbcache.h)
description: Exposes memory-efficient methods for accessing bitmaps. This interface is used as a thin wrapper around HBITMAP objects, allowing those objects to be reference counted and protected from having their underlying data changed.
helpviewer_keywords: ["ISharedBitmap","ISharedBitmap interface [Windows Shell]","ISharedBitmap interface [Windows Shell]","described","_shell_ISharedBitmap","shell.ISharedBitmap","thumbcache/ISharedBitmap"]
old-location: shell\ISharedBitmap.htm
tech.root: shell
ms.assetid: 72be7757-f969-4f4f-ada1-71789b8d1de0
ms.date: 12/05/2018
ms.keywords: ISharedBitmap, ISharedBitmap interface [Windows Shell], ISharedBitmap interface [Windows Shell],described, _shell_ISharedBitmap, shell.ISharedBitmap, thumbcache/ISharedBitmap
req.header: thumbcache.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Thumbcache.idl
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
 - ISharedBitmap
 - thumbcache/ISharedBitmap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Thumbcache.h
api_name:
 - ISharedBitmap
---

# ISharedBitmap interface


## -description

Exposes memory-efficient methods for accessing bitmaps. This interface is used as a thin wrapper around HBITMAP objects, allowing those objects to be reference counted and protected from having their underlying data changed.

## -inheritance

The <b>ISharedBitmap</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISharedBitmap</b> also has these types of members:

## -remarks

This interface is used in conjunction with the methods of <a href="/windows/desktop/api/thumbcache/nn-thumbcache-ithumbnailcache">IThumbnailCache</a>. Bitmaps returned by <a href="/windows/desktop/api/thumbcache/nf-thumbcache-ithumbnailcache-getthumbnail">IThumbnailCache::GetThumbnail</a> and <a href="/windows/desktop/api/thumbcache/nf-thumbcache-ithumbnailcache-getthumbnailbyid">IThumbnailCache::GetThumbnailByID</a> are of type <b>ISharedBitmap</b>.

When an <b>ISharedBitmap</b> object is retrieved from the thumbnail cache, the underlying bitmap may reside in shared memory to provide improved performance.

The underlying data of the memory-mapped bitmap is protected while the client is accessing it.
