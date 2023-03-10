---
UID: NS:t2embapi.TTLOADINFO
title: TTLOADINFO (t2embapi.h)
description: The TTLOADINFO structure contains the URL from which the embedded font object has been obtained.
helpviewer_keywords: ["TTLOADINFO","TTLOADINFO structure [Windows GDI]","_win32_TTLOADINFO","gdi.ttloadinfo","t2embapi/TTLOADINFO"]
old-location: gdi\ttloadinfo.htm
tech.root: gdi
ms.assetid: 7a4beae7-cd30-47e3-b310-d0a79c3c8c36
ms.date: 12/05/2018
ms.keywords: TTLOADINFO, TTLOADINFO structure [Windows GDI], _win32_TTLOADINFO, gdi.ttloadinfo, t2embapi/TTLOADINFO
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
req.typenames: TTLOADINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TTLOADINFO
 - t2embapi/TTLOADINFO
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
 - TTLOADINFO
---

# TTLOADINFO structure


## -description

The <b>TTLOADINFO</b> structure contains the URL from which the embedded font object has been obtained.

## -struct-fields

### -field usStructSize

Size, in bytes, of this structure. The client should set this value to <b>sizeof</b>(TTLOADINFO).

### -field usRefStrSize

Size, in wide characters, of <i>pusRefStr</i>, including the terminating null character.

### -field pusRefStr

Pointer to the string containing the current URL.

## -see-also

<a href="/windows/desktop/api/t2embapi/ns-t2embapi-ttembedinfo">TTEMBEDINFO</a>



<a href="/windows/desktop/api/t2embapi/nf-t2embapi-ttloadembeddedfont">TTLoadEmbeddedFont</a>

