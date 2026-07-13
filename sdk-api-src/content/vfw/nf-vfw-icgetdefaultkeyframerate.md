---
UID: NF:vfw.ICGetDefaultKeyFrameRate
title: ICGetDefaultKeyFrameRate macro (vfw.h)
description: The ICGetDefaultKeyFrameRate macro queries a video compression driver for its default (or preferred) key-frame spacing. You can use this macro or explicitly call the ICM_GETDEFAULTKEYFRAMERATE message.
helpviewer_keywords: ["ICGetDefaultKeyFrameRate","ICGetDefaultKeyFrameRate macro [Windows Multimedia]","_win32_ICGetDefaultKeyFrameRate","multimedia.icgetdefaultkeyframerate","vfw/ICGetDefaultKeyFrameRate"]
old-location: multimedia\icgetdefaultkeyframerate.htm
tech.root: Multimedia
ms.assetid: 81ae287a-13e3-4bf0-bdd8-915a81e78d32
ms.date: 07/01/2025
ms.keywords: ICGetDefaultKeyFrameRate, ICGetDefaultKeyFrameRate macro [Windows Multimedia], _win32_ICGetDefaultKeyFrameRate, multimedia.icgetdefaultkeyframerate, vfw/ICGetDefaultKeyFrameRate
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
 - ICGetDefaultKeyFrameRate
 - vfw/ICGetDefaultKeyFrameRate
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
 - ICGetDefaultKeyFrameRate
---

# ICGetDefaultKeyFrameRate macro

## -syntax

```cpp
DWORD ICGetDefaultKeyFrameRate(
     hic,
     wParam
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns ICERR_OK if the driver supports this message or ICERR_UNSUPPORTED otherwise.


## -description

The <b>ICGetDefaultKeyFrameRate</b> macro queries a video compression driver for its default (or preferred) key-frame spacing. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/icm-getdefaultkeyframerate">ICM_GETDEFAULTKEYFRAMERATE</a> message.

## -parameters

### -param hic

Handle to a compressor. 


#### - wParam

Address to contain the preferred key-frame spacing.

## -remarks

The <b>ICGetDefaultKeyFrameRate</b> macro returns the default key frame rate.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
