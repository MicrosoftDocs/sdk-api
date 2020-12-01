---
UID: NF:vfw.DrawDibStart
title: DrawDibStart function (vfw.h)
description: The DrawDibStart function prepares a DrawDib DC for streaming playback.
helpviewer_keywords: ["DrawDibStart","DrawDibStart function [Windows Multimedia]","_win32_DrawDibStart","multimedia.drawdibstart","vfw/DrawDibStart"]
old-location: multimedia\drawdibstart.htm
tech.root: Multimedia
ms.assetid: 2c992a4f-3308-4f0a-a1cf-40515e28ae33
ms.date: 12/05/2018
ms.keywords: DrawDibStart, DrawDibStart function [Windows Multimedia], _win32_DrawDibStart, multimedia.drawdibstart, vfw/DrawDibStart
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
 - DrawDibStart
 - vfw/DrawDibStart
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
 - DrawDibStart
---

# DrawDibStart function


## -description

The <b>DrawDibStart</b> function prepares a DrawDib DC for streaming playback.

## -parameters

### -param hdd

Handle to a DrawDib DC.

### -param rate

Playback rate, in microseconds per frame.

## -returns

Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.

## -see-also

<a href="/windows/desktop/Multimedia/drawdib-functions">DrawDib Functions</a>