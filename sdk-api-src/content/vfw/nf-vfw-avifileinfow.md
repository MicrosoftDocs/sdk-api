---
UID: NF:vfw.AVIFileInfoW
title: AVIFileInfoW function (vfw.h)
description: The AVIFileInfoW function (vfw.h) obtains information about an AVI file.
helpviewer_keywords: ["AVIFileInfo", "AVIFileInfo function [Windows Multimedia]", "AVIFileInfoW", "_win32_AVIFileInfo", "multimedia.avifileinfo", "vfw/AVIFileInfo", "vfw/AVIFileInfoW"]
old-location: multimedia\avifileinfo.htm
tech.root: Multimedia
ms.assetid: 10d7decf-a133-4d55-93d5-867952307819
ms.date: 08/16/2022
ms.keywords: AVIFileInfo, AVIFileInfo function [Windows Multimedia], AVIFileInfoA, AVIFileInfoW, _win32_AVIFileInfo, multimedia.avifileinfo, vfw/AVIFileInfo, vfw/AVIFileInfoA, vfw/AVIFileInfoW
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AVIFileInfoW (Unicode) and AVIFileInfoA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Vfw32.lib
req.dll: Avifil32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AVIFileInfoW
 - vfw/AVIFileInfoW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avifil32.dll
 - Ext-MS-Win-Media-Avi-L1-1-0.dll
api_name:
 - AVIFileInfo
 - AVIFileInfoA
 - AVIFileInfoW
---

# AVIFileInfoW function


## -description

The <b>AVIFileInfo</b> function obtains information about an AVI file.

## -parameters

### -param pfile

Handle to an open AVI file.

### -param pfi

Pointer to the structure used to return file information. Typically, this parameter points to an <a href="/windows/desktop/api/vfw/ns-vfw-avifileinfoa">AVIFILEINFO</a> structure.

### -param lSize

Size, in bytes, of the structure.

## -returns

Returns zero if successful or an error otherwise.

## -remarks

The argument <i>pfile</i> is a pointer to an <a href="/windows/desktop/api/vfw/nn-vfw-iavifile">IAVIFile</a> interface.





> [!NOTE]
> The vfw.h header defines AVIFILEINFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>
