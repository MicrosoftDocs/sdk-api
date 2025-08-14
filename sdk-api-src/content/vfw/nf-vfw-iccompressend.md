---
UID: NF:vfw.ICCompressEnd
title: ICCompressEnd macro (vfw.h)
description: The ICCompressEnd macro notifies a video compression driver to end compression and free resources allocated for compression. You can use this macro or explicitly call the ICM_COMPRESS_END message.
helpviewer_keywords: ["ICCompressEnd","ICCompressEnd macro [Windows Multimedia]","_win32_ICCompressEnd","multimedia.iccompressend","vfw/ICCompressEnd"]
old-location: multimedia\iccompressend.htm
tech.root: Multimedia
ms.assetid: 04daaf34-63c3-40c1-9ed6-2ae07558d1b8
ms.date: 07/01/2025
ms.keywords: ICCompressEnd, ICCompressEnd macro [Windows Multimedia], _win32_ICCompressEnd, multimedia.iccompressend, vfw/ICCompressEnd
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
 - ICCompressEnd
 - vfw/ICCompressEnd
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
 - ICCompressEnd
---

# ICCompressEnd macro

## -syntax

```cpp
DWORD ICCompressEnd(
     hic
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns ICERR_OK if successful or an error otherwise.


## -description

The <b>ICCompressEnd</b> macro notifies a video compression driver to end compression and free resources allocated for compression. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/icm-compress-end">ICM_COMPRESS_END</a> message.

## -parameters

### -param hic

Handle of the compressor.

## -remarks

VCM saves the settings of the most recent <b>ICCompressBegin</b> macro. <b>ICCompressBegin</b> and <b>ICCompressEnd</b> do not nest. If your driver receives the <b>ICM_COMPRESS_BEGIN</b> message before compression is stopped with the <b>ICM_COMPRESS_END</b> message, it should restart compression with new parameters.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
