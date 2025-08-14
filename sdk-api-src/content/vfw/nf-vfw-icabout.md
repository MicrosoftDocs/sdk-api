---
UID: NF:vfw.ICAbout
title: ICAbout macro (vfw.h)
description: The ICAbout macro notifies a video compression driver to display its About dialog box. You can use this macro or explicitly call the ICM_ABOUT message.
helpviewer_keywords: ["ICAbout","ICAbout macro [Windows Multimedia]","_win32_ICAbout","multimedia.icabout","vfw/ICAbout"]
old-location: multimedia\icabout.htm
tech.root: Multimedia
ms.assetid: 18ec2659-8589-4a13-95ea-825a3aecbf98
ms.date: 07/01/2025
ms.keywords: ICAbout, ICAbout macro [Windows Multimedia], _win32_ICAbout, multimedia.icabout, vfw/ICAbout
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
 - ICAbout
 - vfw/ICAbout
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
 - ICAbout
---

# ICAbout macro

## -syntax

```cpp
DWORD ICAbout(
     hic,
     hwnd
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns ICERR_OK if the driver supports this message or ICERR_UNSUPPORTED otherwise.


## -description

The <b>ICAbout</b> macro notifies a video compression driver to display its About dialog box. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/icm-about">ICM_ABOUT</a> message.

## -parameters

### -param hic

Handle of the compressor.

### -param hwnd

Handle of the parent window of the displayed dialog box.

You can also determine if a driver has an About dialog box by specifying -1 in this parameter, as in the <a href="/windows/desktop/api/vfw/nf-vfw-icqueryabout">ICQueryAbout</a> macro. The driver returns ICERR_OK if it has an About dialog box or ICERR_UNSUPPORTED otherwise.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
