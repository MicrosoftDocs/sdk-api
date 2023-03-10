---
UID: NF:thumbcache.IThumbnailProvider.GetThumbnail
title: IThumbnailProvider::GetThumbnail (thumbcache.h)
description: Gets a thumbnail image and alpha type.
helpviewer_keywords: ["GetThumbnail","GetThumbnail method [Windows Shell]","GetThumbnail method [Windows Shell]","IThumbnailProvider interface","IThumbnailProvider interface [Windows Shell]","GetThumbnail method","IThumbnailProvider.GetThumbnail","IThumbnailProvider::GetThumbnail","WTSAT_ARGB","WTSAT_RGB","WTSAT_UNKNOWN","_shell_IThumbnailProvider_GetThumbnail","shell.IThumbnailProvider_GetThumbnail","thumbcache/IThumbnailProvider::GetThumbnail"]
old-location: shell\IThumbnailProvider_GetThumbnail.htm
tech.root: shell
ms.assetid: 5ea237fb-6b1c-4e87-a9f3-711ffa37b3dc
ms.date: 12/05/2018
ms.keywords: GetThumbnail, GetThumbnail method [Windows Shell], GetThumbnail method [Windows Shell],IThumbnailProvider interface, IThumbnailProvider interface [Windows Shell],GetThumbnail method, IThumbnailProvider.GetThumbnail, IThumbnailProvider::GetThumbnail, WTSAT_ARGB, WTSAT_RGB, WTSAT_UNKNOWN, _shell_IThumbnailProvider_GetThumbnail, shell.IThumbnailProvider_GetThumbnail, thumbcache/IThumbnailProvider::GetThumbnail
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
 - IThumbnailProvider::GetThumbnail
 - thumbcache/IThumbnailProvider::GetThumbnail
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
 - IThumbnailProvider.GetThumbnail
---

# IThumbnailProvider::GetThumbnail


## -description

Gets a thumbnail image and alpha type.

## -parameters

### -param cx [in]

Type: <b>UINT</b>

The maximum thumbnail size, in pixels. The Shell draws the returned bitmap at this size or smaller. The returned bitmap should fit into a square of width and height <i>cx</i>, though it does not need to be a square image. The Shell  scales the bitmap to render at lower sizes. For example, if the image has a 6:4 aspect ratio, then the returned bitmap should also have a 6:4 aspect ratio.

### -param phbmp [out]

Type: <b>HBITMAP*</b>

When this method returns, contains a pointer to the thumbnail image handle. The image must be a DIB section and 32 bits per pixel. The Shell scales down the bitmap if its width or height is larger than the size specified by <i>cx</i>. The Shell always respects the aspect ratio and never scales a bitmap larger than its original size.

### -param pdwAlpha [out]

Type: <b>WTS_ALPHATYPE*</b>

When this method returns, contains a pointer to one of the following values from the WTS_ALPHATYPE enumeration:



#### WTSAT_UNKNOWN (0x0)

0x0. The bitmap is an unknown format. The Shell tries nonetheless to detect whether the image has an alpha channel.



#### WTSAT_RGB (0x1)

0x1. The bitmap is an RGB image without alpha. The alpha channel is invalid and the Shell ignores it.



#### WTSAT_ARGB (0x2)

0x2. The bitmap is an ARGB image with a valid alpha channel.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

