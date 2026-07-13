---
UID: NF:vfw.ICConfigure
title: ICConfigure macro (vfw.h)
description: The ICConfigure macro notifies a video compression driver to display its configuration dialog box. You can use this macro or explicitly send the ICM_CONFIGURE message.
helpviewer_keywords: ["ICConfigure","ICConfigure macro [Windows Multimedia]","_win32_ICConfigure","multimedia.icconfigure","vfw/ICConfigure"]
old-location: multimedia\icconfigure.htm
tech.root: Multimedia
ms.assetid: 58dbe8ff-4236-456c-8361-e7716e764f89
ms.date: 07/01/2025
ms.keywords: ICConfigure, ICConfigure macro [Windows Multimedia], _win32_ICConfigure, multimedia.icconfigure, vfw/ICConfigure
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
 - ICConfigure
 - vfw/ICConfigure
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
 - ICConfigure
---

# ICConfigure macro

## -syntax

```cpp
DWORD ICConfigure(
     hic,
     hwnd
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns ICERR_OK if the driver supports this macro or ICERR_UNSUPPORTED otherwise.


## -description

The <b>ICConfigure</b> macro notifies a video compression driver to display its configuration dialog box. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/icm-configure">ICM_CONFIGURE</a> message.

## -parameters

### -param hic

Handle of the compressor.

### -param hwnd

Handle of the parent window of the displayed dialog box.

## -remarks

The <a href="/windows/desktop/Multimedia/icm-configure">ICM_CONFIGURE</a> message is different from the <a href="/windows/desktop/Multimedia/drv-configure">DRV_CONFIGURE</a> message used for hardware configuration. The dialog box for this message should let the user set and edit the internal state referenced by the <a href="/windows/desktop/api/vfw/nf-vfw-icgetstate">ICGetState</a> and <a href="/windows/desktop/api/vfw/nf-vfw-icsetstate">ICSetState</a> macros. For example, this dialog box can let the user change parameters affecting the quality level and other similar compression options.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
