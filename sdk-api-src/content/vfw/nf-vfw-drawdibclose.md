---
UID: NF:vfw.DrawDibClose
title: DrawDibClose function (vfw.h)
description: The DrawDibClose function closes a DrawDib DC and frees the resources DrawDib allocated for it.
helpviewer_keywords: ["DrawDibClose","DrawDibClose function [Windows Multimedia]","_win32_DrawDibClose","multimedia.drawdibclose","vfw/DrawDibClose"]
old-location: multimedia\drawdibclose.htm
tech.root: Multimedia
ms.assetid: 61f9784e-4992-43d2-9770-17c3a8e5078b
ms.date: 12/05/2018
ms.keywords: DrawDibClose, DrawDibClose function [Windows Multimedia], _win32_DrawDibClose, multimedia.drawdibclose, vfw/DrawDibClose
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
req.lib: Vfw32.lib
req.dll: Msvfw32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrawDibClose
 - vfw/DrawDibClose
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msvfw32.dll
api_name:
 - DrawDibClose
---

# DrawDibClose function


## -description

The <b>DrawDibClose</b> function closes a DrawDib DC and frees the resources DrawDib allocated for it.

## -parameters

### -param hdd

Handle to a DrawDib DC.

## -returns

Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.

## -see-also

<a href="/windows/desktop/Multimedia/drawdib-functions">DrawDib Functions</a>