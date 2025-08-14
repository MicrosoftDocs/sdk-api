---
UID: NF:vfw.ICGetDefaultQuality
title: ICGetDefaultQuality macro (vfw.h)
description: The ICGetDefaultQuality macro queries a video compression driver to provide its default quality setting. You can use this macro or explicitly call the ICM_GETDEFAULTQUALITY message.
helpviewer_keywords: ["ICGetDefaultQuality","ICGetDefaultQuality macro [Windows Multimedia]","_win32_ICGetDefaultQuality","multimedia.icgetdefaultquality","vfw/ICGetDefaultQuality"]
old-location: multimedia\icgetdefaultquality.htm
tech.root: Multimedia
ms.assetid: dd88a141-5461-4725-83f9-c2ead3a3a2b6
ms.date: 07/01/2025
ms.keywords: ICGetDefaultQuality, ICGetDefaultQuality macro [Windows Multimedia], _win32_ICGetDefaultQuality, multimedia.icgetdefaultquality, vfw/ICGetDefaultQuality
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
 - ICGetDefaultQuality
 - vfw/ICGetDefaultQuality
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
 - ICGetDefaultQuality
---

# ICGetDefaultQuality macro

## -syntax

```cpp
DWORD ICGetDefaultQuality(
     hic,
     wParam
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns ICERR_OK if the driver supports this message or ICERR_UNSUPPORTED otherwise.


## -description

The <b>ICGetDefaultQuality</b> macro queries a video compression driver to provide its default quality setting. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/icm-getdefaultquality">ICM_GETDEFAULTQUALITY</a> message.

## -parameters

### -param hic

Handle to a compressor. 


#### - wParam

Address to contain the default quality value. Quality values range from 0 to 10,000.

## -remarks

The <b>ICGetDefaultQuality</b> macro returns the default quality value.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
