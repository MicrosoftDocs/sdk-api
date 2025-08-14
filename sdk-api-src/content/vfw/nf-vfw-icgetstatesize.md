---
UID: NF:vfw.ICGetStateSize
title: ICGetStateSize macro (vfw.h)
description: The ICGetStateSize macro queries a video compression driver to determine the amount of memory required to retrieve the configuration information. You can use this macro or explicitly call the ICM_GETSTATE message.
helpviewer_keywords: ["ICGetStateSize","ICGetStateSize macro [Windows Multimedia]","_win32_ICGetStateSize","multimedia.icgetstatesize","vfw/ICGetStateSize"]
old-location: multimedia\icgetstatesize.htm
tech.root: Multimedia
ms.assetid: 386761e8-9234-4541-b593-ce8e323714bf
ms.date: 07/01/2025
ms.keywords: ICGetStateSize, ICGetStateSize macro [Windows Multimedia], _win32_ICGetStateSize, multimedia.icgetstatesize, vfw/ICGetStateSize
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
 - ICGetStateSize
 - vfw/ICGetStateSize
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
 - ICGetStateSize
---

# ICGetStateSize macro

## -syntax

```cpp
DWORD ICGetStateSize(
     hic
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns the amount of memory, in bytes, required by the state information.


## -description

The <b>ICGetStateSize</b> macro queries a video compression driver to determine the amount of memory required to retrieve the configuration information. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/icm-getstate">ICM_GETSTATE</a> message.

## -parameters

### -param hic

Handle of the compressor.

## -remarks

The structure used to represent configuration information is driver specific and is defined by the driver.

Use <b>ICGetStateSize</b> before calling the <a href="/windows/desktop/api/vfw/nf-vfw-icgetstate">ICGetState</a> macro to determine the size of buffer to allocate for the call.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
