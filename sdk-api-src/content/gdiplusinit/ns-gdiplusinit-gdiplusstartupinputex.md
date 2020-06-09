---
UID: NS:gdiplusinit.GdiplusStartupInputEx
title: GdiplusStartupInputEx
ms.date: 05/07/2020
ms.topic: language-reference
targetos: Windows
description: The **GdiplusStartupInputEx** structure holds a block of arguments that are required by the [GdiplusStartup](/windows/win32/api/gdiplusinit/nf-gdiplusinit-gdiplusstartup) function.
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: gdiplusinit.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - gdiplusinit.h
api_name:
 - GdiplusStartupInputEx
f1_keywords:
 - gdiplusinit/GdiplusStartupInputEx
dev_langs:
 - c++
---

## -description

The **GdiplusStartupInputEx** structure holds a block of arguments that are required by the [GdiplusStartup](/windows/win32/api/gdiplusinit/nf-gdiplusinit-gdiplusstartup) function. **GdiplusStartupInputEx** derives from [**GdiplusStartupInput**](/windows/win32/api/gdiplusinit/nf-gdiplusinit-gdiplusstartupinput-gdiplusstartupinput).

## -struct-fields

### -field StartupParameters

Type: **INT**

See [**GdiplusStartupParams**](/windows/win32/api/gdiplusinit/ne-gdiplusinit-gdiplusstartupparams). The default value is **GdiplusStartupDefault** (0).

## -remarks

## -see-also