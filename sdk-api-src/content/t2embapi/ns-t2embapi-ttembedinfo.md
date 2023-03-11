---
UID: NS:t2embapi.TTEMBEDINFO
title: TTEMBEDINFO (t2embapi.h)
description: The TTEMBEDINFO structure contains a list of URLs from which the embedded font object may be legitimately referenced.
helpviewer_keywords: ["TTEMBEDINFO","TTEMBEDINFO structure [Windows GDI]","_win32_TTEMBEDINFO","gdi.ttembedinfo","t2embapi/TTEMBEDINFO"]
old-location: gdi\ttembedinfo.htm
tech.root: gdi
ms.assetid: 7e1828bf-c9ed-4120-b91f-b4eb45191e48
ms.date: 12/05/2018
ms.keywords: TTEMBEDINFO, TTEMBEDINFO structure [Windows GDI], _win32_TTEMBEDINFO, gdi.ttembedinfo, t2embapi/TTEMBEDINFO
req.header: t2embapi.h
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
req.typenames: TTEMBEDINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TTEMBEDINFO
 - t2embapi/TTEMBEDINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - T2embapi.h
api_name:
 - TTEMBEDINFO
---

# TTEMBEDINFO structure


## -description

The <b>TTEMBEDINFO</b> structure contains a list of URLs from which the embedded font object may be legitimately referenced.

## -struct-fields

### -field usStructSize

Size, in bytes, of this structure. The client should set this value to <b>sizeof</b>(TTEMBEDINFO).

### -field usRootStrSize

Size, in wide characters, of <i>pusRootStr</i> including NULL terminator(s).

### -field pusRootStr

One or more full URLs that the embedded font object may be referenced from. Multiple URLs, separated by NULL terminators, can be specified.

## -see-also

<a href="/windows/desktop/api/t2embapi/nf-t2embapi-ttembedfont">TTEmbedFont</a>



<a href="/windows/desktop/api/t2embapi/nf-t2embapi-ttembedfontex">TTEmbedFontEx</a>



<a href="/windows/desktop/api/t2embapi/nf-t2embapi-ttembedfontfromfilea">TTEmbedFontFromFileA</a>



<a href="/windows/desktop/api/t2embapi/nf-t2embapi-ttloadembeddedfont">TTLoadEmbeddedFont</a>

