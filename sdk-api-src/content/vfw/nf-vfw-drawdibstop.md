---
UID: NF:vfw.DrawDibStop
title: DrawDibStop function (vfw.h)
description: The DrawDibStop function frees the resources used by a DrawDib DC for streaming playback.
helpviewer_keywords: ["DrawDibStop","DrawDibStop function [Windows Multimedia]","_win32_DrawDibStop","multimedia.drawdibstop","vfw/DrawDibStop"]
old-location: multimedia\drawdibstop.htm
tech.root: Multimedia
ms.assetid: 8744d0d2-bcdc-464f-a55c-4b1db6a42522
ms.date: 12/05/2018
ms.keywords: DrawDibStop, DrawDibStop function [Windows Multimedia], _win32_DrawDibStop, multimedia.drawdibstop, vfw/DrawDibStop
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
 - DrawDibStop
 - vfw/DrawDibStop
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
 - DrawDibStop
---

# DrawDibStop function


## -description

The <b>DrawDibStop</b> function frees the resources used by a DrawDib DC for streaming playback.

## -parameters

### -param hdd

Handle to a DrawDib DC.

## -returns

Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.

## -see-also

<a href="/windows/desktop/Multimedia/drawdib-functions">DrawDib Functions</a>