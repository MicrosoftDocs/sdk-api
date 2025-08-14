---
UID: NF:vfw.ICQueryAbout
title: ICQueryAbout macro (vfw.h)
description: The ICQueryAbout macro queries a video compression driver to determine if it has an About dialog box. You can use this macro or explicitly call the ICM_ABOUT message.
helpviewer_keywords: ["ICQueryAbout","ICQueryAbout macro [Windows Multimedia]","_win32_ICQueryAbout","multimedia.icqueryabout","vfw/ICQueryAbout"]
old-location: multimedia\icqueryabout.htm
tech.root: Multimedia
ms.assetid: 073f217f-961b-4de2-9430-5ee81379e807
ms.date: 07/01/2025
ms.keywords: ICQueryAbout, ICQueryAbout macro [Windows Multimedia], _win32_ICQueryAbout, multimedia.icqueryabout, vfw/ICQueryAbout
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
 - ICQueryAbout
 - vfw/ICQueryAbout
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
 - ICQueryAbout
---

# ICQueryAbout macro

## -syntax

```cpp
DWORD ICQueryAbout(
     hic
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns ICERR_OK if the driver supports this message or ICERR_UNSUPPORTED otherwise.


## -description

The <b>ICQueryAbout</b> macro queries a video compression driver to determine if it has an About dialog box. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/icm-about">ICM_ABOUT</a> message.

## -parameters

### -param hic

Handle of the compressor.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
