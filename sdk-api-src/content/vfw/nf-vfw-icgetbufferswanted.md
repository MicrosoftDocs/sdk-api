---
UID: NF:vfw.ICGetBuffersWanted
title: ICGetBuffersWanted macro (vfw.h)
description: The ICGetBuffersWanted macro queries a driver for the number of buffers to allocate. You can use this macro or explicitly call the ICM_GETBUFFERSWANTED message.
helpviewer_keywords: ["ICGetBuffersWanted","ICGetBuffersWanted macro [Windows Multimedia]","_win32_ICGetBuffersWanted","multimedia.icgetbufferswanted","vfw/ICGetBuffersWanted"]
old-location: multimedia\icgetbufferswanted.htm
tech.root: Multimedia
ms.assetid: ed294649-d7e7-4e5f-89d4-49ed65c71b96
ms.date: 07/01/2025
ms.keywords: ICGetBuffersWanted, ICGetBuffersWanted macro [Windows Multimedia], _win32_ICGetBuffersWanted, multimedia.icgetbufferswanted, vfw/ICGetBuffersWanted
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICGetBuffersWanted
 - vfw/ICGetBuffersWanted
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - ICGetBuffersWanted
---

# ICGetBuffersWanted macro

## -syntax

```cpp
DWORD ICGetBuffersWanted(
     hic,
     lpdwBuffers
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns ICERR_OK if successful or ICERR_UNSUPPORTED otherwise.


## -description

The <b>ICGetBuffersWanted</b> macro queries a driver for the number of buffers to allocate. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/icm-getbufferswanted">ICM_GETBUFFERSWANTED</a> message.

## -parameters

### -param hic

Handle to a driver.

### -param lpdwBuffers

Address to contain the number of samples the driver needs to efficiently render the data.

## -remarks

This message is used by drivers that use hardware to render data and want to ensure a minimal time lag caused by waiting for buffers to arrive. For example, if a driver controls a video decompression board that can hold 10 frames of video, it could return 10 for this message. This instructs applications to try to stay 10 frames ahead of the frame it currently needs.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
